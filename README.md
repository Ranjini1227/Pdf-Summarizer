📑 PDFLens — AI Document Summarizer
An AI-powered document summarizer that extracts key insights, summaries, and keywords from any PDF, DOCX, or TXT file instantly.

🚀 Features
📖 Reading time estimation
📝 Word count analysis
📌 Key points extraction
📑 Section-wise summaries
🔑 Keyword identification
💡 Conclusions and takeaways
📁 Supports PDF, DOCX, and TXT files

🛠️ Tech Stack
Layer	Technology
Frontend	React, Create React App
Backend	Python, FastAPI
AI Model	Groq (LLaMA 3.3 70B)
Document Parsing	pdfplumber, python-docx
Package Manager	uv

📁 Project Structure
PDF Summarizer/
  ├── backend/
  │   ├── main.py
  │   └── pyproject.toml
  └── frontend/
      ├── src/
      │   └── App.js
      └── package.json

⚙️ Setup & Installation
Prerequisites
Python 3.10+
Node.js 18+
uv package manager
Groq API Key (free at https://console.groq.com)

Backend Setup
cd backend
uv add fastapi "uvicorn[standard]" groq pdfplumber python-docx python-multipart

# Windows PowerShell
$env:GROQ_API_KEY="your-groq-key-here"

uv run uvicorn main:app --reload --port 8001

Frontend Setup
cd frontend
npm install
$env:PORT=3001; npm start

Open in Browser
http://localhost:3001

🔑 Environment Variables
Variable	Description	Get it from
GROQ_API_KEY	Groq API Key	https://console.groq.com

📡 API Endpoints
Method	Endpoint	Description
GET	/	Root check
GET	/health	Server status
POST	/summarize	Summarize document

POST /summarize — Request
Field	Type	Description
document	file	PDF, DOCX, or TXT file

🖥️ How It Works
User uploads a document (PDF, DOCX, or TXT)
Backend extracts text from the document
Groq AI (LLaMA 3.3 70B) analyzes the content
Returns structured JSON with summary, key points, keywords
Frontend displays results in a beautiful dark orange dashboard

📝 Conclusion
PDFLens is a full-stack AI-powered document summarizer built with React (frontend), FastAPI (backend), and Groq's LLaMA 3.3 70B (AI model). It helps users quickly understand any document by providing an overview, key points, section summaries, keywords, and reading time estimation.

👩‍💻 Author
Made by Ranjini J
