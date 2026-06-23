[← back to profile](https://github.com/HiroAlleyCat)

# Portfolio — Zach (HiroAlleyCat)

Systems administrator moving into applied AI. I build the **systems that let LLMs do real, bounded work** against live infrastructure, and the **signal-processing tooling** that turns physical-world RF into structured data. Production-minded throughout — gated CI/CD, supply-chain security, and human-gated autonomy. Self-hosted on infrastructure I own.

---

### 📦 Yggdrasil AI Labs — open-source signal pipeline

Public · MIT · every repo on a gated CI/CD pipeline (tests → SonarCloud SAST → Snyk SCA → release).
A family of small, single-purpose tools that **capture → normalize → transport** real-world RF into one clean JSON schema.

| Repo | What it does |
|---|---|
| [**Muninn**](https://github.com/Yggdrasil-AI-labs/adsb-to-wdgwars) | Normalizes 13 ADS-B receiver dialects into one JSON schema · Python CLI **and** in-browser (Pyodide/WASM) |
| [**Heimdall**](https://github.com/Yggdrasil-AI-labs/meshcore-to-wdgwars) | LoRa / MeshCore mesh telemetry → normalized records (mirrors Muninn's design) |
| [**wigle-to-wdgwars**](https://github.com/Yggdrasil-AI-labs/wigle-to-wdgwars) | WiGLE Wi-Fi / BLE wardrive CSVs → structured records |
| [**gungnir**](https://github.com/Yggdrasil-AI-labs/gungnir) | Shared HMAC-signed transport client — integrity, retry, cooldown, silent-drop detection |
| [**wdgwars-api-tester**](https://github.com/Yggdrasil-AI-labs/wdgwars-api-tester) | Contract-testing harness for an undocumented HTTP API — probe quorum + 404 fingerprinting |

→ **[github.com/Yggdrasil-AI-labs](https://github.com/Yggdrasil-AI-labs)**

### 🧩 Engineering practices (visible in the public repos)

- **One transport, many tools** — signing / retry / back-pressure live once in `gungnir`; the tools stay small and focused.
- **Local-first by architecture** — browser builds process data in-page (Pyodide/WASM); no server sees raw input.
- **Resilient clients** — chunking around upstream timeouts, 429 back-pressure, cooldown persistence, "accepted ≠ delivered" detection.
- **Tests as the contract** — when an API is undocumented, the test harness is the spec.
- **Production discipline on a homelab** — threat models (SECURITY.md), gated merges, SAST + SCA, branch protection, versioned releases.

### 🤖 Agentic AI operations (self-hosted)

Local LLMs wired into infrastructure through MCP tool surfaces — bounded actions with structured state, audit trails, and human gates:

- a **self-healing operations loop** — monitors the fleet and applies whitelisted remediations (dry-run → live, journaled)
- a **research / synthesis pipeline** — cost-gated, routes local-vs-cloud, multi-model fallback
- a **control plane** — exposes infrastructure as typed MCP tools for safe agent operation
- a **memory layer** — retrieval over a local knowledge base that agents read and write back
- **assistant interfaces** — budget-capped, allowlisted, shadow-mode before going live

*Guardrails designed before capabilities.*

### 🧠 Local models

Self-hosted via **Ollama** — I track the top of each major open-weight family:

![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![Llama](https://img.shields.io/badge/Llama_(Meta)-0866FF?style=flat-square) ![Qwen](https://img.shields.io/badge/Qwen_(Alibaba)-7C3AED?style=flat-square) ![Gemma](https://img.shields.io/badge/Gemma_(Google)-1A73E8?style=flat-square) ![Mistral](https://img.shields.io/badge/Mistral_%2F_Mixtral-FF7000?style=flat-square) ![Phi](https://img.shields.io/badge/Phi_(Microsoft)-00A4EF?style=flat-square) ![DeepSeek](https://img.shields.io/badge/DeepSeek-4D6BFE?style=flat-square)

### ☁️ Cloud models

Across agent workflows, tooling, and evaluation — the major frontier families:

![Claude](https://img.shields.io/badge/Claude_(Anthropic)-D97757?style=flat-square&logo=anthropic&logoColor=white) ![GPT](https://img.shields.io/badge/GPT_(OpenAI)-412991?style=flat-square&logo=openai&logoColor=white) ![Gemini](https://img.shields.io/badge/Gemini_(Google)-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) ![Grok](https://img.shields.io/badge/Grok_(xAI)-000000?style=flat-square)

### 🔭 Currently exploring

- **Edge AI** — small LLM agents on microcontrollers (ESP32 + MCP)
- **Cost-gated model routing** — local-vs-cloud selection by task and budget
- **Tighter human-in-the-loop autonomy** for operations agents

---

### 🛠️ Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white) ![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![SonarCloud](https://img.shields.io/badge/SonarCloud-F3702A?style=flat-square&logo=sonarqubecloud&logoColor=white) ![Snyk](https://img.shields.io/badge/Snyk-4C4A73?style=flat-square&logo=snyk&logoColor=white) ![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white)

### 🧭 Core skills

- **Agentic system design** — MCP tool surfaces, structured state, human-gated autonomy, blast-radius control
- **Local-first / vendor-agnostic AI** — Ollama, cost-gated model routing, privacy by architecture
- **Automation & operations** — Python, Bash, systemd, a Linux homelab at real uptime
- **DevSecOps** — gated CI/CD, SAST (SonarCloud) + SCA (Snyk), secret hygiene, branch protection
- **Data engineering** — SQLite/WAL, FastAPI services, MQTT event buses, retrieval over local knowledge
