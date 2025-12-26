# 🤖 FinBot: Hybrid AI Financial Analyst (Cloud + Local)

![Python](https://img.shields.io/badge/Tech-OpenAI%20%7C%20Ollama-green)
![Models](https://img.shields.io/badge/LLMs-GPT4%20%7C%20TinyLlama-blue)
![Frontend](https://img.shields.io/badge/Frontend-Streamlit-red)

## 📋 Executive Summary
Financial analysts often struggle to extract insights from dense 10-K reports.
**FinBot** is a Dual-Mode RAG Application (Retrieval-Augmented Generation) that allows users to chat with financial PDFs.

It features a **Hybrid Architecture**:
1.  **Cloud Mode (Production):** Uses OpenAI (GPT-3.5) for high-precision, client-facing answers.
2.  **Local Mode (Privacy/Dev):** Uses Ollama (TinyLlama/Phi-3) to run 100% offline and free on local hardware.

## 🛠️ Technical Architecture

### ☁️ Option A: Cloud (High Accuracy)
* **LLM:** GPT-3.5-Turbo (OpenAI)
* **Embeddings:** OpenAI Embeddings (ada-002)
* **Pros:** Best reasoning capability, fast response.
* **Cons:** Costs per token ($).

### 💻 Option B: Local (Privacy & Free)
* **LLM:** TinyLlama (1.1B) or Phi-3 (3.8B) running via **Ollama**.
* **Embeddings:** HuggingFace (`all-MiniLM-L6-v2`) running on CPU.
* **Pros:** 100% Free, Data never leaves the laptop (Privacy).
* **Cons:** Depends on local RAM/CPU.

## 🚀 How to Run

### Prerequisites
1.  Python 3.10+
2.  [Ollama](https://ollama.com/) installed (for Local mode).

### Installation
```bash
pip install streamlit PyPDF2 langchain-text-splitters langchain-openai langchain-community faiss-cpu

1️⃣ Running Cloud Mode (OpenAI)
Requires an API Key.

Bash
streamlit run app.py

2️⃣ Running Local Mode (Ollama)
Requires pulling the model first (ollama run tinyllama).

Bash
streamlit run app_local.py

💼 Business Value
Cost Optimization: Use Local mode for development/testing and Cloud mode for final reports.

Data Privacy: Local mode ensures sensitive financial data is processed entirely on-premise.

Author
Glauber Rocha - Data Scientist & AI Engineer
