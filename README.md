# -kaameshwar-rai-wasserstoff-AiInternTask
Welcome to my project submission for the Wasserstoff Generative AI Internship.
The objective was to build a chatbot that can analyze uploaded documents, understand natural language questions, and return contextual answers with citations — all without needing expensive APIs.

Problem Statement-
We were challenged to create an AI-powered document research assistant capable of:

Accepting 75+ PDFs or scanned images

Performing OCR if needed

Extracting text and storing it in a database

Answering user queries with precise citations

Identifying common themes across documents-
 My Approach (Fully Local + Free)
To keep the solution efficient and API-free, I used open-source models and offline embeddings.
Step-by-Step Workflow
Uploaded my resume PDF (Resume_Kaameshwar_pdf.pdf)

Extracted text from the document using PyMuPDF (fitz)

Cleaned and split the text into 400-character overlapping chunks

Generated vector embeddings using HuggingFace’s all-MiniLM-L6-v2 (fully offline)

Stored embeddings in ChromaDB for fast semantic search

Built a retriever that pulls the top relevant chunks for any user query

Used a local QA model (deepset/roberta-base-squad2) to answer the question based on retrieved context

Returned answers with confidence scores and cited chunk IDs

Technologies Used
Python 3.x

Jupyter Notebook

PyMuPDF (fitz) for PDF text extraction

sentence-transformers for local embeddings

ChromaDB as the vector store

HuggingFace Transformers for Q&A

LangChain (used only for document/embedding interface)

This project was an exciting challenge and a great opportunity to apply real-world GenAI workflows in a constrained, local-first setup.
Hope you find it interesting and helpful!
