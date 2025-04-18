# 🧠 Master Research Agent

This is the core AI research assistant project that uses a **LangGraph-powered Oracle agent** to autonomously:

- Classify and understand your query
- Search ArXiv papers, filter relevance, and search the web
- Use Retrieval-Augmented Generation (RAG) to inject facts
- Generate a well-informed, cited answer using GPT-4o

---

## 🧰 Tools Used by the Oracle Agent

The central oracle LLM agent decides what tools to use based on your query:

| Tool Name         | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `rag_search`        | Performs similarity search via Pinecone using embedded query              |
| `rag_search_filter` | Filters relevant context from ArXiv/Pinecone embeddings                   |
| `fetch_arxiv`       | Fetches full metadata/content from ArXiv (open source requests)           |
| `web_search`        | Real-time web search via SerpAPI                                          |
| `final_answer`      | Synthesizes a complete, cited answer with GPT-4o                          |

The agent may loop through these tools, refine context, and only then generate an answer.

---

## 🧠 Agent Flow Overview

The workflow is implemented using **LangGraph**, where:

1. Input goes to the **oracle LLM node**
2. The oracle decides whether to:
   - Query RAG (ArXiv via Pinecone)
   - Fetch ArXiv
   - Search the web (SerpAPI)
   - Filter and refine context
4. Finally, the **`final_answer`** tool synthesizes a response with citations.

![Agent Flow](/master_research_agent/graph.png)

---

## 🚀 Run the Agent

1. Add your API keys to the `.env` file
2. Download all the requirements
3. Run the Notebook

