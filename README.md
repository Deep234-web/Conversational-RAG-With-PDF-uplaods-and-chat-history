# Conversational RAG with PDF Uploads and Chat History

This project demonstrates a Conversational Retrieval-Augmented Generation (RAG) system built using Streamlit, where users can upload PDF documents and engage in a Q&A session with the content. The system utilizes historical chat context to enhance the quality of questions and answers, making the conversation history-aware.

## Features
- **PDF Uploads**: Upload multiple PDF files, and the content will be processed for question answering.
- **Chat History Awareness**: The system uses chat history to contextualize questions, reformulating them for better understanding.
- **Retrieval-Augmented Generation (RAG)**: Integrates retrieval of document chunks via FAISS and combines it with a language model to provide concise and accurate answers.
- **Custom Language Model**: The project leverages the Groq `Gemma2-9b-It` model for question answering.
- **Embeddings**: Uses HuggingFace embeddings (`all-MiniLM-L6-v2`) for document chunking and vector storage.
- **Session State Management**: Each session maintains its own chat history.

Live Demo(https://conversational-rag-with-pdf-uplaods-and-chat-history-t8efqtjxd.streamlit.app/)

## Requirements
- Python 3.8+
- The following Python packages:
  - streamlit
  - langchain
  - FAISS
  - HuggingFace Transformers
  - PyPDFLoader
  - dotenv

## Installation
1. Clone the repository.
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
3. Set up the environment variables:
    Create a .env file with the following keys:
    HF_TOKEN: Hugging Face token for the embeddings
    GROQ_API_KEY: API key for Groq language model
4. Run the streamlit app
   ```bash
   streamlit run app.py

## Usage
- Enter your Groq API key when prompted.
- Upload one or more PDF files.
- Enter a session ID to track your conversation history.
- Ask questions related to the content of the uploaded PDFs. The system will retrieve relevant information and respond using the context.

