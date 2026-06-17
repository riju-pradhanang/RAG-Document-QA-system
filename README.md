# RAG

A small Retrieval-Augmented Generation (RAG) project scaffold using Python, LangChain, and local vector stores.

This repository includes sample text and PDF data loaders, a persisted ChromaDB vector store, and example notebooks for exploring RAG workflows.

## Contents

- `main.py` - Minimal project entrypoint.
- `pyproject.toml` - Project metadata and dependency declarations.
- `requirements.txt` - Installable runtime dependencies.
- `data/` - Project data files and vector store persistence.
  - `pdf/` - Stored PDF files.
  - `text_files/` - Plain text documents used for ingestion.
  - `vector_store/` - Persisted Chroma vector store data.
- `notebook/` - Jupyter notebooks demonstrating PDF loading and document workflows.

## Features

- Python 3.13+ compatibility
- LangChain integration
- Local embeddings with `sentence-transformers`
- Vector storage via `chromadb` and `faiss-cpu`
- PDF and text file ingestion with `pymupdf` / `pypdf`
- OpenAI support through `langchain-openai`
- Example notebooks for interactive exploration

## Requirements

- Python 3.13 or newer
- A virtual environment is recommended

## Installation

From the repository root:

```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

Or if you prefer `pyproject.toml`:

```bash
pip install .
```

## Usage

Currently the repository includes a simple Python entrypoint:

```bash
python main.py
```

This prints a greeting and is the starting point for extending the RAG pipeline.

## Working with the notebooks

Open the notebooks in `notebook/` to explore the pipeline interactively:

- `pdf_loader.ipynb` — example PDF ingestion and processing.
- `document.ipynb` — example document workflow for building a retrieval pipeline.

## Data layout

- `data/pdf/` — PDF source files for ingestion.
- `data/text_files/` — Sample plain text documents.
- `data/vector_store/` — Chroma persistence files for vector embeddings.

## Environment variables

If you use OpenAI or other external providers, create a `.env` file with keys such as:

```text
OPENAI_API_KEY=your_api_key_here
```

## Notes

This repo is currently scaffolded for RAG experiments and is ready to be extended with custom ingestion, embedding, retrieval, and generation code.

If you want to add a real RAG pipeline, start by implementing document loaders, embedding creation, vector storage setup, and query-answering logic in `main.py` or a new module.
