# Hi there 👋

I'm **Ramchandra Chawla**, a software developer focused on building reliable AI-integrated systems — from LLM observability infrastructure to real-time verification pipelines and ML-based prediction engines. I enjoy turning complex engineering problems into clean, well-structured solutions.

This repository is a collection of my projects, research work, and applied systems across:

- Artificial Intelligence 🤖
- Backend Engineering & API Systems 🧱
- Machine Learning 🧠
- Language Processing & Compliance Logic 📊

Feel free to explore my projects or reach out if you would like to collaborate.

---

## 🌟 Recently Worked On / Currently Working On

### 1. AI Agent Auditor — Real-Time LLM Observability Platform *(In Progress)*

A real-time monitoring and auditing platform that intercepts, logs, analyzes, and scores the behavior of any LLM-powered agent pipeline — flagging unsafe decisions, cost inefficiencies, hallucinations, and compliance violations. Fully open-source stack, no paid APIs required beyond the LLM being audited.

**Key Features and Technologies:**
- **Behavior Interception:** Hooks into agent pipelines to capture inputs, outputs, tool calls, and intermediate reasoning steps without modifying agent code.
- **Risk Scoring Engine:** Deterministic scoring system that evaluates each agent action against safety, cost, and compliance thresholds in real time.
- **Hallucination Detection:** Implements retrieval-based cross-checking to flag factually inconsistent or ungrounded model outputs.
- **Audit Logging:** Structured event logs with metadata for reproducible post-hoc analysis and debugging.
- **Dashboard Interface:** Live feed of agent sessions with risk scores, flag summaries, and cost metrics.

**Tech Stack:** Python, FastAPI, SQLite/DuckDB, LLM APIs

---

### 2. Message Rewriter v3 — Compliance-Grade Language Processing Engine

A professional message rewriting engine with deterministic risk scoring and structured compliance checks — built for reliability and auditability, not just fluency.

**Key Features and Technologies:**
- **Risk Scoring Logic:** Developed a reproducible, rule-based scoring system that evaluates rewritten messages against compliance criteria with no randomness in outputs.
- **Structured Compliance Checks:** Defined layered validation rules for tone, content policy, and domain-specific constraints.
- **Deterministic Output:** Engineered the pipeline to produce consistent, explainable results for any given input — critical for production compliance systems.

**Tech Stack:** TypeScript, NLP, Rule-Based Scoring

---

### 3. Soccer Match Prediction — ML-Based Outcome Modeling

A machine learning project to predict soccer match outcomes using data-driven feature engineering and model experimentation.

**Key Features and Technologies:**
- **Feature Engineering:** Designed match-level features including form metrics, head-to-head statistics, and home/away differentials.
- **Model Experimentation:** Evaluated multiple classification approaches to identify the best-performing model configuration.
- **Prediction Accuracy:** Iterated on feature selection and model parameters to improve accuracy on held-out match data.

**Tech Stack:** Python, Scikit-learn, Pandas, Jupyter

---

### 4. PitchIQ — AI-Native Cricket Decision Intelligence Platform

An AI-powered decision platform for IPL/T20 franchises that generates explainable predicted playing XIs, collapse-risk alerts, and opposition intelligence from open ball-by-ball datasets.

**Key Features and Technologies:**
- **Explainable XI Prediction Engine:** Rules-based scoring engine across four model versions (`rules_v1` through `rules_v4_calibrated`), incorporating match context, toss awareness, venue/pitch profiles, opposition matchup weights, and overseas player caps — with per-player explanations surfaced in the UI.
- **Collapse-Risk Backtesting:** Calibrates predicted risk scores against historical model runs, computes Brier scores for accuracy measurement, and stores labeled match outcomes for audit.
- **Multi-Role Access Architecture:** Role-gated routes and dashboards for `TEAM_USER`, `ANALYST_USER`, and `LEAGUE_ADMIN` — each with scoped data access, quick actions, and landing page preferences persisted to the database.
- **Analytics & Scheduled Exports:** Collapse analytics drill-down with row expanders, trend charts, CSV export, and a scheduled export pipeline with webhook delivery, HMAC signing, and Resend email integration.
- **Supabase Backend:** Full migration from Prisma to Supabase with SQL-scaffolded schemas for squads, match outcomes, scheduled exports, and user preferences.

**Tech Stack:** TypeScript · Next.js · Supabase · Tailwind CSS · Resend

---

## ⚡ Hackathon Projects

Fast-built, high-pressure projects from competitive hackathons — focused on shipping real systems under time constraints.

---

### 🏆 [Collapse-Radar](https://github.com/Ramlols2604/Collapse-Radar) — Real-Time Sports Intelligence Platform *(Hackalytics @ Georgia Tech · February 2026)*

> Predicts short-term momentum collapse in international football using rolling event stream features and statistical modeling.

Transforms raw match event streams into minute-level risk probabilities and tactical decision insights — built end-to-end during a competitive hackathon.

**What we built in the time limit:**
- **Rolling Event Features:** Engineered instability metrics such as turnover burstiness and territory tilt to quantify momentum shifts in real time.
- **Time Series Validation:** Trained logistic regression models using TimeSeriesSplit to prevent temporal data leakage.
- **Change Point Detection:** Implemented CUSUM to detect structural shifts before risk spikes occur.
- **Counterfactual Simulations:** Designed nearest-neighbor simulations to estimate risk reduction under tactical adjustments.
- **Backend Infrastructure:** Built a FastAPI backend with DuckDB to serve real-time predictions efficiently, with a TypeScript frontend for live match visualization.

**Tech Stack:** Python · scikit-learn · FastAPI · DuckDB · TypeScript

---

### 🏆 [Predictive Compliance AI](https://github.com/Ramlols2604/predictive-compliance-ai) — Automated Compliance Risk Scoring *(LPL Financial Hackathon · February 2026)*

> A compliance risk scoring system that analyzes communications for policy violations, regulatory flags, and tone anomalies using AI-driven classification.

Built to demonstrate how compliance review workflows can be automated without sacrificing audit transparency — every decision is traceable.

**What we built in the time limit:**
- **Risk Classification Pipeline:** Structured multi-label classifier to flag messages across categories including tone violations, regulatory language, and policy breaches.
- **Audit Trail Generation:** Every scored message produces a structured log with decision rationale for post-hoc review.
- **API Layer:** REST API serving real-time compliance scores for integration into messaging or workflow platforms.
- **Threshold Configuration:** Configurable risk thresholds allowing teams to tune sensitivity without retraining the model.

**Tech Stack:** TypeScript · AI Classification · REST API · Compliance Logic

---

### 🏆 [Strata](https://github.com/Ramlols2604/strata-sustainability-ai) — Sustainability Intelligence Platform *(HooHacks · March 2026)*

> Five AI agents debate each other in real time to determine whether a neighborhood or company is genuinely improving — or just performing sustainability.

Most sustainability scores tell you where something stands today. STRATA scores the trajectory — and when agents disagree sharply, it flags that disagreement as actionable intelligence no rating agency produces.

**What we built in the time limit:**
- **Multi-Agent Debate Architecture:** Five specialized Gemini 2.5 Flash agents fire in parallel via `asyncio.gather()`, each reasoning through their own lens — Climate Resilience, Public Health, Urban Development, Equity Analyst, and a Devil's Advocate that challenges the highest-confidence claim with a cited counter-source.
- **Dual Mode — Neighborhood & Corporate:** Neighborhood mode detects green gentrification by cross-referencing every sustainability signal against Census rent trajectories. Corporate mode produces a no-expansion action list of carbon improvements requiring zero capex, ranked by impact-per-dollar with 90-day, 6-month, and 12-month tags.
- **Trajectory Verdicts + Dissent Scoring:** Outputs one of four verdicts — `IMPROVING`, `STAGNANT`, `DECLINING`, or `CONTESTED` — alongside a dissent score that quantifies how much to trust the verdict.
- **Real-Time Streaming Radar:** Results stream token-by-token over SSE to a live radar chart that updates as each agent finishes — built with Leaflet.js and Chart.js.
- **Local Computer Vision Pipeline:** NDVI vegetation index, green coverage, impervious surface ratio, and construction activity detection all run locally with OpenCV and rasterio — zero additional API cost.

**Tech Stack:** Python · FastAPI · Gemini 2.5 Flash · asyncio · SSE · OpenCV · SQLite · Redis · Leaflet.js · Chart.js · Railway · Vercel

---

### 🏆 [ProofPulse](https://github.com/Ramlols2604/proofpulse) — Real-Time Video Claim Verification *(HackNCState · February 2026)*

> Multimodal AI pipeline that verifies factual claims in live or recorded video content using retrieval-augmented generation and caching infrastructure.

Built under hackathon time constraints with a focus on end-to-end completeness — ingestion, retrieval, verification, and response in a single pipeline.

**What we built in the time limit:**
- **Multimodal Ingestion:** Extracted and timestamped claims from video transcripts for downstream verification.
- **Retrieval Pipeline:** Built a RAG pipeline to match claims against a curated knowledge base and web retrieval sources.
- **Caching Layer:** Designed a caching infrastructure to reduce redundant retrieval and improve response latency on repeated claims.
- **Speed Optimization:** Prioritized sub-second verification for real-time use cases through pipeline parallelization and efficient indexing.

**Tech Stack:** TypeScript · Multimodal AI · RAG · Vector Search

---

## 📚 I'm Currently Learning

- LLM observability, agent evaluation frameworks, and AI safety tooling
- Distributed backend systems and scalable API infrastructure
- Advanced feature engineering and time-series model validation

---

## 🤝 I'm Looking to Collaborate On

- AI agent monitoring, safety, and compliance tooling
- Backend systems that serve ML models or analytics pipelines
- Applied AI projects with measurable real-world impact

---

## 💬 Ask Me About

- Building deterministic scoring and compliance logic for language systems
- Designing RAG pipelines and retrieval infrastructure
- Real-time AI pipeline architecture
- FastAPI backend development

---

## 🛠️ Technologies & Tools

| Area | Tools |
|---|---|
| **Languages** | TypeScript · Python · Java · HTML |
| **AI / ML** | LLM Pipelines · RAG · Scikit-learn · Multimodal AI |
| **Backend** | FastAPI · REST APIs · System Design |
| **Data** | DuckDB · SQLite · Pandas |
| **Tooling** | Git · GitHub · VS Code |

---

## 🔭 Currently Looking For

Opportunities in **AI engineering**, **backend development**, and **ML systems** — particularly roles involving LLM infrastructure, applied AI tooling, or data-driven backend platforms.

---

## 📁 Other Work

### [Forage JPMC — Advanced Software Engineering](https://github.com/Ramlols2604/forage-midas)
> Industry-style tasks from the JPMorgan Chase Advanced SWE Forage program.

Practiced real-world software engineering fundamentals in a structured, industry-aligned environment — covering backend development, testing, and system design principles.

**Tech Stack:** Java

---

### [Recipe App](https://github.com/Ramlols2604/recipe)
> A full-stack Django web application for browsing, creating, and managing recipes with user profiles and authentication.

Built using the Django MVT pattern with SQLite, covering user profile management, recipe detail pages, and CRUD operations — a practical exercise in full-stack web development with Python.

**Tech Stack:** Python · Django · SQLite · HTML · CSS · JavaScript

---

## 🔗 Connect with Me

- **GitHub:** [github.com/Ramlols2604](https://github.com/Ramlols2604)
- **LinkedIn:** [https://www.linkedin.com/in/ramchandrachawla/]
- **Portfolio:** [https://ramchandrachawla-portfolio.vercel.app/]
