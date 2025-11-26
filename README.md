# Session 5 — Retrieval-Augmented Generation (RAG)

This repository contains the materials for **Session 5** of *Applied NLP*.  
- Slides: see [`slides/`](./slides/) folder  
- Notebooks: see [`notebooks/`](./notebooks/) folder 
---

## 📑 Session Outline

This session introduces **Retrieval-Augmented Generation (RAG)**, a technique that combines information retrieval with large language models to answer questions based on external documents.

### What you'll learn:

1. **Text Chunking** — Split long documents into overlapping chunks for efficient retrieval
2. **Embeddings** — Convert text chunks into semantic vector representations
3. **Vector Databases** — Store and search embeddings using FAISS
4. **Retrieval Chains** — Build a complete RAG pipeline connecting retrieval + generation
5. **Local LLM Integration** — Use Ollama for API-free local inference

### Dataset:

We use Lewis Carroll's two *Alice* books as our corpus like all previous sessions:
- *Alice's Adventures in Wonderland*
- *Through the Looking-Glass*

### Key Technologies:

- **LangChain** — Framework for building LLM applications
- **FAISS** — Facebook AI Similarity Search for vector storage
- **Sentence Transformers** — Embedding models (`all-mpnet-base-v2`)
- **Ollama** — Local LLM runtime (using `llama3.2` model)
- **LangSmith** — Prompt hub for retrieval templates


---
## 🚀 Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

> ⚠️ If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
> On Apple M1/M2 systems you may also need to install additional system packages (the “M1 shizzle”).

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You’re now ready to run the session notebooks!

Deactivate the environment when you’re done:
```bash
deactivate
```
