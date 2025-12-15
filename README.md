# 🌾 Agentic RAG System for Agricultural Advisory

This repository contains the implementation of a **Domain-Specific Agentic Retrieval-Augmented Generation (Agentic RAG) system** designed to provide **accurate, safe, and trustworthy agricultural advisory responses**.  
The system combines **semantic retrieval, reranking, and multi-agent reasoning** to reduce hallucinations and improve factual grounding.

---

## 📌 Project Overview

Traditional digital advisory systems and basic chatbots often provide generic or unreliable answers, which is risky in agriculture.  
This project addresses those challenges by building an **Agentic RAG framework** that:

- Grounds answers in verified agricultural manuals
- Uses multiple agents for reasoning, grading, and verification
- Reduces hallucinations and improves evidence relevance
- Scales efficiently on consumer-grade hardware

---

## 🧠 Key Features

- **Agentic RAG Architecture**
  - Query Reformulation Agent  
  - Retrieval Agent  
  - Source Selection Agent  
  - Grader  
  - Verifier  
  - LLM-based Answer Generator  

- **Semantic Retrieval**
  - FAISS vector indexing
  - BAAI/bge-m3 embeddings

- **Reranking**
  - FlashRank-based reranker for improved relevance

- **Evaluation**
  - BLEU
  - ROUGE-L
  - Cosine Similarity
  - BERTScore (F1)

---

## 📂 Data Sources

- **TNAU Agricultural Manuals** (PDFs)
- **KisanVaani Dataset** (Farmer queries)

These datasets are used to build a **domain-specific knowledge base** for agricultural advisory.

---

## 🛠️ Tech Stack

- **Language**: Python  
- **LLM**: Llama-3.1-8B  
- **Embeddings**: BAAI/bge-m3, all-MiniLM-L6-v2  
- **Vector Store**: FAISS  
- **Reranker**: FlashRank  
- **Frameworks**: LangChain, LangGraph  
- **Hardware**: Tested on NVIDIA T4 GPU  

---

## ⚙️ Methodology Pipeline

1. Data Collection (PDFs + datasets)
2. Text Preprocessing
3. Sentence-based Chunking
4. Embedding Generation
5. FAISS Indexing
6. Query Expansion
7. Retrieval + Reranking
8. Agentic Reasoning Loop
9. Answer Generation
10. Verification

Each stage improves the accuracy and reliability of the final response.

---

## 📊 Key Results

- **Best Configuration**:  
  **Llama-3.1-8B + BAAI/bge-m3 + Reranker**
- Achieved highest scores across:
  - BLEU
  - ROUGE-L
  - Cosine Similarity
  - BERTScore
- Demonstrated reduced hallucination and improved factual grounding

---

## 📁 Repository Structure

```text
├── Agri_bot_Llama_3_1_8B_Instruct.ipynb
├── data/
│   └── pdfs
├── evaluation_English.csv
├── Dataset.docx
├── README.md

▶️ How to Run

Clone the repository:

git clone https://github.com/SaiSuriya29/Agentic_RAG_For_Agri_Domain.git
cd Agentic_RAG_For_Agri_Domain

Run the notebook:

jupyter notebook or Google Colab

🔬 Evaluation Strategy

The system was evaluated using a progressive setup:

Baseline (No RAG)

FAISS Retrieval Only

Retrieval + Reranking

Embedding Comparison

Full Agentic RAG Pipeline

👨‍🌾 Expert Validation

System-generated responses were reviewed by an agricultural domain expert.
The expert confirmed that the outputs were:

Factually accurate

Context-aware

Aligned with real-world agricultural practices

🚀 Future Work

Expand region-specific and multilingual agricultural datasets

Fine-tune models using supervised data or expert feedback (RLAIF)

Enhance grader to balance safety and recall

Integrate image-based disease diagnosis using vision transformers

Deploy in real-world advisory systems with human-in-the-loop oversight

📚 References

All the links are providede in the Dataset.docx document

🙏 Acknowledgements

Tamil Nadu Agricultural University (TNAU)

KisanVaani Dataset

Open-source NLP and RAG research community

👤 Author

Sai Kiran Thamminaina
MSc Data Science | NLP & Generative AI

