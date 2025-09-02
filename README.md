 Constitution RAG System

A Retrieval-Augmented Generation system built to query a constitution document. This project demonstrates the core RAG pipeline: loading a document, chunking it, creating vector embeddings, and generating answers to questions based on the retrieved context.

## Features

- **Document Processing:** Loads and chunks a constitution from XML/text.
- **Vector Search:** Uses ChromaDB and sentence transformers for free, offline embedding.
- **Answer Generation:** Implements both zero-shot and one-shot prompting techniques using open-source LLMs (Google Flan-T5).
- **Flexible Prompting:** Easy-to-modify prompts for experimenting with different query styles.

## How It Works

1.  **Retrieval:** A user's question is converted into a vector. The system finds the most relevant chunks of the constitution based on semantic similarity.
2.  **Generation:** The retrieved chunks are passed to an LLM alongside the question and a instructions to generate a concise answer.

## Challenges & Learnings

- **Precision vs. Recall:** Tuning the system to retrieve the most directly relevant text (e.g., "France is a republic") versus related legal context is a key challenge.
- **Prompt Engineering:** The project explores how few-shot examples can guide the LLM to provide better-formatted answers.
- **Handling Scale:** Experimenting with chunking strategies to manage large context windows for open-source models.

## Future Improvements

- Implement a re-ranking step to improve retrieval precision.
- Experiment with larger open-source models (e.g., Llama 3).
- Add a simple web interface using Gradio or Streamlit.
