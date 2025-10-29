# Retrieval-Augmented Generation (RAG) Web Information Extractor
Overview

This project demonstrates how to implement a Retrieval-Augmented Generation (RAG) pipeline using LangChain, FAISS, HuggingFace embeddings, and Microsoft Phi-3.
It retrieves, processes, and summarizes information directly from multiple websites.
While the demo uses public web pages about the DC Comics universe as an example dataset, the architecture can be easily adapted for business use cases — such as:

collecting and summarizing product information from e-commerce sites,

extracting insights from marketing or R&D reports,

creating internal knowledge retrieval tools.

🔧 Technologies Used

Python

LangChain

FAISS (vector database for semantic search)

HuggingFace sentence-transformers

Microsoft Phi-3-mini model via llama-cpp-python

WebBaseLoader for dynamic website content extraction

⚙️ How It Works

Loads and cleans text from multiple websites using WebBaseLoader.

Splits text into manageable chunks with RecursiveCharacterTextSplitter.

Generates embeddings using sentence-transformers/all-MiniLM-L6-v2.

Indexes data into a FAISS vector store for semantic retrieval.

Queries are answered through an integrated Phi-3 LLM, combining retrieval and generation for accurate responses.

💡 Example Use Case

You can adapt this project to:

Build a product knowledge assistant that retrieves product specs and reviews.

Summarize company documents or research papers.

Develop a chatbot that answers questions about your organization’s data.

🧠 Sample Query
user_question = "Who invented Batman?"


Response (example):

Batman, a character in the DC Comics universe, was created by artist Bob Kane and writer Bill Finger. His first appearance is in Detective Comics #27 published on March 30, 1939.

📂 Dataset Note

The current dataset (DC Comics articles) was used to demonstrate functionality.
The same pipeline can be applied to any website.

