# Retrieval Augmented Generation and RAG Agent

This application demonstrates the implementation of Retrieval Augmented Generation (RAG) and a RAG Agent using the LangChain and LangGraph libraries. The application loads documents from arXiv, creates a vector store using FAISS, and builds a retrieval-augmented generation chain. It also creates a RAG Agent that can perform a series of actions to answer questions based on the retrieved context.

## Features

- Loads documents from arXiv related to "Retrieval Augmented Generation"
- Splits the documents into chunks using RecursiveCharacterTextSplitter
- Creates a FAISS vector store from the chunked documents
- Builds a retrieval-augmented generation chain using the vector store and OpenAI's GPT-3.5-turbo model
- Implements a RAG Agent with a tool belt containing DuckDuckGoSearchRun and ArxivQueryRun
- Creates a workflow for the RAG Agent using LangGraph's StateGraph
- Integrates the retrieval-augmented generation chain into the RAG Agent's workflow
- Determines if a question is fully answered by the response using GPT-4
- Invokes the RAG Agent to answer questions based on the retrieved context

## Prerequisites

Before running the application, make sure you have the following:

- Python 3.7 or higher
- OpenAI API key (set as an environment variable named `OPENAI_API_KEY`)
- Required Python packages (listed in the `requirements.txt` file)

## Installation

1. Clone the repository:

```
git clone https://github.com/your-username/your-repository.git
```

2. Navigate to the project directory:

```
cd your-repository
```

3. Install the required packages:

```
pip install -r requirements.txt
```

4. Set your OpenAI API key as an environment variable:

```
export OPENAI_API_KEY=your-api-key
```

## Usage

To run the application, execute the following command:

```
python main.py
```

The application will load the documents, create the vector store, build the retrieval-augmented generation chain, and create the RAG Agent. It will then invoke the RAG chain and the RAG Agent with sample questions and print the responses.

## Code Structure

The code is organized into the following main components:

- `RetrievalAugmentedGeneration`: Handles loading documents, creating the vector store, and building the retrieval-augmented generation chain.
- `RAGAgent`: Implements the RAG Agent with a tool belt, creates the workflow using LangGraph's StateGraph, and integrates the retrieval-augmented generation chain into the workflow.
- `main`: The entry point of the application, where the components are instantiated, and sample questions are asked.

## Dependencies

The application relies on the following main dependencies:

- LangChain: A framework for developing applications with large language models.
- LangGraph: A library for building and executing workflows using state graphs.
- FAISS: A library for efficient similarity search and clustering of dense vectors.
- OpenAI: The OpenAI API for accessing language models like GPT-3.5-turbo and GPT-4.

## Acknowledgements

- The LangChain and LangGraph communities for providing powerful tools and resources.
- OpenAI for their advanced language models and APIs.
- The authors of the research papers and documents used in this application.
