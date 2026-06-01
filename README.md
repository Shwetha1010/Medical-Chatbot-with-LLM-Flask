# HealBot: AI-Powered Medical Assistant using RAG, LangChain, Pinecone, and LLMs

## Overview

HealBot is an intelligent medical question-answering system built using Retrieval-Augmented Generation (RAG), LangChain, Pinecone Vector Database, and Groq's Llama 3.3 70B model.

The system retrieves relevant medical information from a document repository and generates context-aware responses grounded in trusted medical sources. By combining semantic search with large language models, HealBot reduces hallucinations and improves the reliability of generated responses.

This project demonstrates the practical implementation of modern Generative AI concepts including Retrieval-Augmented Generation, Vector Databases, Semantic Search, Prompt Engineering, and LLM-based Question Answering.

---

## Key Features

### Medical Knowledge Retrieval

* Extracts information from medical PDF documents
* Performs intelligent document chunking for efficient retrieval
* Preserves document context during processing

### Semantic Search

* Converts medical content into vector embeddings
* Stores embeddings in Pinecone Vector Database
* Retrieves relevant information using similarity search

### Context-Aware Question Answering

* Powered by Groq's Llama 3.3 70B model
* Generates grounded responses using retrieved context
* Reduces hallucinations through retrieval-based reasoning

### Web-Based Interface

* Built using Flask
* Supports real-time question-answer interaction
* Provides a simple and user-friendly experience

---

## System Architecture

```text
User Query
     │
     ▼
Flask Web Application
     │
     ▼
Embedding Generation
     │
     ▼
Pinecone Vector Database
     │
     ▼
Top Relevant Medical Chunks
     │
     ▼
Groq Llama 3.3 70B
     │
     ▼
Generated Response
     │
     ▼
User
```

---

## Technology Stack

### Generative AI

* LangChain
* Retrieval-Augmented Generation (RAG)
* Prompt Engineering

### Large Language Models

* Groq API
* Llama 3.3 70B

### Embeddings

* Sentence Transformers
* all-MiniLM-L6-v2

### Vector Database

* Pinecone

### Backend

* Python
* Flask

### Document Processing

* PyPDFLoader
* Recursive Character Text Splitter

### Deployment and DevOps

* Docker
* GitHub Actions

---

## How It Works

### Step 1: Document Ingestion

Medical PDF documents are loaded using PyPDFLoader.

### Step 2: Document Chunking

Documents are divided into smaller chunks using Recursive Character Text Splitter.

### Step 3: Embedding Generation

Each chunk is converted into vector embeddings using Sentence Transformers.

### Step 4: Vector Storage

Embeddings are stored in Pinecone Vector Database.

### Step 5: Query Processing

User queries are converted into embeddings and matched against stored vectors.

### Step 6: Context Retrieval

The most relevant document chunks are retrieved based on semantic similarity.

### Step 7: Response Generation

Retrieved context is passed to the LLM to generate a grounded and context-aware response.


---

## Installation

### Clone the Repository

```bash
git clone https://github.com/Shwetha1010/Medical-Chatbot-with-LLM-Flask.git
cd Medical-Chatbot-with-LLM-Flask
```

### Create Virtual Environment

```bash
python3.11 -m venv .venv
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Environment Variables

Create a `.env` file:

```env
PINECONE_API_KEY=your_pinecone_api_key
GROQ_API_KEY=your_groq_api_key
```

### Create Vector Index

```bash
python store_index.py
```

### Run Application

```bash
python app.py
```

Open:

```text
http://127.0.0.1:8080
```

---

