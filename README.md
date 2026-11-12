# NexoraAI — Intelligent Vector Database

NexoraAI is a C++17-based vector database demonstration featuring multiple similarity-search algorithms, a browser-based visualization interface, and an Ollama-powered document retrieval and question-answering pipeline.

The project explores how vector indexing, nearest-neighbor search, embeddings, and Retrieval-Augmented Generation (RAG) work together.

## Features

- **Multiple search algorithms:** HNSW, KD-Tree, and Brute Force.
- **Distance metrics:** Cosine Similarity, Euclidean Distance, and Manhattan Distance.
- **Interactive visualization:** 2D PCA projection of demo vectors.
- **Vector operations:** Insert, search, and delete vectors through the interface.
- **Algorithm benchmarking:** Compare search execution times.
- **Document processing:** Text chunking and document embeddings.
- **RAG pipeline:** Retrieve document chunks and generate answers using a local language model.
- **REST API:** HTTP endpoints for interacting with the vector database.

## Technology Stack

| Component | Technology |
|---|---|
| Programming language | C++17 |
| Frontend | HTML5, CSS3, JavaScript |
| Backend | C++ and cpp-httplib |
| Build system | CMake |
| Vector search | HNSW, KD-Tree, Brute Force |
| Embedding model | Ollama – nomic-embed-text |
| Language model | Ollama – llama3.2 |
| Visualization | HTML Canvas and PCA |

## Architecture

```text
             User
              |
              v
       Web Interface
       HTML / CSS / JS
              |
              v
          REST API
       C++ HTTP Server
              |
       +------+------+
       |             |
       v             v
  Vector Search   Document Pipeline
       |             |
   +---+---+         v
   |   |   |     Text Chunking
  HNSW KD  BF       |
                    v
              Ollama Embeddings
                    |
                    v
              Vector Retrieval
                    |
                    v
               RAG Pipeline
                    |
                    v
              Ollama LLM
```

## Getting Started

### Prerequisites

- Windows, Linux, or macOS
- C++17-compatible compiler
- CMake
- Git
- [Ollama](https://ollama.com/)

### Install AI models

Pull the models used by the project:

```bash
ollama pull nomic-embed-text
ollama pull llama3.2
```

Make sure Ollama is running before using the document and AI features.

### Clone the repository

```bash
git clone https://github.com/sohanroy1234/NexoraAI.git
cd NexoraAI
```

### Build

```bash
cmake -S . -B build
cmake --build build
```

### Run

On Windows:

```powershell
.\build\nexora.exe
```

Open the localhost URL printed by the application in your browser.

## Project Structure

```text
NexoraAI/
├── build/
├── .gitignore
├── CMakeLists.txt
├── README.md
├── httplib.h
├── index.html
└── main.cpp
```

## Learning Objectives

This project provides practical exposure to:

- Approximate Nearest Neighbor (ANN) search.
- Vector indexing and similarity measurement.
- HNSW graph-based search.
- KD-Tree spatial indexing.
- REST API development in C++.
- Text embeddings and document retrieval.
- Retrieval-Augmented Generation (RAG).
- Local AI model integration.

## Project Status

This is an evolving project. Further work can include algorithm improvements, stronger input validation, automated testing, improved retrieval quality, and more reliable document handling.

## Original Project Attribution

NexoraAI is based on and adapted from **Your-OWN-AI**, originally created by [perryvegehan](https://github.com/perryvegehan/Your-OWN-AI).

The inherited implementation and third-party components retain their applicable original licensing and attribution requirements. Changes and additional contributions should be documented as they are made.

## Author

**Sohan Roy**

GitHub: [@sohanroy1234](https://github.com/sohanroy1234)
