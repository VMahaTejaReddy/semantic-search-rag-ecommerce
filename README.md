# 🔎 Semantic Search & RAG Pipeline for E-Commerce Reviews

## 🚀 Overview
This project implements an end-to-end Semantic Search and Retrieval-Augmented Generation (RAG) system on Flipkart product reviews.

Unlike traditional keyword search, this system retrieves results based on meaning using dense vector embeddings and FAISS similarity search.

---

## 🏗 System Architecture

User Query  
↓  
Sentence Embedding (SBERT – all-MiniLM-L6-v2)  
↓  
Vector Similarity Search (FAISS – IndexFlatIP)  
↓  
Top-K Relevant Reviews  
↓  
Context Construction + Threshold Filtering  
↓  
Local LLM (FLAN-T5)  
↓  
Grounded Answer Generation  

---

## 📊 Exploratory Data Analysis

### Rating Distribution
![Rating Distribution](images/rating_distribution.png)

### Word Cloud
![Word Cloud](images/wordcloud.png)

---

## 🧠 PCA Visualization of Embeddings

![PCA Plot](images/pca_plot.png)

The PCA projection shows meaningful clustering of reviews in embedding space, validating semantic grouping.

---

## 📈 Evaluation

- Precision@5 = 1.00 for sentiment-aligned queries
- Similarity threshold = 0.65
- Thresholding prevents hallucination for out-of-domain queries

---

## 🧩 Key Technologies

- Sentence-Transformers (all-MiniLM-L6-v2)
- FAISS (IndexFlatIP)
- PCA (Scikit-learn)
- Transformers (FLAN-T5)
- Python, Pandas, Matplotlib

---

## 🎯 Business Impact

This system improves:
- Intent-based product discovery
- Context-aware customer support
- Search relevance beyond keyword matching

