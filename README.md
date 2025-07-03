# Zillow-Generative-AI-Dashboard

# 🏠 Zillow Generative AI Dashboard

This project combines Generative AI, data engineering, and interactive visualization to deliver natural-language insights into U.S. housing trends using Zillow's Home Value Index (ZHVI) data. It demonstrates a full-stack RAG (Retrieval-Augmented Generation) pipeline with integrated LLM prompts, a vector store, and a Streamlit chatbot, alongside a Tableau dashboard.

---

## 🚀 Features

- 🔍 **RAG Pipeline**: Built using HuggingFace embeddings + FAISS for fast vector search
- 🧠 **Prompt Engineering**: Designed and tested prompt templates to generate city-level housing summaries
- 📊 **Tableau Dashboard**: Visualized ZHVI trends, top/bottom cities, and geo-based growth using filters and KPI tiles
- 💬 **Streamlit Chatbot**: Natural-language interface that answers queries with LLM-generated insights
- 📁 **Zillow Dataset**: Used ZHVI ZIP/metro-level data spanning 2000–2025

---

## 📦 Tech Stack

| Layer              | Tools Used                                     |
|-------------------|-------------------------------------------------|
| Data Source        | Zillow Research Data (ZHVI CSV)                |
| Embeddings         | HuggingFace (`all-MiniLM-L6-v2`)               |
| Vector DB          | FAISS                                           |
| LLM                | Local model (`flan-t5-small`) or OpenAI (optional) |
| Backend            | Python, Pandas, NumPy, Scikit-learn            |
| Frontend           | Streamlit + Embedded Tableau Dashboard         |
| Visualization      | Tableau Public                                 |

---

## 🧠 How It Works

1. **Summarization**: Reshape Zillow data and generate region-wise text summaries (e.g., price trends from 2020–2025).
2. **Embedding + Indexing**: Convert summaries into vector embeddings and store them in a FAISS index.
3. **Prompt Generation**: Build prompts combining user queries + relevant context chunks.
4. **Answering**: Use an LLM to generate accurate and stylistic natural language responses.
5. **Interface**: Use Streamlit to accept queries and visualize results alongside Tableau.

---

## 📈 Sample Use Cases

- "Which cities in Texas had the fastest home price growth since 2020?"
- "Show me housing market trends for California metros."
- "What happened in New York housing prices post-COVID?"

---

## 🗂️ File Structure

├── zillow_summarizer.py # Summary generator for ZHVI regions
├── vector_store_setup.py # FAISS index builder
├── rag_local_answer.py # Local LLM-based RAG answering
├── streamlit_app.py # Chatbot UI + Tableau embed
├── reshaped_zillow.csv # Tableau-ready long-format dataset
├── zillow_summaries.txt # Text summaries for RAG
├── README.md

---

## 🧩 Future Enhancements

- Support for OpenAI / Azure / Claude APIs
- Prompt performance evaluation and scoring
- User-driven feedback loop for LLM fine-tuning
- Real-time Zillow data updates via APIs

---
