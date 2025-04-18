# LLM-Research-Agent
LLM Research Agent: LangGraph + GPT-4o + Pinecone + Google SerpAPI + ArXiv

---

## 🧠 What It Does

This project features a **LangGraph-powered Oracle agent** that:
- Understands your query
- Chooses from multiple tools (RAG, ArXiv, Web Search)
- Retrieves relevant academic and real-time information
- Synthesizes a clear, cited answer using GPT-4o

---

### `master_research_agent/` – **Main Project**
- A full LangGraph-based LLM agent using:
  - `rag_search`, `rag_search_filter`
  - `fetch_arxiv`, `web_search`, `final_answer`
- Uses Pinecone for vector search, SerpAPI for real-time data, and GPT-4o for final reasoning.

👉 [Explore the Master Agent](master_research_agent/README.md)

---

### `starter_agent/` – **Beginner-Friendly Notebooks**
- `01_building_an_agent_from_scratch.ipynb`: ReAct agent using pure Python
- `02_building_with_langgraph.ipynb`: LangGraph chatbot with Tavily AI

Great for learning agentic LLMs step-by-step.

### 🚀 Quickstart

1. **Download this repo**

2. **Before running notebooks, open the `.env` file and paste your API keys**:
   - `OPENAI_API_KEY`
   - `PINECONE_API_KEY`
   - `SERPAPI_API_KEY`
   - *(Optional)* `TAVILY_API_KEY`
