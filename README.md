# Medical Chatbot

## Description
The Medical Chatbot is an end-to-end generative AI application designed to provide helpful answers to medical queries based on specific document contexts. It utilizes Retrieval-Augmented Generation (RAG), combining the power of the Llama 2 large language model with a vector database to ensure responses are grounded in provided medical literature. With a responsive web-based chat interface, the app allows users to interact with an AI assistant that retrieves relevant information from a curated knowledge base of PDF documents.

## Features

### 1. PDF Data Extraction & Processing
- Automatically loads and extracts text from medical PDF documents in a directory
- Splits documents into manageable text chunks for efficient processing

### 2. Vector Search Integration
- Converts text chunks into high-dimensional embeddings using Hugging Face models
- Stores and retrieves information from the Pinecone vector database for rapid semantic search

### 3. AI-Powered Chat Interface
- Uses the Llama-2-7b-chat model to generate conversational and context-aware responses
- Includes a specialized prompt template to ensure the bot remains helpful and avoids making up answers

### 4. Real-Time Web Dashboard
- A Flask-based web application providing a modern, dark-themed chat window
- Features asynchronous message handling using jQuery for a smooth user experience

### 5. Secure Environment Management
- Uses environment variables to securely handle sensitive API keys for cloud services

## Tech Stack

| Category | Tool/Technology |
|----------|-----------------|
| Programming Language | Python |
| Web Framework | Flask |
| LLM Orchestration | LangChain |
| Large Language Model | Llama-2-7b-chat (GGML version) |
| Vector Database | Pinecone |
| Embeddings Model | Hugging Face (sentence-transformers) |
| Frontend | HTML5, CSS3, Bootstrap, jQuery |

## Project Timeline

| Duration | Task | Key Deliverables & Source Reference |
|----------|------|--------------------------------------|
| Week 1 | Project Setup & Data Ingestion | Initialize project structure using template.py. Implement PDF loading and recursive text splitting. |
| Week 2 | Vector Store & Embeddings | Generate embeddings using Hugging Face models. Initialize Pinecone and push text chunks to the cloud index. |
| Week 3 | LLM Integration & Backend | Configure Llama 2 with CTransformers and set up the RetrievalQA chain. Design the prompt template for medical accuracy. |
| Week 4 | Frontend UI & Deployment | Develop the Flask routes and the chat interface. Apply final styling and conduct end-to-end testing. |

## Expected Outcome
By the end of the project, a fully functional Medical Chatbot will be operational. It will allow users to input natural language questions through a web browser and receive medically relevant answers derived from a private document library. The system will demonstrate a complete AI pipeline: from raw data extraction and vector indexing to real-time inference using a quantized Llama 2 model, ensuring an efficient and intelligent user experience.

## Installation & Setup
The installation and setup process will be revealed soon.
