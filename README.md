<div align="center">

# Saksham Kriplani
### **Applied AI & Full-Stack Systems Engineer**

*Designing grounded document intelligence engines, hybrid retrieval architectures, and type-safe distributed web applications.*

<br/>

[![Live Demo](https://img.shields.io/badge/Live_Demo-enterprise--ai--knowledge--engine.vercel.app-0070F3?style=for-the-badge&logo=vercel&logoColor=white)](https://enterprise-ai-knowledge-engine.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/SakshamKriplani)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kriplanisaksham.31@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SakshamKriplani)

</div>

---

## 📌 Executive Summary

I am a software engineer focused on bridging the gap between cutting-edge AI models and production software engineering. My work focuses on **auditable Retrieval-Augmented Generation (RAG)**, **hybrid vector-lexical search algorithms**, and **modular backend/frontend architectures**.

Rather than relying on ungrounded generative black boxes, I design deterministic information retrieval pipelines that enforce page-level auditability, sub-second latency, and zero hallucination tolerances.

---

## 🏗️ Core Engineering Specializations

```text
┌──────────────────────────────────────────────────────────────────────────────┐
│  AI & Grounded Retrieval (RAG)                                               │
│  Dense Vector Search (FAISS) • BM25 Lexical Scoring • Reciprocal Rank Fusion │
│  Sentence Transformers • Page-Bounded Chunking • Deterministic Relevance Gate│
├──────────────────────────────────────────────────────────────────────────────┤
│  Backend Systems & Data Architecture                                         │
│  FastAPI • Python 3.11+ • Pydantic v2 • Async Architecture • SQLite • REST   │
├──────────────────────────────────────────────────────────────────────────────┤
│  Modern Frontend Engineering                                                 │
│  React 18 • TypeScript (Strict) • Tailwind CSS 4 • Vite • Recharts • SPA     │
├──────────────────────────────────────────────────────────────────────────────┤
│  DevOps & Platform Engineering                                               │
│  Docker Containerization • Vercel Edge • Linux • CI/CD Pipelines • Git Ops   │
└──────────────────────────────────────────────────────────────────────────────┘
```

---

## 🚀 Flagship Project: Enterprise AI Knowledge Engine

> **Production-grade grounded document intelligence platform with hybrid retrieval, page-level citations, and local LLM reasoning.**  
> 🔗 **Repository:** [github.com/SakshamKriplani/Enterprise-AI-Knowledge-Engine](https://github.com/SakshamKriplani/Enterprise-AI-Knowledge-Engine)  
> 🌐 **Interactive Live Application:** [enterprise-ai-knowledge-engine.vercel.app](https://enterprise-ai-knowledge-engine.vercel.app)

```mermaid
flowchart LR
    PDF["📄 Raw PDFs"] --> PARSE["PyMuPDF Extraction"]
    PARSE --> CHUNK["Token Chunker (200t, Within Page)"]
    CHUNK --> FAISS[("FAISS Dense Vectors")]
    CHUNK --> BM25["BM25 Sparse Index"]
    
    Q["Query"] --> DENSE["Vector Search (Top 20)"]
    Q --> SPARSE["BM25 Search (Top 20)"]
    DENSE & SPARSE --> RRF["Reciprocal Rank Fusion (k=60)"]
    RRF --> GATE{"Relevance Gate"}
    GATE -->|Pass| LLM["Ollama / llama3.2:3b"]
    GATE -->|Fail| DET["Deterministic 'Not Found'"]
    LLM --> OUT["Grounded Answer + [n] Citations"]
```

### Architectural & Engineering Highlights:
- **Token-Aware Page-Bounded Chunking:** Chunks are strictly constrained within individual PDF pages and tokenized via `sentence-transformers/all-MiniLM-L6-v2` tokenizer offsets (200 tokens window, 40 overlap), guaranteeing 100% exact page-level citations.
- **Reciprocal Rank Fusion (RRF):** Fuses dense embeddings and BM25 lexical scores ($k=60$) to eliminate scale mismatches between cosine similarity and BM25 scores.
- **Deterministic Hallucination Gate:** An empirical cosine threshold ($0.25$) halts pipeline execution on out-of-domain queries, bypassing generative hallucination.
- **Real Benchmark Performance:**
  - **Hybrid Hit@1:** `86.7%` (vs. Semantic `80.0%`, Keyword `73.3%`)
  - **Hybrid Hit@5:** `96.7%` | **MRR:** `0.897`
- **In-Browser Demo Engine:** The entire retrieval lifecycle (BM25 tokenization, RRF fusion, candidate deduplication, and citation parsing) was ported to client-side TypeScript to run in the browser at zero operational cost.

---

## 🛠️ Comprehensive Technical Stack

### Languages & Runtime
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

### AI, Information Retrieval & NLP
![FAISS](https://img.shields.io/badge/FAISS-Vector_Search-00599C?style=flat-square)
![SentenceTransformers](https://img.shields.io/badge/Sentence--Transformers-all--MiniLM--L6--v2-FFA500?style=flat-square)
![BM25](https://img.shields.io/badge/BM25Okapi-Lexical_Search-green?style=flat-square)
![RRF](https://img.shields.io/badge/Reciprocal_Rank_Fusion-Rank_Merging-purple?style=flat-square)
![PyMuPDF](https://img.shields.io/badge/PyMuPDF-PDF_Parsing-red?style=flat-square)
![Ollama](https://img.shields.io/badge/Ollama-Local_LLM_Inference-black?style=flat-square&logo=ollama&logoColor=white)

### Backend Engineering
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic_v2-E92063?style=flat-square&logo=pydantic&logoColor=white)
![Uvicorn](https://img.shields.io/badge/Uvicorn-499848?style=flat-square&logo=gunicorn&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![HTTPX](https://img.shields.io/badge/HTTPX-Async_Client-blue?style=flat-square)
![Pytest](https://img.shields.io/badge/Pytest-Testing-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

### Frontend Engineering
![React](https://img.shields.io/badge/React_18-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS_4-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router_7-CA4245?style=flat-square&logo=react-router&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=flat-square&logo=axios&logoColor=white)
![Recharts](https://img.shields.io/badge/Recharts-Data_Viz-22b5bf?style=flat-square)

### Tooling & Infrastructure
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

## 📐 Engineering Principles & Practices

1. **Deterministic Grounding Over Blind Trust:** AI outputs must be bounded by structured source passages. Every generated claim must link directly to an auditable document and page number.
2. **Strict Type Contracts:** End-to-end type safety using Python Pydantic v2 schemas for all backend I/O and strict TypeScript with zero `any` on the frontend.
3. **Data-Driven Architecture:** Algorithms and configurations (such as chunk size, overlap, embedding models, and RRF parameters) are selected through empirical benchmarking (`run_eval.py`), not intuition.
4. **Resilient Failure Modes:** Explicit HTTP status contracts, clean error boundaries, and graceful degradation paths when upstream AI components or network dependencies are unreachable.

---

## 📊 Analytics & Activity

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=SakshamKriplani&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="Saksham's GitHub Stats" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=SakshamKriplani&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" width="48%" />
</div>

<br/>

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=SakshamKriplani&theme=tokyonight&hide_border=true" alt="GitHub Streak" width="96%" />
</div>

---

## 📬 Let's Connect

I am always open to discussing distributed systems, RAG architectures, applied machine learning, or software engineering opportunities.

- 💼 **LinkedIn:** [linkedin.com/in/SakshamKriplani](https://linkedin.com/in/SakshamKriplani)
- 📧 **Direct Inquiries:** [kriplanisaksham.31@gmail.com](mailto:kriplanisaksham.31@gmail.com)
- 🌐 **Project Showcase:** [enterprise-ai-knowledge-engine.vercel.app](https://enterprise-ai-knowledge-engine.vercel.app)

<br/>

<div align="center">
  <sub>Built with engineering rigor • Saksham Kriplani</sub>
</div>
