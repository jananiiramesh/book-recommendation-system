# 📚 Book Recommendation System

Welcome to the **Book Recommendation System**!  
This intelligent engine helps users discover books they'll love based on their interests by combining **vector similarity**, **OpenAI embeddings**, and **LLMs** for smarter recommendations.  

---

## 🚀 Features

- ✨ **Semantic Search**: Uses OpenAI embeddings to represent book descriptions as vectors and matches them with user queries.  
- 🔍 **Vector Database**: Efficient similarity search using [ChromaDB](https://www.trychroma.com/).  
- 🧠 **LLM-powered Category Mapping**: Maps complex or obscure book genres to familiar, broader categories for a better user experience.  
- 📊 **Clean & Preprocessed Data**: Utilizes the "7k Books" dataset from Kaggle with thorough data cleaning and validation.

---

## 🧰 Tech Stack

- 🧠 **OpenAI Embeddings** – for converting book descriptions and user queries into dense vector representations.
- 🧲 **ChromaDB** – a vector database for storing and retrieving book vectors.
- 🤖 **LLMs** – for intelligently grouping niche categories into familiar, user-friendly ones.
- 🧼 **Pandas & Python** – for data preprocessing and pipeline management.

---

## 🗃️ Dataset

- **Source**: [7k Books Dataset on Kaggle](https://www.kaggle.com/datasets)  
- **Preprocessing**:
  - Removed missing or null entries.
  - Ensured that missing values were not correlated with any specific factor to preserve recommendation integrity.
  - Standardized the data format for efficient processing and embedding.

---

## 🧠 How It Works

1. **Preprocessing**: Clean and normalize the Kaggle dataset to remove any inconsistencies or biases.
2. **Embedding Generation**: Use OpenAI’s `text-embedding-ada-002` to convert each book’s description into a numerical vector.
3. **Vector Storage**: Store all book vectors in ChromaDB for fast similarity searches.
4. **Query Matching**: When a user enters a search or interest query, it’s embedded and compared to the book vectors to find the most relevant matches.
5. **Category Simplification**: To avoid overwhelming users with niche categories, an LLM intelligently maps them into 2–3 intuitive umbrella genres like *Fiction*, *Non-Fiction*, and *Self-Help*.

---

## 💡 Example Use Case

> User enters: *"I want something motivational and based on true events."*  
🔍 The system:
- Converts this query into a vector.
- Searches for the closest matching book vectors.
- Filters and ranks results.
- Groups them into a familiar category (e.g., *Self-Help* or *Biography*) using LLM insights.  
✅ Final result: A list of books that are both motivational and based on true stories!

---
