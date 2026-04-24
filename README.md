
# 📧 AI-Powered Cold Email Generator

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/Powered%20by-LangChain-brightgreen)](https://python.langchain.com/)
[![Vector Database](https://img.shields.io/badge/Vector%20DB-ChromaDB-orange)](https://www.trychroma.com/)
[![LLM](https://img.shields.io/badge/LLM-Llama--3.1--70B-red)](https://groq.com/)

An automated B2B tool that scrapes job postings from career pages and generates personalized cold emails. It uses a vector database to dynamically match a company's past project portfolio to the specific skills required in the job description.

## 🚀 How it Works
1. **Web Scraping:** Uses `WebBaseLoader` to extract raw text from any career URL.
2. **LLM Extraction:** Converts unstructured text into a clean JSON format (Role, Skills, Experience) using **Llama-3.1-70B**.
3. **Vector Search:** Queries **ChromaDB** to find the most relevant portfolio links from a CSV based on the extracted tech stack.
4. **Email Generation:** Crafts a personalized email from the perspective of a BDE (Business Development Executive).

## 🛠️ Tech Stack
* **Framework:** LangChain
* **LLM:** Groq (Llama 3.1)
* **Database:** ChromaDB (Vector Store)
* **Data:** Pandas & Scikit-learn

## 📂 Repository Structure
```text
├── main.py              # Main Python script
├── my_portfolio.csv     # Portfolio database (Tech stacks & Links)
├── vectorstore/         # Persistent ChromaDB storage
└── requirements.txt     # Dependencies
