# RockyBot: News Research Tool 📈

RockyBot is an AI-powered News Research Tool designed to simplify information retrieval from news articles. Users can provide article URLs, and the system automatically processes the content, builds a searchable knowledge base, and answers questions using Retrieval-Augmented Generation (RAG).

The application is especially useful for analyzing stock market, finance, business, and technology news articles, enabling users to quickly extract insights without reading entire articles.
![Uploading Screenshot 2026-06-28 113157.png…]()

---

## Overview

Researching multiple news articles can be time-consuming. RockyBot solves this problem by automatically collecting article content, converting it into vector embeddings, and allowing users to ask natural language questions.

Instead of manually searching through lengthy articles, users can simply ask questions and receive concise answers along with the original source references.

---

## Features

* Load and process news articles directly from URLs
* Extract article content using LangChain's UnstructuredURLLoader
* Split large articles into manageable chunks
* Generate semantic embeddings using HuggingFace Embeddings
* Store embeddings efficiently using FAISS Vector Database
* Retrieve relevant article sections through similarity search
* Ask questions in natural language
* Generate contextual answers using Groq LLM
* Display source URLs for transparency and verification
* Fast and user-friendly Streamlit interface

---

## Technical Architecture

### Stage 1: Data Collection

Users provide one or more news article URLs.

The application fetches article content using:

* UnstructuredURLLoader

---

### Stage 2: Text Processing

The retrieved content is divided into smaller chunks using:

* RecursiveCharacterTextSplitter

This ensures efficient retrieval and better context management.

---

### Stage 3: Embedding Generation

Text chunks are converted into vector embeddings using:

* HuggingFace Embeddings
* Sentence Transformers

These embeddings capture the semantic meaning of the content.

---

### Stage 4: Vector Storage

Generated embeddings are stored inside:

* FAISS (Facebook AI Similarity Search)

FAISS enables lightning-fast similarity search across thousands of document chunks.

---

### Stage 5: Question Answering (RAG)

When a user asks a question:

1. Relevant chunks are retrieved from FAISS.
2. Retrieved context is sent to the Groq LLM.
3. The model generates an answer grounded in the retrieved content.
4. Source URLs are displayed alongside the answer.

This Retrieval-Augmented Generation (RAG) approach reduces hallucinations and improves answer accuracy.

---

## Tech Stack

* Python
* Streamlit
* LangChain
* Groq LLM
* HuggingFace Embeddings
* Sentence Transformers
* FAISS Vector Database
* UnstructuredURLLoader
* Retrieval-Augmented Generation (RAG)

---

## Project Workflow

1. Input article URLs.
2. Fetch article content.
3. Split content into chunks.
4. Generate vector embeddings.
5. Store embeddings in FAISS.
6. Retrieve relevant context for user queries.
7. Generate answers using Groq LLM.
8. Display answers with source references.

---

## User Interface

The Streamlit application allows users to:

* Enter news article URLs
* Process articles with a single click
* Ask questions about the articles
* Receive contextual answers
* View source URLs for verification

---

## Future Improvements

* Multi-document summarization
* Financial sentiment analysis
* News trend detection
* PDF and document upload support
* Chat history memory
* Source citation highlighting
* Support for multiple LLM providers

---

## Learning Outcomes

Through this project, I gained hands-on experience with:

* Retrieval-Augmented Generation (RAG)
* Vector Databases (FAISS)
* Embedding Models
* LangChain Framework
* Prompt Engineering
* Streamlit Deployment
* Large Language Models (LLMs)
* End-to-End AI Application Development

---

## Acknowledgements

Special thanks to **Codebasics** for the inspiration and learning resources that helped in understanding LangChain, RAG architecture, Vector Databases, and Generative AI application development.

A special thanks to **Dhaval Patel** and the entire Codebasics team for their excellent educational content and practical AI projects.

---

## Author

**Yadnesh Narkhede**

Data Analyst | Data Engineer | AI Engineer Enthusiast
