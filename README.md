# live-regulatory-compliance-agent
A live, agentic AI system for real-time regulatory compliance using Pathway streaming engine.
# Live Regulatory Compliance Agent

A real-time, agentic AI system that provides always-updated and explainable regulatory
compliance intelligence using Pathway’s streaming engine.

This project is built for **Track 1: Agentic AI with Live Data** and demonstrates how
streaming ingestion and agent-based reasoning can overcome the limitations of static RAG
systems.

---

## 🔍 Problem Overview

Regulatory documents such as circulars, notifications, and policies are updated frequently.
Traditional compliance tools and RAG-based AI systems rely on static embeddings that become
outdated immediately after a document change.

This leads to:
- Stale compliance answers
- Manual re-indexing overhead
- Lack of change awareness
- Poor explainability for audits

---

## 💡 Solution Summary

This project implements a **Live Regulatory Compliance Agent** that:
- Continuously monitors regulatory documents
- Updates embeddings incrementally at chunk level
- Performs multi-step agentic reasoning
- Produces explainable, traceable compliance outputs

The system guarantees **data freshness without re-indexing**.

---

## 🏗️ Architecture (High Level)

Regulatory Documents
↓
Pathway Streaming Engine
↓
Live Vector Store (Incremental Embeddings)
↓
Agent Reasoning Layer (LangGraph / LangChain)
↓
LLM Reasoning Engine
↓
User Interface / API

yaml
Copy code

---

## 🔄 Workflow Overview

1. Regulatory document is added / edited / deleted
2. Pathway streaming engine detects the change
3. Only modified document chunks are processed
4. Incremental embeddings are updated in real time
5. Agent retrieves latest regulatory context
6. Multi-step reasoning is performed:
   - Change detection
   - Applicability analysis
   - Impact assessment
   - Action recommendation
7. Explainable response is generated with references

---

## ✨ Key Features & Novelties

- Real-time document ingestion (no batch jobs)
- Incremental, chunk-level embedding updates
- Event-driven compliance intelligence
- Agentic multi-step reasoning (not simple Q&A)
- Explainable outputs with clause references
- Zero downtime updates
- Future-ready for BDH integration

---

## 🧰 Tech Stack

- **Pathway** – Real-time streaming engine
- **Pathway Vector Store** – Live embeddings
- **LangGraph / LangChain** – Agent orchestration
- **LLM (OpenAI / Claude / Mistral)** – Reasoning & explanation
- **Python** – Backend implementation
- **Streamlit / Gradio** – Demo UI
- **GitHub** – Version control

---

## ▶️ Live Demo Instructions

### Step 1: Start the system
```bash
python app/app.py
