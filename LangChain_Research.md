# LangChain: Complete History, Timeline & Features

---

## Origins & Founding Story

**Harrison Chase**, a Harvard graduate (Statistics + CS, 2017), was working as Head of ML at **Robust Intelligence** in 2022. While building GPT-3 prototypes internally, he noticed a recurring pain point: developers were stitching together LLMs with fragmented tools and no shared abstractions.

In **9 days** — between October 16–25, 2022 — Chase built LangChain from his apartment as a side project. The first version was a single ~800-line Python file: essentially a wrapper for prompt templates.

---

## Full Timeline

### 2022 — The Spark

| Date | Event |
|------|-------|
| **Oct 16–25, 2022** | Harrison Chase pushes first LangChain commit to `hwchase17/langchain` on GitHub. Initial version: a Python prompt-template wrapper. |
| **Nov 2022** | OpenAI launches ChatGPT. Developer interest in LLM tooling explodes. LangChain starts gaining rapid organic traction. |
| **Dec 2022** | LangChain grows to thousands of GitHub stars. First wave of community contributors arrives. |

---

### 2023 — Hypergrowth & Company Formation

| Date | Event |
|------|-------|
| **Jan 2023** | LangChain formally incorporated as a company. Co-founder **Ankush Gola** joins Harrison Chase. |
| **Feb 2023** | GitHub stars hit **5,000**. LangChain becomes one of the fastest-growing open-source projects ever. |
| **Mar 2023** | **$10M seed round** led by **Benchmark**. |
| **Apr 2023** | **$20M+ Series A** led by **Sequoia Capital** at $200M+ valuation. GitHub stars jump from 5K → **18K** in 2 months. |
| **Mid 2023** | **LangChain Expression Language (LCEL)** introduced — a declarative, composable syntax using the `\|` pipe operator for defining chains. Replaces older `LLMChain` / `SequentialChain` classes. Adds auto-batching, streaming, and async support. |
| **Summer 2023** | **LangSmith beta** launched — an observability, tracing, and evaluation platform. Designed to be framework-agnostic. Development on **LangGraph** begins based on user feedback requesting more agent controllability. |
| **Oct 2023** | **LangServe** released — a deployment tool for hosting LCEL chains as production-ready REST APIs. |

---

### 2024 — Agents Take Center Stage

| Date | Event |
|------|-------|
| **Early 2024** | **LangGraph** launches publicly. Introduces graph-based, stateful agent orchestration with: persistent checkpoints, cyclic execution, human-in-the-loop support, and streaming. |
| **Feb 2024** | **LangSmith** released as a generally available product (was beta). **$25M Series A** led by Sequoia Capital announced alongside it. |
| **Throughout 2024** | LangChain ecosystem splits into modular packages: `langchain-core`, `langchain-community`, `langchain-openai`, etc. Major enterprise customers onboard (LinkedIn, Uber, Klarna). |
| **Dec 2024** | LangChain crosses **96K GitHub stars** and **28 million monthly downloads**. |

---

### 2025 — Stability, Scale & v1.0

| Date | Event |
|------|-------|
| **Apr 2025** | LangChain featured in **Forbes AI 50** list. |
| **May 14, 2025** | **LangGraph Platform** reaches General Availability — managed cloud infrastructure for deploying long-running, stateful agents. |
| **Oct 20–22, 2025** | **LangChain 1.0 & LangGraph 1.0** released simultaneously. Landmark stable releases committing to no breaking changes until 2.0. |
| **Oct 2025** | **$125M Series B** at **$1.25B valuation** announced. |

---

### 2026 — Current State

| Date | Event |
|------|-------|
| **Jan 2026** | LangSmith Self-Hosted v0.13 released with expanded feature parity and Insights integration. |
| **Feb 2026** | Cost tracking expanded across full agent stack. Agent Builder gains chat, file upload, and tool registry access. |
| **Mar 2026** | LangSmith Agent Builder renamed to **LangSmith Fleet**. |
| **May 2026** | LangGraph 1.2 released with content-block-aware streaming, improved `interrupt()` semantics, Python 3.10–3.14 support. LangChain: **80M monthly downloads**, **1M+ developer community**. |

---

## Core Products & Features

### 1. LangChain Framework (Core)

The foundational Python/JS library for building LLM applications.

| Feature | Description | Added |
|---------|-------------|-------|
| **Prompt Templates** | Reusable, parameterized instruction blueprints | Oct 2022 |
| **LLM Wrappers** | Unified interface over OpenAI, Anthropic, Cohere, etc. | Oct 2022 |
| **Chains** | Sequential/parallel pipelines of LLM calls and actions | Late 2022 |
| **Document Loaders** | Load from PDFs, HTML, Notion, Google Drive, S3, 50+ formats | 2023 |
| **Text Splitters** | Chunking strategies for long documents | 2023 |
| **Embeddings** | Unified interface for embedding models | 2023 |
| **Vector Stores** | Connectors for FAISS, Pinecone, Chroma, Weaviate, pgvector, etc. | 2023 |
| **Retrievers** | Semantic + keyword search, MMR, contextual compression | 2023 |
| **Memory** | Conversation buffer, summary, entity, and vector-store-backed memory | 2023 |
| **Agents** | ReAct, OpenAI Functions, structured tool-calling agents | 2023 |
| **Tools** | Web search, calculators, code execution, API calls | 2023 |
| **LCEL (Expression Language)** | Pipe-based composable chain syntax with streaming/async | Q3 2023 |
| **Callbacks** | Logging, tracing, and monitoring hooks | 2023 |
| **Output Parsers** | Structured JSON/Pydantic extraction from LLM output | 2023 |
| **Content Blocks** | Standardized message format (text, reasoning, citations, tool calls) | Oct 2025 |
| **Middleware** | Injectable behaviors (HITL, PII redaction, summarization) at any agent step | Oct 2025 |
| **`create_agent()`** | New standard agent entrypoint replacing `create_react_agent` | Oct 2025 |

---

### 2. LangServe

A deployment tool for serving LangChain/LCEL apps as REST APIs.

- **Released:** October 2023
- Auto-generates OpenAPI docs
- Built on FastAPI
- Handles streaming, batching, async
- *Note: largely superseded by LangGraph Platform by 2025*

---

### 3. LangSmith

Observability, evaluation, and debugging platform for LLM apps.

| Feature | Description | Timeline |
|---------|-------------|----------|
| **Tracing** | Full trace of every chain/agent step | Beta: Summer 2023; GA: Feb 2024 |
| **Evaluation** | Run test datasets, score outputs | 2024 |
| **Datasets** | Build golden datasets for regression testing | 2024 |
| **Annotation Queues** | Human feedback labeling workflows | 2024 |
| **Experiments** | A/B test prompts and models | 2024 |
| **Pairwise Comparison** | Side-by-side output comparison | Dec 2025 |
| **Cost Tracking** | Full-stack cost visibility (not just LLM calls) | Feb 2026 |
| **Insights Agent** | Scheduled report generation | Feb 2026 |
| **LangSmith Fetch CLI** | Terminal-based trace debugging tool | Dec 2025 |
| **LangSmith Fleet** | Agent deployment builder (formerly Agent Builder) | Mar 2026 |
| **Self-Hosted v0.13** | On-prem deployment with full feature parity | Jan 2026 |

---

### 4. LangGraph

A stateful, cyclic graph orchestration layer for complex agents.

| Feature | Description | Timeline |
|---------|-------------|----------|
| **Graph-based orchestration** | Nodes = actions, edges = conditional routing | Early 2024 |
| **Persistent state (checkpointing)** | Survives restarts, resumes mid-workflow | Early 2024 |
| **Human-in-the-loop (HITL)** | Pause execution for human review/approval | Early 2024 |
| **Streaming** | Token and intermediate-step streaming | Early 2024 |
| **Multi-agent support** | Supervisor, hierarchical, and collaborative agent patterns | 2024 |
| **LangGraph Platform** | Managed cloud infra for stateful agents | GA: May 2025 |
| **LangGraph 1.0** | Stable, production-committed release | Oct 2025 |
| **LangGraph 1.2** | Content-block streaming, improved interrupts | May 2026 |

---

## Integrations & Ecosystem (as of 2026)

| Category | Options |
|----------|---------|
| **LLM Providers** | OpenAI, Anthropic, Google Gemini, AWS Bedrock, Azure OpenAI, Cohere, Mistral, Ollama, Hugging Face, and 40+ more |
| **Vector Databases** | FAISS, Pinecone, Chroma, Weaviate, Qdrant, Milvus, pgvector, Redis, Elasticsearch |
| **Document Sources** | PDF, Word, HTML, Markdown, Notion, Google Drive, S3, Confluence, Slack, GitHub |
| **Tools / APIs** | Google Search, Bing, Wolfram Alpha, Wikipedia, SQL DBs, REST APIs, Python REPL, Zapier |
| **Cloud Providers** | AWS, Google Cloud, Microsoft Azure |

---

## Funding History

| Date | Round | Amount | Lead Investor | Valuation |
|------|-------|--------|---------------|-----------|
| Mar 2023 | Seed | $10M | Benchmark | — |
| Apr 2023 | Series A | $20M+ | Sequoia Capital | $200M+ |
| Feb 2024 | Series A extension | $25M | Sequoia Capital | — |
| Oct 2025 | Series B | $125M | — | **$1.25B** |

---

## Key Metrics (May 2026)

| Metric | Value |
|--------|-------|
| GitHub Stars | 96K+ |
| Monthly Downloads | 80 million |
| Developer Community | 1 million+ |
| Enterprise Customers | Uber, LinkedIn, Klarna, Rippling, Vanta, Cloudflare, Replit, Harvey, J.P. Morgan, BlackRock |

---

## Sources

- [LangChain - Wikipedia](https://en.wikipedia.org/wiki/LangChain)
- [Reflections on Three Years of Building LangChain](https://www.langchain.com/blog/three-years-langchain)
- [LangChain Changelog](https://changelog.langchain.com/)
- [LangChain and LangGraph Agent Frameworks Reach v1.0 Milestones](https://www.langchain.com/blog/langchain-langgraph-1dot0)
- [LangChain 1.0 now generally available](https://changelog.langchain.com/announcements/langchain-1-0-now-generally-available)
- [LangGraph 1.0 is now generally available](https://changelog.langchain.com/announcements/langgraph-1-0-is-now-generally-available)
- [Report: LangChain Business Breakdown & Founding Story - Contrary Research](https://research.contrary.com/company/langchain)
- [Founder Story: Harrison Chase of LangChain](https://www.frederick.ai/blog/harrison-chase-langchain)
- [LangChain vs LangGraph vs LangSmith vs LangFlow - DataCamp](https://www.datacamp.com/tutorial/langchain-vs-langgraph-vs-langsmith-vs-langflow)
- [What's new in LangChain v1 - Docs](https://docs.langchain.com/oss/javascript/releases/langchain-v1)
