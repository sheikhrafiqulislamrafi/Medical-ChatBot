# Medical Chatbot

## Description

The **Medical Chatbot** is a sophisticated Generative AI application designed to provide context-aware answers to medical queries. By utilizing **Retrieval-Augmented Generation (RAG)**, the system ensures that responses are not generated in a vacuum but are grounded in specific, curated medical literature.

The application leverages the **Llama 2** large language model and a high-performance vector database to retrieve relevant information from PDF-based knowledge bases, providing a reliable and responsive AI assistant through a modern web interface.

## Architecture & How It Works

The system follows the RAG workflow to minimize hallucinations and improve factual accuracy:

1.  **Data Ingestion:** Medical PDFs are processed and converted into structured text.
2.  **Chunking:** Text is split into smaller, overlapping segments to maintain context.
3.  **Embedding:** Text chunks are converted into high-dimensional vectors using Hugging Face models.
4.  **Vector Storage:** Embeddings are stored in Pinecone for efficient semantic retrieval.
5.  **Retrieval & Generation:** When a user asks a question, the system retrieves the most relevant chunks and passes them to Llama 2 to generate a grounded response.

## Key Features

- **PDF Data Processing:** Automated loading and recursive text splitting of medical documents.
- **Vector Search Integration:** Rapid semantic search powered by Pinecone and Hugging Face `sentence-transformers`.
- **AI-Powered Conversations:** Conversational memory and context-aware responses using the Llama-2-7b-chat model.
- **Real-Time Dashboard:** A responsive, dark-themed Flask web application featuring asynchronous messaging via jQuery.
- **Secure Configuration:** Implementation of environment variables for sensitive API and cloud service management.

## Technology Stack

| Category                 | Tool / Technology                                |
| :----------------------- | :----------------------------------------------- |
| **Programming Language** | Python                                           |
| **Web Framework**        | Flask                                            |
| **LLM Orchestration**    | LangChain                                        |
| **Large Language Model** | Llama-2-7b-chat (GGML version via CTransformers) |
| **Vector Database**      | Pinecone                                         |
| **Embeddings Model**     | Hugging Face (sentence-transformers)             |
| **Frontend**             | HTML5, CSS3, Bootstrap, jQuery                   |

## Project Roadmap

| Phase      | Task                           | Key Deliverables                                                            |
| :--------- | :----------------------------- | :-------------------------------------------------------------------------- |
| **Week 1** | Project Setup & Data Ingestion | Initialize structure (`template.py`), PDF loading, and recursive splitting. |
| **Week 2** | Vector Store & Embeddings      | Embedding generation and Pinecone cloud index synchronization.              |
| **Week 3** | LLM Integration & Backend      | CTransformers configuration and RetrievalQA chain implementation.           |
| **Week 4** | Frontend UI & Deployment       | Flask route development, UI styling, and end-to-end testing.                |

## References & Technical Documentation

This project is built upon industry-standard frameworks and research-backed methodologies:

- **Retrieval-Augmented Generation (RAG):** Grounding LLMs in external knowledge. [IBM Research on RAG](https://research.ibm.com/blog/retrieval-augmented-generation-RAG).
- **Llama 2:** Open Foundation and Fine-Tuned Chat Models. [Meta AI Llama 2 Documentation](https://ai.meta.com/llama/).
- **LangChain:** Framework for developing applications powered by language models. [LangChain Documentation](https://python.langchain.com/docs/get_started/introduction).
- **Pinecone:** Managed vector database for high-performance AI applications. [Pinecone Documentation](https://docs.pinecone.io/docs/overview).
- **Hugging Face:** Sentence Embeddings using Siamesse BERT-Networks. [Sentence-Transformers (SBERT) Documentation](https://www.sbert.net/).

# How to run?

### STEPS:

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n medibot python=3.11 -y
```

```bash
conda activate medibot
```

### STEP 02- install the requirements

```bash
pip install -r requirements.txt
```

### Create a `.env` file in the root directory and add your Pinecone & openai credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
GIMINI_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

```bash
# run the following command to store embeddings to pinecone
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,

```bash
open up localhost:
```
