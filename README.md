# AI Financial Anomaly Detection Agent

[![Frontend Deployment](https://img.shields.io/badge/Frontend-Live%20Demo-brightgreen?style=for-the-badge&logo=vercel)](https://anomaly-detection-frontend-topaz.vercel.app/)
[![Backend Status](https://img.shields.io/badge/Backend-API%20Live-blue?style=for-the-badge&logo=render)](https://anomaly-detection-backend-5zl8.onrender.com)

An intelligent full-stack application that leverages Large Language Models (LLMs) to analyze financial transaction data and identify potential risks, duplicates, and suspicious patterns. This tool moves beyond traditional rule-based systems by using the contextual reasoning power of modern AI to provide nuanced, human-like analysis of financial data.

 
![AI Anomaly Detector](https://github.com/user-attachments/assets/b55138e7-56cc-4ba2-a2a5-d1c3d43ab967)



---

## 📖 Introduction

In the world of finance and operations, identifying anomalous transactions is a critical but often manual and time-consuming task. Traditional systems rely on rigid rules that can miss subtle, context-dependent risks.

This **AI Financial Anomaly Detection Agent** was built to solve this problem. It provides a user-friendly interface for uploading raw transaction data (CSV) and returns a sophisticated, AI-driven analysis in seconds. The backend uses a carefully engineered prompt to instruct **GPT-4o-mini** to act as a senior fraud analyst, allowing it to detect anomalies that are not just numerically out of place but also contextually suspicious.

This project showcases skills in full-stack development, applied AI, data analysis, and building practical FinTech solutions.

---

## ✨ Features

-   **🧠 Intelligent Anomaly Detection:** Utilizes LLM reasoning to detect a wide range of anomalies, including:
    -   Duplicate transactions.
    -   Unusually high amounts for a given category.
    -   Transactions at odd hours (e.g., late at night).
    -   Suspicious vendor patterns.
-   **📊 Dynamic Results Dashboard:** Presents complex AI output in a clean, user-friendly interface with:
    -   **Summary Cards:** At-a-glance metrics for total anomalies, highest risk amount, and common issues.
    -   **Detailed Anomalies Table:** A sortable table listing each flagged transaction with its severity, confidence score, and a clear reason from the AI.
-   **⬆️ Simple CSV Upload:** Effortless file upload and parsing for any standard transaction CSV.
-   **🌗 Dark/Light Theme:** A sleek, modern UI with a persistent dark/light mode toggle managed with Zustand.

---

## 🔧 Tech Stack & Architecture

This project is built with a modern, full-stack architecture designed for performance, scalability, and a great developer experience.

### **🧠 AI/ML Layer (Backend Intelligence)**

| Component         | Description                                                                              |
| :---------------- | :--------------------------------------------------------------------------------------- |
| **GPT-4o-mini**   | The core LLM used via **OpenRouter** to perform contextual anomaly detection.            |
| **Prompt Eng.**   | A carefully crafted system prompt guides the model to return structured, reliable JSON data. |

### **🖥️ Frontend (Client-Side Web App)**

| Tool/Library      | Purpose                                                                |
| :---------------- | :--------------------------------------------------------------------- |
| **React**         | For building the interactive and component-based user interface.       |
| **Tailwind CSS**  | Utility-first CSS framework for rapid, responsive UI development.      |
| **Zustand**       | Minimalist global state management for theme and analysis data.        |
| **Framer Motion** | For smooth, polished animations and page transitions.                  |
| **Lucide React**  | For clean and modern icons used in the UI.                             |
| **Vite**          | A fast, modern build tool for a superior development experience.       |

### **🌐 Backend (API & AI Communication)**

| Component         | Description                                                                          |
| :---------------- | :----------------------------------------------------------------------------------- |
| **FastAPI**       | A high-performance Python web framework for building the `/analyze` API endpoint.      |
| **Pandas**        | For robust and efficient parsing and manipulation of the uploaded CSV data.          |
| **OpenRouter**    | Acts as a gateway to access various LLMs, providing flexibility and reliability.     |
| **CORS**          | FastAPI middleware configured to securely allow requests from the Vercel-hosted frontend. |

---

## 🚀 How to Use

1.  **Navigate** to the live demo: [https://anomaly-detection-frontend-topaz.vercel.app/](https://anomaly-detection-frontend-topaz.vercel.app/)
2.  **Upload a CSV file** containing transaction data. The file should have columns like `date`, `amount`, `vendor`, and `description`.
3.  **Click the "Analyze Transactions" button.**
4.  The app will process the file, call the backend AI agent, and display the results on the dashboard.
5.  **Review the anomalies** in the summary cards and the detailed table.
6.  **Toggle dark mode** for your preferred viewing experience!
