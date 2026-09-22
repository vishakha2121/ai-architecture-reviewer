<div align="center">

# 🏛️ Arch Reviewer AI

### Autonomous Enterprise Architecture Reviewer

*Detect design flaws. Recommend improvements. Generate modernization roadmaps.*

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-009688?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18+-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev)
[![Gemini](https://img.shields.io/badge/Gemini-AI-4285F4?style=flat&logo=google&logoColor=white)](https://ai.google.dev)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**[Features](#-features) • [Demo](#-demo) • [Tech Stack](#-tech-stack) • [Setup](#-quick-start) • [Architecture](#-architecture)**

</div>

---

## 📖 What is Arch Reviewer AI?

**Arch Reviewer AI** is an autonomous AI-powered system that reviews enterprise 
software architectures the way a senior architect would — but in seconds.

Upload your architecture (code, description, or diagram), and the system will:

- 🔍 **Detect design flaws** — tight coupling, single points of failure, 
  circular dependencies, anti-patterns, scalability bottlenecks
- 💡 **Recommend improvements** — concrete, prioritized, actionable fixes
- 🗺️ **Generate modernization roadmaps** — phased migration plans 
  (e.g., monolith → microservices) with timelines and tasks
- 🕸️ **Visualize as a Knowledge Graph** — interactive node-edge view of 
  components and their relationships

Unlike simple LLM wrappers, Arch Reviewer AI combines:

- **Static Analysis** (deterministic, rule-based code parsing)
- **Knowledge Graphs** (structured representation of architecture)
- **GraphRAG** (graph-aware retrieval + LLM reasoning)
- **Gemini AI** (for high-level reasoning and recommendations)

This hybrid approach delivers **explainable, accurate, and grounded** results 
— not hallucinations.

---

## 🎯 Problem It Solves

Enterprise architectures silently accumulate **technical debt**:

- Microservices that become distributed monoliths
- Tight coupling between modules
- Single points of failure
- Outdated patterns blocking modernization

Manual architecture reviews are:

- ❌ Expensive (senior architects cost $$$)
- ❌ Slow (weeks per review)
- ❌ Subjective (opinion-based)
- ❌ Inconsistent (varies by reviewer)

**Arch Reviewer AI makes it:**

- ✅ Free / low-cost
- ✅ Instant (seconds)
- ✅ Objective (rules + AI)
- ✅ Consistent (same standard every time)

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🤖 **AI-Powered Analysis** | Gemini LLM with custom architecture-specific prompts |
| 🕸️ **Knowledge Graph Engine** | NetworkX-based graph of components, dependencies, and patterns |
| 🔎 **GraphRAG Retrieval** | ChromaDB + graph traversal for grounded AI responses |
| 📊 **Static Code Analysis** | AST-based parsing (Python) for dependency extraction |
| ⚠️ **Flaw Detection** | 20+ anti-pattern rules + AI-driven detection |
| 💡 **Smart Recommendations** | Priority-ranked, effort-estimated, actionable |
| 🗺️ **Modernization Roadmaps** | Multi-phase plans with tasks and timelines |
| 📈 **Interactive Dashboard** | Charts, metrics, severity scores |
| 🎨 **Beautiful UI** | Dark-mode glassmorphism, Framer Motion animations |
| 📄 **PDF Reports** | Downloadable analysis reports |

---

## 🛠️ Tech Stack

**Backend**

- Python 3.11+ · FastAPI · SQLAlchemy · SQLite
- Google Gemini API · ChromaDB · NetworkX
- Python AST (static analysis) · JWT Auth

**Frontend**

- React 18 · Vite · TailwindCSS
- React Flow (graph) · Recharts (charts) · Framer Motion
- Zustand (state) · Axios · React Router

**AI / ML**

- GraphRAG pipeline (graph + vector retrieval)
- Custom prompt engineering for architecture domain
- Embedding-based semantic search

---

## 🏗️ Architecture

---

## 🚀 Quick Start

### Prerequisites

- Python 3.11+
- Node.js 18+
- Gemini API Key ([Get it here](https://aistudio.google.com/apikey))

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vishakha2121/ai-architecture-reviewer.git
cd ai-architecture-reviewer

cd backend
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate

pip install -r requirements.txt
cp .env.example .env
# Add your GEMINI_API_KEY in .env

uvicorn main:app --reload

cd frontend
npm install
npm run dev