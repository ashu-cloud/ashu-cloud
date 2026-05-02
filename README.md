<div align="center">

```
█████╗ ███████╗██╗  ██╗██╗   ██╗    ██████╗  █████╗ ███╗   ██╗ ██████╗██╗  ██╗ █████╗ ██╗
██╔══██╗██╔════╝██║  ██║██║   ██║    ██╔══██╗██╔══██╗████╗  ██║██╔════╝██║  ██║██╔══██╗██║
███████║███████╗███████║██║   ██║    ██████╔╝███████║██╔██╗ ██║██║     ███████║███████║██║
██╔══██║╚════██║██╔══██║██║   ██║    ██╔═══╝ ██╔══██║██║╚██╗██║██║     ██╔══██║██╔══██║██║
██║  ██║███████║██║  ██║╚██████╔╝    ██║     ██║  ██║██║ ╚████║╚██████╗██║  ██║██║  ██║███████╗
╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝ ╚═════╝     ╚═╝     ╚═╝  ╚═╝╚═╝  ╚═══╝ ╚═════╝╚═╝  ╚═╝╚═╝  ╚═╝╚══════╝
```

### Backend & Full-Stack Engineer · Building systems that actually scale

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ashu-panchal-24b5bb189/)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ashupanchal8360@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/AshuPanchal/)
[![CodeChef](https://img.shields.io/badge/CodeChef-5B4638?style=for-the-badge&logo=codechef&logoColor=white)](https://www.codechef.com/users/ashu_cloud_29)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://docs.google.com/document/d/1-Yjb5ENYOD2Vs0dJ_CEWB1U7fV6E2rJllVRu3-bMotE/edit?usp=sharing)

</div>

---

<div align="center">

| 🏆 LeetCode | 🌟 CodeChef | 📚 CGPA | 🗂️ Repos | 🎓 Certs |
|:-----------:|:-----------:|:-------:|:--------:|:--------:|
| **1834** peak rating | **3★** peak | **7.8 / 10** | **20+** public | **2× Oracle OCI** |
| Top 6.5% globally | Div. 2 | JSS Academy, Noida | TypeScript · Python · C++ | Gen AI · AI Foundations |

</div>

---

## `whoami`

```typescript
const ashu = {
  role:     "3rd-Year B.Tech IT @ JSS Academy of Technical Education, Noida (AKTU 2023–27)",
  seeking:  "Paid Software Engineering Internship — Backend · Full-Stack · Fintech",
  
  builds:   [
    "Event-driven backends with BullMQ, Celery, Redis",
    "AI-powered products using GPT-4o, Claude, Gemini, LLaMA via Groq",
    "Fintech systems — double-entry ledgers, idempotency, ACID guarantees",
    "Agentic systems — browser-use automation, LLM-driven task execution",
  ],

  stack:    {
    primary:  ["TypeScript", "Node.js", "Next.js", "PostgreSQL", "Redis"],
    growing:  ["Python", "FastAPI", "Celery", "Docker", "Kubernetes"],
    ai:       ["OpenAI", "Anthropic Claude", "Groq / LLaMA", "Google Gemini"],
  },

  cp:       { leetcode: 1834, codechef: "3★", language: "C++" },
  certs:    ["Oracle OCI Generative AI Professional 2025", "Oracle OCI AI Foundations Associate 2025"],
};
```

> I don't just learn technologies — I build production-grade systems with them. Every project below ships with real architecture decisions, not toy examples.

---

## 🚀 Featured Projects

### 🔴 [`Postly`](https://github.com/ashu-cloud/Postly--ai-publishing-system-backend-) — Queue-Orchestrated AI Publishing Engine
> **`TypeScript` `Node.js` `Express` `BullMQ` `Redis` `PostgreSQL` `Prisma` `Docker` `GPT-4o` `Claude` `Telegram Bot`**

Takes a raw idea and dispatches platform-optimised content to Twitter, LinkedIn, Threads, and Instagram through an **async, fault-tolerant pipeline**. The REST API never calls a social platform directly — every request is serialised into a BullMQ job processed by isolated workers.

- **Dual-model AI** — GPT-4o (primary) + Claude (fallback) via OpenRouter with platform-specific prompts
- **Exponential backoff** with 5 retries per job; Redis persists queue state across server restarts
- **JWT + refresh-token rotation** with HTTP-only cookies; Redis sliding-window rate limiter on all public endpoints
- **Telegram Bot** (@Postly_49_Bot) interface via webhook — zero UI required
- **Containerised** with Docker Compose; CI/CD pipeline; deployed on Render

```
Client / Telegram Bot → Express API → BullMQ Queue → [Twitter | LinkedIn | Threads | Instagram] Workers
                                    ↘ AI Engine (GPT-4o / Claude via OpenRouter)
```

[![Live API](https://img.shields.io/badge/Live_API-Render-46E3B7?style=flat-square&logo=render)](https://postly-ai-publishing-system-backend.onrender.com)
[![Repo](https://img.shields.io/badge/Repo-GitHub-181717?style=flat-square&logo=github)](https://github.com/ashu-cloud/Postly--ai-publishing-system-backend-)

---

### 🟡 [`TradePulse`](https://github.com/ashu-cloud/trading-core-backend) — Fintech Trading Platform Core
> **`Node.js` `Express` `MongoDB` `React` `WebSockets` `Finnhub API`**

A production-grade stock trading platform built around the hard parts of fintech — money movement, consistency, and real-time data.

- **Double-entry ledger** — every transaction creates two balanced journal entries; no money appears from thin air
- **4-state payment state machine** — `PENDING → PROCESSING → SETTLED / FAILED`; clean transitions, no invalid states
- **Idempotency keys** — duplicate payment requests are deduplicated safely, ACID-safe across all trade flows
- **WebSocket feed** — live price updates from Finnhub, pushed to connected clients without polling

---

### 🟢 [`PrepPath`](https://github.com/ashu-cloud/PrepPath) — AI-Powered Course Generation Platform
> **`Next.js` `TypeScript` `PostgreSQL` `Drizzle ORM` `Google Gemini 2.5 Flash` `LLaMA 3.3 via Groq` `NDJSON Streaming`**

Full-stack platform that generates personalised learning tracks on any topic using multi-model AI.

- **NDJSON streaming** — course content streams to the UI token-by-token; no waiting for full generation
- **Dual-model architecture** — Gemini for curriculum structure, LLaMA via Groq for content expansion
- **Drizzle ORM** with PostgreSQL — type-safe queries, schema migrations baked in

---

### 🔵 [`PanelPilot`](https://github.com/ashu-cloud/PanelPilot) — AI Browser Automation Agent
> **`Python` `FastAPI` `Playwright` `browser-use` `Groq (LLaMA-4-Scout)` `Jinja2`**

An AI agent that performs IT admin tasks by **visually navigating** a real browser — no CSS selectors, no API shortcuts. The agent reads the page DOM, decides what to click or fill, and acts like a human operator.

- **Natural language → action** — `"Reset password for john@company.com to NewSecure2024"` runs in 3–6 steps
- `temperature=0.0` for deterministic, repeatable navigation in production workflows
- **PRG pattern** on all POSTs gives the agent unambiguous success/failure feedback via banner states
- **32 tests, zero API calls** — fully mocked test suite, ~1 second runtime
- Slack bot integration; Headless mode for CI/CD; deployed on Railway

---

### 🟣 [`AI Task Processing Platform`](https://github.com/ashu-cloud/AI-Task-Processing-Platform) — Full-Stack DevOps Showcase
> **`Next.js` `Express` `Python Worker` `MongoDB` `Redis` `Docker` `Kubernetes` `Argo CD` `CI/CD`**

End-to-end task processing system demonstrating the full DevOps lifecycle from local Docker Compose to Kubernetes cluster deployment with GitOps via Argo CD.

- Async task processing with Redis queue; Python worker for background jobs
- JWT auth, bcrypt, Helmet, rate limiting — security-first API
- **Kubernetes manifests + Argo CD GitOps** pipeline included in repo
- GitHub Actions CI/CD workflow

---

### 🟠 [`Real-Time Document Analysis Pipeline`](https://github.com/ashu-cloud/Real-time-document-analysis-pipeline) — Async Processing with Live SSE
> **`React` `FastAPI` `Celery` `PostgreSQL` `Redis Pub/Sub` `SSE` `Docker Compose`**

Upload documents, watch them process in real time, edit extracted data, and export as JSON/CSV — powered by a Celery worker pool with Redis Pub/Sub streaming progress to the frontend via SSE.

- Live job status (Queued → Processing → Completed/Failed) without WebSocket overhead
- Full retry logic for failed jobs; SSE chosen over WebSockets for uni-directional correctness
- Docker Compose orchestrates 5 services: frontend, backend, worker, PostgreSQL, Redis

---

### ⚪ [`Nymity`](https://github.com/ashu-cloud/Nymity) — Real-Time Anonymous Feedback Platform
> **`Next.js` `MongoDB` `Pusher WebSockets` `Upstash Redis`**

Anonymous feedback platform with real-time delivery — feedback appears instantly on the receiver's dashboard without page refresh. Redis used for rate limiting anonymous submissions.

---

### ⚫ [`SummaryStreet`](https://github.com/ashu-cloud/SummaryStreet) — AI Summarisation App
> **`TypeScript` `Next.js` `PostgreSQL`**

[![Live Demo](https://img.shields.io/badge/Live_Demo-Vercel-000000?style=flat-square&logo=vercel)](https://summary-street.vercel.app/)

---

## 🛠 Tech Stack

<div align="center">

**Languages**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

**Backend & Runtime**

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)

**Databases & Queues**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![BullMQ](https://img.shields.io/badge/BullMQ-FF3333?style=for-the-badge&logo=bull&logoColor=white)
![Celery](https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=celery&logoColor=white)

**AI / LLM**

![OpenAI](https://img.shields.io/badge/OpenAI_GPT--4o-412991?style=for-the-badge&logo=openai&logoColor=white)
![Claude](https://img.shields.io/badge/Anthropic_Claude-D4845A?style=for-the-badge)
![Gemini](https://img.shields.io/badge/Google_Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)
![Groq](https://img.shields.io/badge/Groq_LLaMA-F55036?style=for-the-badge)

**DevOps & Infra**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![Drizzle](https://img.shields.io/badge/Drizzle_ORM-C5F74F?style=for-the-badge)

</div>

---

## 🏆 Competitive Programming

<div align="center">

| Platform | Handle | Peak Rating | Rank |
|:--------:|:------:|:-----------:|:----:|
| [![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/u/AshuPanchal/) | [AshuPanchal](https://leetcode.com/u/AshuPanchal/) | **1834** | **Top 6.5% Globally** |
| [![CodeChef](https://img.shields.io/badge/CodeChef-5B4638?style=flat-square&logo=codechef&logoColor=white)](https://www.codechef.com/users/ashu_cloud_29) | [ashu_cloud_29](https://www.codechef.com/users/ashu_cloud_29) | **1633** | **3★ (Div. 2)** |

Problem-solving in **C++** · Strong in graphs, DP, greedy, binary search

</div>

---

## 🎓 Certifications

<div align="center">

| Certification | Issuer | Year |
|:-------------|:------:|:----:|
| 🏅 Generative AI Professional | Oracle OCI | 2025 |
| 🏅 AI Foundations Associate | Oracle OCI | 2025 |
| 🏅 HENNGE Global Internship Challenge | HENNGE | 2024 · RFC 6238 TOTP + HMAC-SHA-512 · HTTP 200 ✅ |

</div>

---

## 📊 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ashu-cloud&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB&text_color=C9D1D9" height="165" alt="GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ashu-cloud&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9" height="165" alt="Top Languages" />
</div>

<div align="center">
  <img src="https://streak-stats.demolab.com?user=ashu-cloud&theme=tokyonight&hide_border=true&background=0D1117&ring=58A6FF&fire=FF7B54&currStreakLabel=C9D1D9" alt="GitHub Streak" />
</div>

---

## 📬 Let's Talk

I'm actively looking for **paid software engineering internships** in backend, full-stack, or fintech roles. If you're building something interesting and need someone who ships production-grade code — let's connect.

<div align="center">

**ashupanchal8360@gmail.com** · [LinkedIn](https://www.linkedin.com/in/ashu-panchal-24b5bb189/) · [GitHub](https://github.com/ashu-cloud)

![Profile Views](https://komarev.com/ghpvc/?username=ashu-cloud&style=for-the-badge&color=58A6FF&label=PROFILE+VIEWS)

</div>
