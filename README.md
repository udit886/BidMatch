Request For Proposal (RFP) Analyzer 📄🤖
An AI-powered document analysis tool built with Streamlit, LangChain, and Google Gemini Pro. This application allows users to upload multiple vendor proposal PDFs, parse and index their contents, and query the system to evaluate and extract the best proposals based on specific criteria like pricing, delivery dates, and special conditions.

🚀 Features
Multi-PDF Processing: Upload and parse multiple vendor proposals simultaneously.

Intelligent Text Chunking: Dynamically splits large PDF payloads using RecursiveCharacterTextSplitter for accurate context matching.

Vector Search Local Storage: Uses Chroma DB to create local vector embeddings via GoogleGenerativeAIEmbeddings.

Context-Aware Analysis: Leverages a customized Gemini Pro prompt optimized specifically for comparative RFP evaluation (comparing product offerings, delivery timelines, pricing, location data, and online bidding compliance).

🛠️ Tech Stack
Frontend: Streamlit

LLM & Embeddings: Google Generative AI (gemini-pro, embedding-001)

Orchestration: LangChain

Vector Database: Chroma DB

PDF Parsing: PyPDF2

📋 Prerequisites
Before setting up the project, ensure you have:

Python 3.9 or higher installed.

A Google AI Studio API Key (Get one from Google AI Studio).

💻 Installation & Setup
1. Clone the Repository
Bash
git clone https://github.com/your-username/rfp-analyzer.git
cd rfp-analyzer
2. Create a Virtual Environment
Bash
# Windows
python -m venv venv
venv\Scripts\activate

📖 Usage Guide
Enter Your Query: Type your specific evaluation criteria into the main text input field (e.g., "Which company offers the best price for 500 units with a delivery date before next month?").

Upload Documents: Use the sidebar to upload your target vendor proposal PDFs.

Process & Analyze: Click the Submit & Process button. The application will extract text, generate vector embeddings, run a similarity search against your question, and output a structured breakdown ranking the best proposals.

📁 Project Structure
Plaintext
├── app.py               # Main Streamlit application source code
├── .env                 # Environment variables (API Keys)
├── chroma_index/        # Directory where Chroma DB persists vector embeddings
└── README.md            # Project documentation
