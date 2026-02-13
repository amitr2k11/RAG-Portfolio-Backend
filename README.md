🚀 AI-Powered Portfolio Chatbot (RAG Backend)

Retrieval-Augmented Generation (RAG) Backend using FastAPI + LangChain + FAISS + Ollama

🌐 Live Project

🔹 Portfolio (Frontend): https://amitr2k11.github.io/

🔹 Backend Repository: https://github.com/amitr2k11/RAG-Portfolio-Backend

The chatbot dynamically answers questions about my experience using a real RAG pipeline powered by a local LLM.

🧠 Project Overview

This project implements a Retrieval-Augmented Generation (RAG) chatbot integrated into my personal portfolio website.

Instead of hardcoded responses, the chatbot:

Loads knowledge from profile.txt

Converts text into embeddings

Stores vectors using FAISS

Retrieves relevant context for each query

Generates intelligent responses using a local LLM (phi3)

⚡ Fully local — no OpenAI API required.

🏗️ Architecture
User (GitHub Pages Frontend)
        ↓
JavaScript fetch()
        ↓
Cloudflare Tunnel (Public URL)
        ↓
FastAPI Backend (/chat)
        ↓
RAG Pipeline (LangChain + FAISS)
        ↓
Ollama (phi3 LLM)
        ↓
Generated Response

🛠️ Tech Stack
🔹 Backend

FastAPI

LangChain

FAISS (Vector Store)

Ollama (Local LLM)

Uvicorn

🔹 AI Models

phi3 → Response generation

nomic-embed-text → Embeddings

🔹 Deployment

Local backend server

Exposed via Cloudflare Tunnel

Frontend hosted on GitHub Pages

📁 Project Structure
RAG-Portfolio-Backend/
│── app.py              # FastAPI entry point
│── rag.py              # RAG pipeline logic
│── requirements.txt    # Python dependencies
│── .gitignore
│
└── Data/
    └── profile.txt     # Knowledge base

⚙️ Local Setup
1️⃣ Install Ollama

Download from:
https://ollama.com/

Pull required models:

ollama pull phi3
ollama pull nomic-embed-text

2️⃣ Install Python Dependencies
pip install -r requirements.txt

3️⃣ Run Backend
uvicorn app:app --reload


Runs at:

http://127.0.0.1:8000

4️⃣ Expose Backend (Optional - Public Access)
cloudflared tunnel --url http://127.0.0.1:8000


Copy generated URL and update frontend fetch request:

fetch("https://your-tunnel-url/chat")

🔐 Security

.env file excluded via .gitignore

No API keys committed

Fully local LLM (no external API dependency)

GitHub secret scanning enabled

💡 Why This Project Is Impressive

✔ Real RAG implementation
✔ Local LLM deployment
✔ Vector search using FAISS
✔ Frontend + Backend integration
✔ Cloudflare tunneling setup
✔ Secure Git workflow (secret handling, repo separation)
✔ Production-style architecture

This demonstrates:

AI engineering fundamentals

Full-stack integration

Deployment knowledge

Secure development practices

🚀 Future Improvements

Persistent backend hosting (Railway / Render / Fly.io)

Streaming token responses

Chat memory support

Admin dashboard for knowledge updates

Docker containerization

👨‍💻 About Me

Amit Ranjan
Product Consultant | AI Builder | Data-Driven Problem Solver

🔗 LinkedIn: https://www.linkedin.com/in/amitrnjan/

🌐 Portfolio: https://amitr2k11.github.io/

⭐ If You Like This Project

Give it a ⭐ on GitHub — it motivates further AI builds!
