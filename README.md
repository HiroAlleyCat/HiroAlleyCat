# Zach — systems admin → applied AI engineer

> Self-hosted, vendor-agnostic AI ops & SIGINT/signals tooling — shipped with gated CI/CD.<br>It runs on my own hardware. The cloud is optional, not load-bearing.

I came up through systems administration and moved into applied AI: building the **systems that let LLMs do real, bounded work** against live infrastructure, and the **signal-capture tooling** that turns the physical world into structured data.

---

### 📡 Yggdrasil AI Labs — the feeder family

Public · MIT · every repo on a gated CI pipeline (tests → SonarCloud → Snyk → release).
Small tools that **capture → convert → transport** real-world RF into one clean JSON shape.

| Repo | What it does |
|---|---|
| [**Muninn**](https://github.com/Yggdrasil-AI-labs/adsb-to-wdgwars) | 13 ADS-B aircraft dialects → one JSON · CLI **and** in-browser (Pyodide) |
| [**Heimdall**](https://github.com/Yggdrasil-AI-labs/meshcore-to-wdgwars) | LoRa / MeshCore mesh feeder — Muninn's mirror, different parser |
| [**wigle-to-wdgwars**](https://github.com/Yggdrasil-AI-labs/wigle-to-wdgwars) | WiGLE Wi-Fi / BLE wardrive CSVs → leaderboard |
| [**gungnir**](https://github.com/Yggdrasil-AI-labs/gungnir) | shared HMAC-signed transport (retry, cooldown, silent-drop detection) |
| [**wdgwars-api-tester**](https://github.com/Yggdrasil-AI-labs/wdgwars-api-tester) | a living spec for an undocumented API — probe quorum + 404 fingerprinting |

→ **[github.com/Yggdrasil-AI-labs](https://github.com/Yggdrasil-AI-labs)**

### 🧩 Engineering themes (all visible in the public repos)

- **One transport, many feeders** — signing / retry / back-pressure live once in `gungnir`; the feeders stay tiny.
- **Local-first by architecture** — browser builds convert captures in-page (Pyodide/WASM); no server sees raw data.
- **Built for an unreliable upstream** — 10k-row chunking around Cloudflare 524s, 429 back-pressure, cooldown, "accepted ≠ delivered" silent-drop detection.
- **The test suite is the spec** — when an API has no docs, the probe tool becomes the contract.
- **Homelab treated like production** — SECURITY.md threat models, gated merges, SAST + SCA, versioned releases.

### 🤖 Agentic ops (private lab)

Self-hosted agentic systems: local LLMs (Ollama) + MCP tool surfaces, structured state, audit trails, and **human-gated autonomy** — bounded actions against real infrastructure, guardrail designed before the capability. *(Details on request.)*

---

### 🛠️ Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![SonarCloud](https://img.shields.io/badge/SonarCloud-F3702A?style=flat-square&logo=sonarqubecloud&logoColor=white) ![Snyk](https://img.shields.io/badge/Snyk-4C4A73?style=flat-square&logo=snyk&logoColor=white) ![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat-square&logo=tailscale&logoColor=white)

### 🧭 Skills I reach for

- **Agentic system design** — MCP tool surfaces, structured state, human-gated autonomy, blast-radius control
- **Local-first / vendor-agnostic AI** — Ollama, cost-gated model routing, privacy by architecture
- **Automation & ops** — Python, Bash, systemd, a Linux homelab at real uptime
- **DevSecOps** — gated CI/CD, SAST (SonarCloud) + SCA (Snyk), secret hygiene, branch protection
- **Data plumbing** — SQLite/WAL, FastAPI services, MQTT event buses, RAG over local knowledge

---
<sub>Norse-named tools · signals turned into data · AI that earns its keep on hardware I own.</sub>
