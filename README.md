# 💬 Loan Approval Q&A Chatbot using RAG and Gemini 1.5 Flash

This repository contains a Q&A chatbot built using a RAG (Retrieval-Augmented Generation) approach on a real-world loan approval dataset. It combines document retrieval (via FAISS) with generative responses powered by Google's Gemini 1.5 Flash model. The chatbot is capable of answering user questions based on contextual data from the dataset.

## ⚙️ Technologies Used

- **Google Colab** – for development and running the chatbot
- **Gemini 1.5 Flash** – to generate intelligent responses
- **FAISS** – for efficient vector-based document retrieval
- **SentenceTransformers** – to convert text into embeddings
- **Pandas** – for handling tabular data
- **Gradio** (optional) – to build a simple chatbot UI

## 📂 Dataset

We used the publicly available [Loan Approval Prediction dataset on Kaggle](https://www.kaggle.com/datasets/sonalisingh1411/loan-approval-prediction), which contains information about applicants, their financial status, and loan approval decisions.

## 🧠 Project Flow

1. The CSV file is loaded and each row is turned into a text document.
2. SentenceTransformers generate vector embeddings for these documents.
3. A FAISS index helps retrieve relevant rows for any user question.
4. Gemini 1.5 Flash takes the user query + retrieved context and generates a helpful, natural language answer.

## 💡 Example Question

```text
Q: How does credit history affect loan approval?
