# Medical RAG Chatbot: Intelligent Healthcare Information Retrieval

> Empowering remote healthcare with advanced AI-driven information retrieval

## 🌟 Overview

This innovative project combines state-of-the-art Language Models (LLMs) with semantic chunking to create an intelligent medical chatbot. By leveraging Retrieval-Augmented Generation (RAG), we provide accurate, personalized medical information while minimizing AI hallucinations - a critical requirement in healthcare applications.

## 🚀 Key Features

- **CPU-Friendly Local Deployment**: Run the entire system locally without GPU requirements
- **Advanced Vector Storage**: Powered by Qdrant vector database
- **Smart Document Processing**: Implements semantic chunking for optimal information retrieval
- **Medical Domain Expertise**: Utilizes BioMistral-7B, a specialized medical LLM
- **Enhanced Word Understanding**: Integrates PubMed-BERT embeddings for medical terminology

## 🛠️ Technical Stack

- **Database**: Qdrant (Docker-based)
- **Language Model**: BioMistral-7B
- **Embeddings**: PubMed-BERT
- **API Framework**: FastAPI + Flask
- **Deployment**: Local CPU-based setup

## 📋 Setup Guide

### System Requirements

- Docker Desktop
- Python 3.x
- Internet connection for initial model download

### Quick Start

1. **Clone the Repository**
   ```bash
   git clone https://github.com/fenil210/Medical-RAG
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download Model**
   - Get BioMistral-7B.Q4_K_M.gguf from [Hugging Face](https://huggingface.co/MaziyarPanahi/BioMistral-7B-GGUF)
   - Place the model file in your project root directory

### Database Setup

```bash
# Pull Qdrant image
docker pull qdrant/qdrant

# Start Qdrant container
docker run -p 6333:6333 qdrant/qdrant
```

### Launch Application

1. **Test the Model**
   ```bash
   python retriever.py
   ```

2. **Start the Web Server**
   ```bash
   uvicorn rag:app
   ```
   Access the application at: http://127.0.0.1:8000

> ⚠️ Note: Response time averages 25-30 seconds due to CPU-based processing. Responses include source context and metadata.

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to your branch
5. Open a Pull Request

## 🙏 Acknowledgments

This project builds on the shoulders of giants:

- [Qdrant](https://qdrant.tech/) - Vector database excellence
- [Hugging Face](https://huggingface.co/) - Home of BioMistral-7B and PubMed-BERT
- [FastAPI](https://fastapi.tiangolo.com/) & [Flask](https://flask.palletsprojects.com/) - Web framework backbone
