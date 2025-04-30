# AI-Powered News QA Agent with LangChain & Pinecone

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) pipeline using LangChain and Pinecone to answer questions about real-world news articles. The system retrieves semantically relevant documents from a Pinecone vector database and uses an OpenAI language model to generate answers grounded in those documents.

## Features

- Vector Database with Pinecone: Stores embeddings of news articles for fast semantic search.
- LangChain Agent: Dynamically queries the database and orchestrates LLM-driven reasoning.
- OpenAI Integration: Uses `gpt-3.5-turbo` or similar to synthesize answers from multiple articles.
- Metadata Filtering: Supports custom filtering (e.g., category = Politics) to refine retrieval.
- Google Colab Compatible: Designed to run in an interactive notebook environment.

## Tech Stack

- Python  
- LangChain  
- Pinecone  
- OpenAI API  
- Google Colab

## How It Works

1. Initialization: Load OpenAI and Pinecone credentials from environment variables.
2. Document Indexing: Pre-processed Guardian news articles are embedded and stored in Pinecone.
3. Agent Execution: An agent receives a user query, performs a vector similarity search across articles, and uses LLM reasoning to answer based on relevant documents.
4. Multi-Doc Context: The agent can synthesize responses using all retrieved articles, not just the last one.

## Example Use Case

> “What did recent articles say about Trump's role in Israeli politics?”

The agent retrieves multiple relevant articles with metadata like category and publication date, and synthesizes a coherent summary based on all available information.

## Files

- `AI_Agent_Pinecone.ipynb`: Main notebook implementing the agent pipeline and inference loop.

## Note

Make sure to configure the following:
- Your own `OPENAI_API_KEY`
- A valid Pinecone API key and environment
