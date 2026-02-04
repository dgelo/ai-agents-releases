<p align="center">
  <h1 align="center">🤖 AI Agent Management System</h1>
  <p align="center">
    <strong>Enterprise platform for autonomous AI agents</strong>
  </p>
  <p align="center">
    <a href="#-features">Features</a> •
    <a href="#-quick-start">Quick Start</a> •
    <a href="#-documentation">Documentation</a> •
    <a href="#-architecture">Architecture</a>
  </p>
</p>

---

## ✨ Features

| | |
|---|---|
| 🧠 **Autonomous Agents** | Create and manage AI agents that execute tasks from natural language instructions |
| 🔌 **Plugin System** | Extend functionality with Rust, Python, WebAssembly, or MCP plugins |
| 📊 **Real-time Monitoring** | Track agent execution, logs, and performance metrics |
| 🔐 **Enterprise Security** | Role-based access control, SSO integration, audit logging |
| 🌐 **Modern Web UI** | Responsive React dashboard with real-time updates |
| 📡 **REST & WebSocket API** | Full-featured API with OpenAPI documentation |

---

## 🚀 Quick Start

### Prerequisites

- 🦀 Rust 1.75+
- 📦 Bun 1.0+ (or Node.js 18+)
- 🗄️ SQLite 3.35+

### Run Locally

```bash
# Backend
cargo run --release

# Frontend (separate terminal)
cd ui && bun install && bun run dev
```

### Docker

```bash
docker compose up -d
```

---

## 📚 Documentation

| Resource | Description |
|----------|-------------|
| 📖 [Getting Started](docs/guides/getting-started/overview.md) | First steps and setup guide |
| 🏗️ [Architecture](docs/guides/getting-started/architecture.md) | System design overview |
| 🔧 [API Reference](docs/system/api/reference.md) | REST API documentation |
| 🔌 [Plugin Development](docs/guides/developer/plugin-development.md) | Build custom plugins |
| ⚙️ [Configuration](docs/system/operations/configuration.md) | Server configuration options |
| 🚢 [Deployment](docs/system/operations/deployment.md) | Production deployment guide |

---

## 🏛️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        Web UI (React)                       │
└─────────────────────────┬───────────────────────────────────┘
                          │ REST / WebSocket
┌─────────────────────────▼───────────────────────────────────┐
│                     API Server (Actix)                      │
├─────────────────────────────────────────────────────────────┤
│  Auth  │  Agents  │  Tasks  │  Plugins  │  Integrations    │
└────────┴──────────┴─────────┴───────────┴───────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                    Core Engine (Rust)                       │
├─────────────────────────────────────────────────────────────┤
│  Task Executor  │  LLM Integration  │  Plugin Runtime       │
└─────────────────┴───────────────────┴───────────────────────┘
                          │
┌─────────────────────────▼───────────────────────────────────┐
│                   Storage (SQLite)                          │
└─────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Backend** | Rust, Actix-web, SQLite |
| **Frontend** | React 19, TypeScript, TailwindCSS |
| **Plugins** | Rust (native), Python, WebAssembly, MCP |
| **DevOps** | Docker, GitHub Actions |

---

## 📄 License

MIT
