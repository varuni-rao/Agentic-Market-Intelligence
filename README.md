# Agentic Market Intelligence: Multi-Agent RAG Collaborative System 🤖📊

## 📌 Executive Summary
In high-stakes industries, competitive intelligence is often a manual, error-prone process. This project implements a **Multi-Agent Retrieval-Augmented Generation (RAG) system** that automates end-to-end competitor analysis. 

By leveraging **LangGraph** for state-machine logic and **Tavily** for real-time web intelligence, the system orchestrates a fleet of specialized AI agents to research, synthesize, and report on any given company with zero human intervention.

---

## 🏗 System Architecture & "Systems Thinking"
Drawing from my background in **SCADA and Control Systems**, I designed this pipeline as a sequential state-controlled loop. Each node in the graph ensures data integrity before passing it to the next stage.

### The Collaborative Workflow:
1. **Analyst Agent (Question Generator):** Validates the company name, identifies the industry sector, and generates targeted strategic questions.
2. **Research Agent (Data Retrieval & Storage):** Executes parallel web searches via Tavily, cleans the raw content, and populates a **ChromaDB Vector Store**.
3. **Strategist Agent (Report Drafter):** Performs RAG to retrieve context-aware data and synthesizes a professional, actionable report.

<div align="center">
  <img src="<Path to your architecture diagram>" width="700px" alt="System Architecture">
</div>

---

## 🛠 Tech Stack & Engineering Rigor
* **Orchestration:** `LangGraph` (State-based execution and sequential logic).
* **LLM:** `OpenAI GPT-4o-mini` with **Structured Outputs** (Pydantic models) for type-safety and reliability.
* **Real-time Intelligence:** `Tavily AI` for high-depth web crawling and RAG-ready content.
* **Vector Database:** `ChromaDB` (Persistent storage for high-dimensional embeddings).
* **Validation:** `Pydantic` for strict state management and data schema enforcement.

---

## 🎯 Case Study: NFL Market Analysis
To demonstrate the system's power, I ran an analysis of the **National Football League (NFL)** in the sports entertainment sector.
* **Input:** "NFL"
* **Process:** The system identified key competitors (NBA, MLB, Streaming platforms), researched global expansion strategies, and analyzed player safety metrics.
* **Output:** A comprehensive Markdown report including SWOT analysis, market differentiators, and 5-year strategic recommendations.

<div align="center">
  <img src="https://github.com/user-attachments/assets/faed92f5-d393-4440-8131-34b66e0160ad" width="700px" alt="Project Results">
</div>

---

## 🚀 Key Technical Highlights
* **State Management:** Uses a `CompetitiveAnalysisState` object to ensure "shared memory" across agents, preventing data loss during complex transitions.
* **RAG Loop:** Unlike standard RAG, this system *generates its own queries* based on identified market gaps before searching.
* **Scalability:** The architecture is modular; new agents (e.g., a Financial Analyst agent or a Risk Compliance agent) can be plugged into the LangGraph with minimal friction.

---

## ⚙️ Setup & Installation
1. Clone the repository.
2. Provide your `OPENAI_API_KEY` and `TAVILY_API_KEY` in your environment variables.
3. Run the Jupyter Notebook `agentic_market_intelligence.ipynb`.
