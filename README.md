# 📄 Local RAG Assistant for Videos & Documents

A fully local RAG (Retrieval-Augmented Generation) assistant that enables intelligent conversations with your documents and YouTube videos. Everything runs locally - no APIs, no cloud, complete privacy.

## 🎥 Demo Video (53 seconds)

```

**Quick Demo Overview:**
- 📤 Document upload and processing (PDF, DOCX, EXCEL, TXT)
- 🎬 YouTube video transcription with Whisper
- 💬 Real-time intelligent Q&A
- ⚡ Fast semantic search with FAISS
- 🎯 Advanced reranking for optimal results

---

## ✨ Features

### 📍 Document Processing
- Upload and process multiple file formats: **PDF, DOCX, EXCEL, TXT**
- Intelligent text chunking to maintain context
- Efficient document parsing and preprocessing

### 📍 Video Transcription
- YouTube video integration via URL
- Local transcription using **Whisper AI**
- Accurate speech-to-text conversion without external APIs

### 📍 Semantic Search with Reranking
- **FAISS** vector database for fast similarity search
- **all-MiniLM-L6-v2** embeddings for semantic understanding
- **Reranking** for improved result accuracy and relevance
- Two-stage retrieval: initial search + intelligent reranking
- Instant retrieval of most relevant content chunks

### 📍 RAG Pipeline with Reranking
- **LangChain** framework orchestrating the entire workflow
- **Two-stage retrieval**: FAISS initial search + intelligent reranking
- Context-aware response generation
- Grounded answers based on retrieved and reranked information
- Improved accuracy through relevance scoring

### 📍 Local LLM
- Powered by **Ollama** for complete privacy
- Offline question answering capabilities
- No data leaves your machine

### 📍 Web Interface
- Clean, responsive UI built with **Bootstrap 5**
- Real-time chat interface
- File upload and management system
- Built with HTML, CSS, and JavaScript

---

## 🏗️ Architecture

```
┌─────────────────┐
│   Web Interface │ (Flask + Bootstrap 5)
└────────┬────────┘
         │
┌────────▼────────┐
│  Flask Backend  │
└────────┬────────┘
         │
    ┌────┴────┐
    │         │
┌───▼──┐  ┌──▼────┐
│Whisper│  │Document│
│ (YT)  │  │Parser │
└───┬───┘  └──┬────┘
    │         │
    └────┬────┘
         │
    ┌────▼────┐
    │ Chunking│
    └────┬────┘
         │
    ┌────▼────────┐
    │  Embeddings │ (all-MiniLM-L6-v2)
    └────┬────────┘
         │
    ┌────▼────┐
    │  FAISS  │ (Initial Search)
    └────┬────┘
         │
    ┌────▼─────────┐
    │  Reranker    │ (Relevance Scoring)
    └────┬─────────┘
         │
    ┌────▼─────────┐
    │  LangChain   │
    │  RAG Chain   │
    └────┬─────────┘
         │
    ┌────▼────┐
    │ Ollama  │ (Local LLM)
    └─────────┘
```

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|-----------|
| **Backend** | Flask |
| **LLM** | Ollama (Local) |
| **Transcription** | Whisper AI |
| **Embeddings** | all-MiniLM-L6-v2 |
| **Vector Store** | FAISS |
| **Reranking** | Cross-encoder model |
| **Framework** | LangChain |
| **Frontend** | HTML, CSS, JavaScript, Bootstrap 5 |
| **Document Processing** | PyPDF2, python-docx, openpyxl |

---

## 📋 Prerequisites

- Python 3.8+
- Ollama installed locally
- FFmpeg (for Whisper)
- 8GB+ RAM recommended

---

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/nourhanwael7/local-RAG-Assistant-for-Videos-Documents.git
cd local-RAG-Assistant-for-Videos-Documents

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install Ollama and pull a model
ollama pull llama2  # or your preferred model
```

---

## 💻 Usage

```bash
# Start the Flask application
python app.py

# Open browser and navigate to
http://localhost:5000
```

### Using the Assistant

1. **📤 Upload Documents**: Click "Upload" and select your PDF, DOCX, EXCEL, or TXT files
2. **🎬 Add YouTube Videos**: Paste a YouTube URL to transcribe and add to knowledge base
3. **💬 Ask Questions**: Type your question in the chat interface
4. **✨ Get Answers**: Receive contextual answers based on your uploaded content

---

## 🎯 Use Cases

- 📚 Research paper analysis
- 📊 Business document Q&A
- 🎓 Educational content exploration
- 📹 Video content summarization
- 📝 Meeting transcript analysis
- 🔍 Knowledge base search

---

## 🔒 Privacy & Security

- ✅ **100% local processing**
- ✅ **No data sent to external servers**
- ✅ **No API keys required**
- ✅ **Complete offline functionality**
- ✅ **Your data stays on your machine**

---

## 📊 Performance

- ⚡ Fast semantic search with FAISS
- 🎯 Advanced reranking for higher accuracy
- 🧩 Efficient chunking for optimal context
- 🤖 Local LLM inference
- 🎨 Responsive web interface

### Why Reranking?

Traditional RAG systems retrieve documents based solely on semantic similarity. This project implements **reranking** as a second stage:

1. **Initial Retrieval**: FAISS quickly finds candidate documents
2. **Reranking**: A specialized model re-scores results for better relevance
3. **Result**: More accurate answers with improved context selection

This two-stage approach significantly improves answer quality while maintaining fast response times.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 🙏 Acknowledgments

- OpenAI Whisper for transcription
- Sentence Transformers for embeddings
- Facebook AI for FAISS
- LangChain community
- Ollama team

---

## 📧 Contact

For questions or feedback, please open an issue on GitHub.

---

## ⚠️ Note

**This is a demonstration project. The actual source code is not publicly available due to confidentiality agreements (NDA).**

---

