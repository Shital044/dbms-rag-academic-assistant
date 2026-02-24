# Academic RAG Study Assistant

A Retrieval-Augmented Generation (RAG) system designed to process academic DBMS PDF documents and provide structured answers using local Large Language Models (LLMs) with Ollama.

---

## Project Overview

This project demonstrates:

- Retrieval-Augmented Generation (RAG)
- Local LLM usage (Ollama)
- Vector database (ChromaDB)
- Chunking strategy comparison
- Retrieval comparison (Top-K vs MMR)
- Structured academic answer generation

The system works completely offline.

---

## Setup Instructions

### 1. Install Python
Make sure Python 3.11 is installed.

---

### 2. Install Dependencies

Run:

pip install -r requirements.txt

---

### 3. Install Ollama

Download Ollama from:
https://ollama.com

Then pull the model:

ollama pull tinyllama

---

### 4. Prepare Data

Create a folder named:

data/

Place your DBMS PDF files inside this folder.

---

### 5. Run the Project

Open:

main.ipynb

Run all cells to:
- Load documents
- Create embeddings
- Build vector database
- Start querying

---

## Folder Structure

```
Academic-RAG-Assistant/
├── main.ipynb
├── data/
├── chroma_db/
├── results.md
├── README.md
└── requirements.txt
```
---

## Technical Workflow

1. Data Loading – Extract text from PDFs using pypdf.
2. Text Chunking – Fixed-size and Sentence-based chunking.
3. Embeddings – sentence-transformers/all-MiniLM-L6-v2.
4. Vector Store – ChromaDB for storage and retrieval.
5. Generation – TinyLlama via Ollama for answer generation.

---

## Experimental Findings

The project compares:

- Fixed-size chunking
- Sentence-based chunking
- Top-K retrieval
- MMR retrieval

Results show:

- Sentence-based chunking improves conceptual clarity.
- MMR provides better retrieval diversity.
- Structured prompting improves answer quality.

---

## Expected Output

When a DBMS question is asked, the system:

- Retrieves relevant context
- Generates structured answer
- Uses only provided documents
- Avoids hallucination

Example:

Question: What is normalization?

Answer:
Normalization is the process of organizing relational database tables to reduce redundancy and improve data integrity.

---

## Author
Shital Phadake


