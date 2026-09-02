# Project-2-StudyPal

StudyPal is an intelligent, RAG‑powered study assistant designed for Class 12 students. It answers questions based on your textbooks, provides relevant YouTube video recommendations, and supports multiple subjects like Biology, Physics, and Chemistry.

✨ Features

📚 Textbook‑Based Q&A – Ask questions about your Class 12 subjects and get accurate answers sourced from your textbooks.

🎥 YouTube Video Recommendations – Each answer comes with 3 relevant video links to reinforce learning.

🧠 RAG (Retrieval‑Augmented Generation) – Uses Groq's high‑performance LLM combined with vector search for grounded answers.

📂 Chapter‑Wise Context – Choose a specific chapter or query across all chapters for comprehensive understanding.

🔄 Conversation Memory – Maintains chat history for contextual follow‑up questions.

⚡ Fast & Lightweight – Powered by Groq's lightning‑fast inference with local HuggingFace embeddings.


🛠️ Tech Stack

Frontend	- Streamlit

LLM	 - Groq 

Embeddings	- HuggingFace (all‑mpnet‑base‑v2 – 768‑dim)

Vector Store	- Chroma 

Document Processing	- UnstructuredFileLoader, RecursiveCharacterTextSplitter

Video Search	- YouTubeSearch, Python

Orchestration	- LangChain 

Language	- Python 3.12


🧠 How It Works

Document Ingestion – PDF textbooks are loaded, split into chunks (2000 chars, 500 overlap), and embedded using HuggingFace embeddings.

Vector Storage – Chroma stores embeddings with 768‑dimension vectors.

Query Processing – When you ask a question:

The query is embedded.

Relevant chunks are retrieved using MMR (Maximum Marginal Relevance) to ensure diversity.

The context, chat history, and query are sent to Groq LLM.

The model generates a grounded answer.

Video Suggestions – Your chat history is used to search YouTube for 3 relevant videos.





