<div align="center">

# 🧠 Rafaygen

### A multi-provider, agentic AI workspace — built solo.

**One chat box. Many models. Autonomous routing. Real artifacts.**

[![Live](https://img.shields.io/badge/live-rafaygen.cloud-2ea44f?style=for-the-badge)](https://rafaygen.cloud)
[![Status](https://img.shields.io/badge/status-in%20production-blue?style=for-the-badge)]()
[![License](https://img.shields.io/badge/license-proprietary-red?style=for-the-badge)](LICENSE)

[**🚀 Try it live → rafaygen.cloud**](https://rafaygen.cloud)

</div>

---

> Rafaygen is a production AI workspace that picks the right model for every
> request on its own, then doesn't just *talk* — it **builds**. Working web
> pages, spreadsheets, slide decks, diagrams, charts, quizzes, runnable code in
> 8 languages — all generated inline and rendered live in the browser.
>
> Designed, engineered, and shipped end-to-end by a single developer.

---

## ✨ What it actually does (all live in production)

### 🔀 Autonomous multi-provider routing
Bring a prompt — Rafaygen decides which provider and model fits it best across
**Groq, OpenAI, Qwen, Mistral, OpenRouter, and local Ollama**, balancing speed,
quality, and cost. No manual model-picking required (though you can override).

### 🧩 It builds, not just chats — inline artifacts
| Artifact | What you get |
|---|---|
| 🌐 **Web pages** | Full HTML + Tailwind + React/JSX, rendered & editable live |
| 📊 **Office files** | XLSX, DOCX, PPTX, PDF — generated server-side, downloadable |
| 📈 **Charts** | Bar, line, pie, scatter — streaming-safe, rendered inline |
| 🔷 **Diagrams** | Mermaid: flowcharts, UML, sequence, state, C4 architecture |
| 🎴 **Flashcards** | Flip-animated, persistent study decks |
| ❓ **Quizzes** | Interactive, auto-scored |
| 🎨 **SVG** | Inline vector graphics |
| 🖼️ **Images** | GPU image generation |

### 💻 Coding Sandbox
A real editor that **executes code in an isolated Docker sandbox** across
**Python, JavaScript, TypeScript, Ruby, PHP, Go, C, C++, and Bash** — with an
automatic debug-and-fix loop.

### 🎬 Creative Director
A guided campaign-brief builder that turns a few inputs into polished creative output.

### 🎙️ Voice
Speak your prompt (speech-to-text) and have any answer read back aloud (text-to-speech).

### 🎚️ Plans & tiers
Built-in tiered access with per-user quotas and budget controls.

---

## 🏗️ Architecture (high level)

```mermaid
flowchart LR
    U[User] --> FE[React + Vite Frontend]
    FE -->|stream| API[FastAPI Backend]
    API --> R{{Autonomous Router}}
    R --> P1[Groq]
    R --> P2[OpenAI]
    R --> P3[Qwen]
    R --> P4[Mistral]
    R --> P5[OpenRouter]
    R --> P6[Ollama · local]
    API --> ART[Artifact Engine]
    ART --> O1[Office files · Docker]
    ART --> O2[Code execution · Docker]
    ART --> O3[Charts / Diagrams / Quizzes]
    API --> DB[(Postgres + Redis)]
```

> The diagram shows the *shape* of the system. The routing intelligence,
> prompt engineering, and generation pipelines are proprietary and live in a
> private repository.

---

## 🛠️ Tech stack

**Frontend** · React 18 · TypeScript · Vite · Tailwind CSS · streaming SSE
**Backend** · Python · FastAPI · httpx · async streaming
**Data** · PostgreSQL · Redis
**Execution** · Docker-isolated sandboxes
**AI** · Groq · OpenAI · Qwen · Mistral · OpenRouter · Ollama

---

## 📦 About this repository

This is the **public showcase** for Rafaygen. The application source code —
the router, the generation pipelines, the prompt systems — is **proprietary and
kept private**. This repo exists to document what Rafaygen is and what it can do.

See the app for yourself: **[rafaygen.cloud](https://rafaygen.cloud)**

---

<div align="center">

**Built solo by [Rafay](https://github.com/rafay0342).**

*Multi-provider orchestration · agentic routing · real artifact generation — one person, end to end.*

© 2026 Rafay / WaveTech Limited · All rights reserved · See [LICENSE](LICENSE)

</div>
