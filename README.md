# 🚀 Advanced RAG Pipeline with Typesense + Groq

A **production-ready Retrieval-Augmented Generation (RAG) system** that combines:

⚡ **Semantic Search (Vector DB)** + 🔍 **Keyword Search (Typesense)** + 🤖 **LLM (Groq)**

This project demonstrates a **Hybrid RAG architecture**, improving retrieval accuracy and reducing hallucinations in LLM responses.

---

## 🔥 Key Features

* 📄 PDF & Text Document Ingestion
* ✂️ Intelligent Chunking
* 🧠 Semantic Embeddings (Sentence Transformers)
* ⚡ Vector Search (FAISS)
* 🔍 Keyword Search (Typesense)
* 🔀 Hybrid Retrieval (Vector + Keyword)
* 🤖 Groq LLM Integration (LLaMA 3.1)
* 📌 Context-Aware Answer Generation
* 🔗 Source Citations
* 🧾 Answer Summarization
* 🕓 Query History Tracking
* ⚡ Streaming Responses

---

## 🏗️ Architecture Diagram

```id="arch1"
                 ┌────────────────────┐
                 │    User Query      │
                 └─────────┬──────────┘
                           │
           ┌───────────────┴───────────────┐
           │                               │
           ▼                               ▼
┌────────────────────┐        ┌────────────────────┐
│ Vector Search      │        │ Keyword Search     │
│ (FAISS)            │        │ (Typesense)        │
└─────────┬──────────┘        └─────────┬──────────┘
          │                             │
          └──────────────┬──────────────┘
                         ▼
              ┌────────────────────┐
              │  Result Fusion     │
              └─────────┬──────────┘
                        │
                        ▼
              ┌────────────────────┐
              │ Context Builder    │
              └─────────┬──────────┘
                        │
                        ▼
              ┌────────────────────┐
              │    LLM (Groq)      │
              │ LLaMA 3.1 Model    │
              └─────────┬──────────┘
                        │
                        ▼
   ┌────────────────────────────────────────────┐
   │ Answer + Citations + Summary              │
   └────────────────────────────────────────────┘
                        │
                        ▼
              ┌────────────────────┐
              │   History Store    │
              └────────────────────┘
```

---

## 🧠 How It Works

1. Documents (PDF/Text) are loaded
2. Split into chunks
3. Converted into embeddings
4. Stored in FAISS (vector DB)
5. Indexed in Typesense (keyword search)
6. User query is processed
7. Retrieval happens via:

   * Semantic search (FAISS)
   * Keyword search (Typesense)
8. Results are combined (Hybrid Retrieval)
9. Context sent to Groq LLM
10. LLM generates:

* Answer
* Citations
* Summary

---

## ⚙️ Tech Stack

* **LangChain**
* **FAISS (Vector Database)**
* **Typesense (Keyword Search Engine)**
* **Groq API (LLaMA 3.1)**
* **Sentence Transformers**
* **Python**

---

## 📁 Project Structure

```id="struct1"
Traditional_RAG/
│
├── data/
│   ├── pdf/
│   └── text_files/
│
├── notebook/
├── main.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env.example
```

---

## 🔐 Environment Setup

Create `.env` file:

```id="env1"
GROQ_API_KEY=your_groq_key
TYPESENSE_API_KEY=your_typesense_key
```

---

## 🚀 Installation

```bash id="inst1"
git clone https://github.com/Pratik3186/Traditional-RAG.git
cd Traditional-RAG

pip install -r requirements.txt
```

---

## ▶️ Usage

```bash id="run1"
python main.py
```

Example:

```id="example1"
Query: What is RAG?
```

---

## 🧾 Sample Output

```id="out1"
Answer:
RAG combines retrieval with generation...

Citations:
[1] research_paper.pdf (page 2)

Summary:
RAG improves LLM accuracy using external knowledge.
```

---

## 🔥 Why Hybrid RAG?

Traditional RAG uses only vector search.

👉 Hybrid RAG improves:

* ✅ Accuracy
* ✅ Relevance
* ✅ Recall

By combining:

* Semantic understanding (FAISS)
* Exact keyword matching (Typesense)

---

## 💡 Future Improvements

* 🔄 Re-ranking (Cross-Encoder)
* 📊 Evaluation (RAGAS)
* 🌐 Web UI (Streamlit / React)
* ☁️ Deployment

---

## 🏆 Resume Highlight

> Built a Hybrid RAG system using FAISS and Typesense with Groq LLM, enabling accurate and context-aware responses with citation tracking and summarization.

---

## 📬 Contact

**Pratik**
GitHub: https://github.com/Pratik3186

---

⭐ Star this repo if you found it useful!
