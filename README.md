# Document Retrieval and Question Answering with OpenAI and Pinecone

## Overview
This project demonstrates a pipeline for retrieving answers to questions by utilizing OpenAI embeddings, Pinecone vector database, and LangChain. It performs the following steps:

1. **Document Loading**: Reads documents from a directory containing PDF files.
2. **Document Chunking**: Splits large documents into smaller chunks for efficient embedding and retrieval.
3. **Embedding Generation**: Generates embeddings using OpenAI or HuggingFace models as a fallback.
4. **Vector Search**: Uses Pinecone for similarity-based document retrieval.
5. **Answer Generation**: Uses OpenAI’s `text-davinci-003` model to generate answers from retrieved documents.

---

## Features
- Flexible document loading and chunking.
- Embedding generation with OpenAI and fallback to HuggingFace.
- Vector-based search with Pinecone.
- Answer generation using LangChain and OpenAI LLMs.

---

## Requirements
- Python 3.8+
- Virtual environment

### Libraries
All required libraries are listed in the `requirements.txt` file. Install them using:

```bash
pip install -r requirements.txt
```
---
## Setup

### Step 1: Clone the Repository
```bash
git clone <repository_url>
cd <repository_name>
```

### Step 2: Create and Activate a Virtual Environment

Windows
```bash
python -m venv venv
venv\Scripts\activate
```
MacOS/Linux
```bash
python3 -m venv venv
source venv/bin/activate
```
### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```
### Step 4: Set Up Environment Variables

Create a .env file in the root directory and add the following:
```bash
OPENAI_API_KEY=your_openai_api_key
PINECONE_API_KEY=your_pinecone_api_key
PINECONE_ENVIRONMENT=your_pinecone_environment
```
Replace your_openai_api_key and your_pinecone_api_key with your actual keys.
---
## Usage

### Step 1: Prepare the Documents

Place all PDF documents in the Document/ directory.

### Step 2: Run the Script

Execute All script:

### Step 3: Query the System

Modify the query in the script to retrieve answers:
```bash
our_query = "How much the agriculture target will be increased by how many crore?"
answer = retrieve_answers(our_query)
print(answer)
```
---
## Project Files

- main.py: The main script for loading documents, generating embeddings, and answering queries.

- requirements.txt: Contains all necessary dependencies.

- Document/: Directory containing the PDF documents.

- .env: File for storing API keys and environment variables.

- .gitignore: Prevents sensitive files like .env and unnecessary files from being tracked by Git.
---
## Libraries Used

- openai

- langchain

- pinecone

- sentence_transformers

- dotenv
---
## Notes

- Ensure your API keys are valid and have sufficient quota.

- For large datasets, consider optimizing chunk size and overlap for better performance.
---
## Acknowledgments

- [LangChain](https://api.python.langchain.com/en/latest/langchain_api_reference.html)

- [Pinecone](https://www.pinecone.io)

- [OpenAI](https://openai.com/)

