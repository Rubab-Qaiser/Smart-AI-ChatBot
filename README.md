

# 🤖 Company AI Assistant (RAG System using Gemini + ChromaDB)

## 📌 Overview

This project is an **AI-powered HR Knowledge Base Assistant** built using:

* 🧠 Retrieval-Augmented Generation (RAG)
* 🗂️ ChromaDB (Vector Database)
* 🔍 Embeddings (Google Gemini / optional local embeddings)
* 💬 Gemini LLM (Gemini 2.5 Flash)
* 🎨 Streamlit (UI)

It allows employees to ask questions about company policies such as:

* Leave policy
* Remote work policy
* Maternity leave
* Work-from-home guidelines
* HR procedures

---

## ⚙️ How It Works

The system follows this pipeline:

```text
User Query
   ↓
Text Embedding (Gemini or Local Model)
   ↓
Vector Search (ChromaDB)
   ↓
Relevant Document Retrieval
   ↓
Context Injection into LLM
   ↓
Final Answer Generation
```

---

## 🧠 Key Features

### ✅ RAG-based Question Answering

Answers are strictly based on company documents.

### ✅ Semantic Search

Finds meaning-based matches (not just keywords).

### ✅ Vector Database

Uses ChromaDB for storing embeddings locally.

### ✅ Streamlit UI

Interactive chat-based interface.

### ✅ HR Knowledge Base

Supports:

* Policies
* Employee guidelines
* Internal documentation

---

## 📁 Project Structure

```
project/
│
├── app.py                      # Streamlit application
├── company_documents/         # HR policy text files
│   ├── leave_policy.txt
│   ├── remote_work.txt
│   └── benefits.txt
│
├── chroma_db/                 # Vector database storage
├── .env                       # API keys (not pushed to GitHub)
└── requirements.txt
```

---

## 🚀 Installation Guide

### 1️⃣ Clone Repository

```bash
git clone https://github.com/your-repo/company-ai-assistant.git
cd company-ai-assistant
```

---

### 2️⃣ Create Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Add Environment Variables

Create a `.env` file:

```env
Course_AI_Lab=YOUR_GEMINI_API_KEY
```

---

### 5️⃣ Run Application

```bash
streamlit run app.py
```

---

## 🔑 API Requirements

This project uses:

### Google Gemini API

* Embeddings: `gemini-embedding-001`
* LLM: `gemini-2.5-flash`

Get API key:
👉 [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)

---

## 📊 Example Questions

Users can ask:

* What is the leave policy?
* Can I work remotely?
* What are maternity leave benefits?
* What is the dress code policy?
* How many paid leaves do employees get?

---

## 🧪 System Architecture

```text
📄 Documents
   ↓
✂️ Chunking (Text Splitter)
   ↓
🧠 Embeddings (Gemini / Local Model)
   ↓
🗃️ ChromaDB Storage
   ↓
🔍 Similarity Search
   ↓
🤖 Gemini LLM Response
```

---

## ⚠️ Known Issues

### 1. API Quota Limits

* Free tier has limited requests (e.g., 20/day)
* Solution: add caching or local embeddings

### 2. Empty Knowledge Base

* If `chroma_db` is not initialized, no results will be found
* Fix: ensure ingestion runs on startup

### 3. Missing Dependencies

Install:

```bash
pip install langchain-community langchain-text-splitters chromadb streamlit
```

---

## 🚀 Future Improvements

* 🔥 Fully offline RAG (no API calls)
* ⚡ Hybrid search (keyword + semantic)
* 📦 FastAPI backend version
* ☁️ Cloud deployment (Streamlit Cloud / Render)
* 🧠 Multi-language support
* 📊 Analytics dashboard

---


## 👨‍💻 Tech Stack

* Python 🐍
* Streamlit 🎨
* ChromaDB 🗂️
* Google Gemini API 🧠
* LangChain 🧩
* Sentence Transformers (optional)

---




