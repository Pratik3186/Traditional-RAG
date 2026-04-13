# 🚀 Advanced RAG Pipeline (Production-Ready)

A **production-grade Retrieval-Augmented Generation (RAG) system** built using modern LLM tooling.
This project demonstrates **end-to-end document understanding**, semantic search, and intelligent answer generation with **citations, summaries, and history tracking**.

---

## 🔥 Key Features

* 📄 **PDF/Text Document Ingestion**
* ✂️ **Smart Chunking (Recursive Splitting)**
* 🧠 **Semantic Embeddings (Sentence Transformers)**
* ⚡ **Vector Search (FAISS)**
* 🤖 **LLM Integration (Groq - LLaMA 3.1)**
* 📌 **Context-aware Answer Generation**
* 🔗 **Citations (source + page tracking)**
* 🧾 **Answer Summarization**
* 🕓 **Query History Tracking**
* ⚡ **Streaming Responses (LLM output)**

---

## 🏗️ Architecture Diagram

```
                ┌────────────────────┐
                │    User Query      │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │  Query Embedding   │
                │ (SentenceTransformer)
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │   Vector Store     │
                │     (FAISS)        │
                └─────────┬──────────┘
                          │
                Top-K Relevant Chunks
                          │
                          ▼
                ┌────────────────────┐
                │  Context Builder   │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │      LLM (Groq)    │
                │   LLaMA 3.1 Model  │
                └─────────┬──────────┘
                          │
                          ▼
        ┌─────────────────────────────────────┐
        │ Answer + Citations + Summary       │
        └─────────────────────────────────────┘
                          │
                          ▼
                ┌────────────────────┐
                │   History Store    │
                └────────────────────┘
```

---

## 🧠 How It Works

1. **Documents are loaded** (PDF/Text)
2. Split into chunks using **RecursiveCharacterTextSplitter**
3. Convert chunks → **vector embeddings**
4. Store embeddings in **FAISS vector database**
5. User query → converted to embedding
6. Retrieve top-K similar chunks
7. Pass context + query to **Groq LLM**
8. Generate:

   * Answer ✅
   * Citations ✅
   * Summary ✅
9. Store interaction in **history**

---

## ⚙️ Tech Stack

* **LangChain**
* **Groq API (LLaMA 3.1)**
* **FAISS (Vector DB)**
* **Sentence Transformers**
* **Python**
* **Jupyter Notebook**

---

## 📁 Project Structure

```
Traditional_RAG/
│
├── data/
│   ├── pdf/
│   └── text_files/
│
├── notebook/
│   └── document.ipynb
│
├── vector_store/        # (ignored in git)
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env.example
```

---

## 🔐 Environment Setup

Create `.env` file:

```
GROQ_API_KEY=your_api_key_here
```

---

## 🚀 Installation

```bash
git clone https://github.com/your-username/Traditional-RAG.git
cd Traditional-RAG

pip install -r requirements.txt
```

---

## ▶️ Usage

Run your notebook or script:

```bash
python main.py
```

Example query:

```
What is RAG?
```

---

## 🧾 Sample Output

```
Answer:
RAG (Retrieval-Augmented Generation) combines retrieval of relevant documents
with LLM-based generation...

Citations:
[1] research_paper.pdf (page 3)

Summary:
RAG improves LLM accuracy by grounding responses in retrieved data.
```

---

## 🧠 Why This Project Matters

This project demonstrates:

* Real-world **LLM system design**
* Understanding of **vector databases**
* Practical use of **RAG architecture**
* Handling **LLM limitations (hallucination)**

---

## 💡 Future Improvements

* 🔍 Hybrid Search (BM25 + Vector)
* 🧠 Re-ranking (Cross-Encoder)
* 🌐 Web UI (Streamlit / React)
* 📊 Evaluation Metrics (RAGAS)
* 🔄 Real-time document updates

---

## 🏆 Resume Highlight

> Built a production-ready Retrieval-Augmented Generation (RAG) system using FAISS, Groq LLM, and LangChain with features like citation tracking, summarization, and semantic search.

---

## 📬 Contact

**Pratik**

* GitHub: https://github.com/Pratik3186

---

⭐ If you like this project, give it a star!
