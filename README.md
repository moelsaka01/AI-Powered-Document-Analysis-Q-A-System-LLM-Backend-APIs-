# AI-Powered-Document-Analysis-Q-A-System-LLM-Backend-APIs-

# AI-Powered Document Analysis and Q&A System

This project is a small but complete backend for an AI document Q and A system.

You can:

- Upload text documents through a REST API
- Automatically split them into chunks and store them in a SQLite database
- Generate embeddings for each chunk using OpenAI
- Ask natural language questions against the ingested documents
- Get answers that are grounded in the stored context, with the source chunks returned

The project uses FastAPI, SQLAlchemy, and OpenAI models. It is designed as a clean reference for building LLM powered backends with retrieval augmented generation.

## Features

- FastAPI based REST API
- Upload and index plain text documents
- Simple chunking and embedding pipeline
- Vector similarity search using cosine similarity
- Retrieval augmented question answering
- SQLite persistence through SQLAlchemy
- Basic test suite for the health endpoint

## Project structure

```text
app/
  core/          - configuration
  db/            - database models and session
  schemas/       - Pydantic models for requests and responses
  services/      - document ingestion, embeddings, retrieval, Q and A
  api/routes/    - FastAPI route definitions
  main.py        - application entrypoint
tests/
  test_healthcheck.py
