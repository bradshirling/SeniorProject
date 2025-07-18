# RAG Senior Project
Overview
This project is a Retrieval-Augmented Generation (RAG) system designed for Tennessee State University (TSU) to assist students with questions regarding enrollment and admissions. The application features:

Frontend: 
A modern chatbot interface that allows users to interact with the system and ask questions about TSU's admissions process.
Backend: A Flask-based API that handles user queries, manages PDF documents, and leverages LangChain and Chroma for document retrieval and question answering.
Admin Portal: Allows administrators to upload, delete, and manage PDF documents that serve as the knowledge base for the chatbot.

Features:
Conversational chatbot interface for students.
Answers are generated using official university registration documents (PDFs).
Admin portal for managing the PDF knowledge base.
Automatic updating of the Chroma vector database when documents are added or removed.
Secure file upload and management.
Built-in support for document listing and retrieval.

Requirements:
The project relies on the following Python packages (see 
requirements.txt):

flask
flask-cors
langchain
langchain-community
langchain-chroma
langchain-text-splitters
pypdf
pytest

Setup Instructions:
Clone the repository
git clone <repo-url>
cd SeniorProject-main

Install dependencies:
pip install -r requirements.txt

Run the backend server:
cd Backend
python main.py
The server will start on http://127.0.0.1:5000/.

Open the frontend Frontend/index.html in your browser for the chatbot.
Open Frontend/admin.html for the admin portal (default password: 1234).

Usage:
Students: Ask questions about admissions, enrollment, deadlines, etc. via the chatbot. The system will answer using the uploaded PDFs.
Admins: Login to the admin portal to upload new PDFs, delete outdated ones, and update the Chroma database as needed.

Notes
Only PDF files are supported as knowledge sources.
After uploading or deleting PDFs, use "Update Database" in the admin portal to refresh the knowledge base.
The system uses a local instance of the Ollama LLM (mistral model) via LangChain.
