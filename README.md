# 🧠 RAG Question-Answering Demo

This is a **Retrieval-Augmented Generation (RAG)** demo built with **Streamlit**, **LangChain**, and **OpenAI GPT-4**.  
It allows users to upload documents or input a website URL, then ask natural language questions about the content.  
The system retrieves the most relevant text chunks from the source and uses GPT-4 to generate context-aware answers.

---

## 🚀 Features

- 📄 Upload `.txt` or `.pdf` files to extract their content  
- 🌐 Load and process content directly from a website URL  
- 🧩 Split large documents into smaller overlapping chunks for better retrieval  
- ⚙️ Generate embeddings using Hugging Face’s `all-MiniLM-L6-v2` model  
- 🧠 Use GPT-4 via LangChain to answer user questions  
- 💬 View retrieved document context for transparency  
- 🔒 Secure API key management via Streamlit Secrets (no `.env` file needed on deployment)

---

## 🧰 Tech Stack

- **Frontend/UI:** [Streamlit](https://streamlit.io)  
- **Language Model:** OpenAI GPT-4 via [LangChain](https://python.langchain.com)  
- **Embeddings:** Hugging Face Sentence Transformers  
- **Vector Storage:** In-memory FAISS (via LangChain)  
- **Environment Variables:** `python-dotenv` (local) / Streamlit Secrets (cloud)

---

## 🏗️ How It Works

1. **Document Loading**  
   - Load content from a website or file upload.  
   - Convert PDFs and text into a list of documents.  

2. **Text Splitting**  
   - Split large text into smaller overlapping chunks (≈1000 characters each).  

3. **Vector Embedding**  
   - Convert chunks into dense vector representations using Hugging Face embeddings.  

4. **Vector Storage & Retrieval**  
   - Store embeddings in memory.  
   - When a user asks a question, retrieve the most relevant chunks.  

5. **Answer Generation**  
   - Send both the question and retrieved chunks to GPT-4 through LangChain.  
   - Display the model’s answer and show the supporting document snippets.

---

## 🧑‍💻 Running Locally

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
