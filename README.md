<img width="1450" height="272" alt="image" src="https://github.com/user-attachments/assets/2c42ceda-d482-4782-ae1c-75f3e8b9f7c1" />

## Project Overview

This project implements a modern **Retrieval-Augmented Generation (RAG)** pipeline using **Large Language Models (LLMs)** to intelligently answer questions based on scientific PDF documents.  
Built with **LangChain**, **OpenAI**, and **ChromaDB**, it allows researchers to upload PDFs, extract relevant context using vector embeddings, and receive accurate, grounded responses from an LLM.

## Objectives

- Create an intelligent, context-aware assistant for exploring scientific PDFs  
- Combine the power of **OpenAI embeddings** with **LangChain’s retrieval framework**  
- Enable **semantic search** and **domain-specific Q&A** with natural language interfaces  
- Provide an interactive **Gradio** UI to streamline human-AI interaction

## Key Features

- Load and parse scientific PDFs using LangChain's `PyPDFLoader`  
- Split documents into manageable chunks with `RecursiveCharacterTextSplitter`  
- Generate dense vector embeddings via OpenAI's `text-embedding-3-large`  
- Store document vectors in a **ChromaDB** persistent vector store  
- Retrieve top-matching content for user queries using a LangChain retriever  
- Answer questions using **LangChain’s RetrievalQA Chain + ChatOpenAI**  
- Query results are traceable to relevant document chunks  
- Fully operational UI with Gradio for uploading PDFs and posing queries  

## Technologies Used

- Python 3.x  
- LangChain  
- OpenAI API (Embeddings + Chat Model)  
- ChromaDB  
- Gradio  
- PyPDF  
- tiktoken  

## Repository Structure

llm-rag-scientific-pdf-assistant/  
├── rag_assistant_scientific_papers_langchain.ipynb  
├── chroma_store/                      # Vector database storage  
├── .env                               # API keys and configuration  
├── README.md  

## Setup Instructions

### 1. Install Dependencies

Use the following to install required libraries:  
pip install langchain langchain_community langchain_openai chromadb pypdf gradio openai tiktoken

Also configure your OpenAI credentials:  
- OPENAI_API_KEY in a `.env` file or environment variables

### 2. Run Notebook

Open the Jupyter notebook `rag_assistant_scientific_papers_langchain.ipynb`  
Follow the cells step-by-step to load a PDF, index content, and interact via Gradio.

### 3. Use Gradio Interface

After executing the final Gradio cell:
- Upload a PDF (e.g., a scientific paper)
- Enter your query in natural language
- Receive a context-grounded answer from the LLM

## Use Cases

- Research paper summarization and Q&A  
- Document intelligence for enterprise data  
- Legal, medical, or technical PDF assistants  
- Semantic search and fact-grounded retrieval for GenAI applications  

## Requirements

- Python ≥ 3.8  
- OpenAI API access  
- Internet connection for embedding/LLM calls

## License

This project is licensed under the MIT License.
