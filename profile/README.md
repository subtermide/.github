<div align="center">

# SubTerm

### Cloud IDE with Real-Time Collaboration

[![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square)](LICENSE)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)](https://docker.com)
[![Node.js](https://img.shields.io/badge/Node.js-20-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-ff69b4?style=flat-square)](https://github.com/dipsubhro/subterm/pulls)

<br />

**Code from anywhere. Collaborate in real-time. Zero setup required.**

<br />

<img src="https://raw.githubusercontent.com/dipsubhro/subterm/main/preview.png" alt="SubTerm IDE Preview" width="100%" style="border-radius: 8px;" />

<br />
<br />

[Get Started](#quick-start) · [Documentation](https://github.com/dipsubhro/subterm/tree/main/docs) · [Report Bug](https://github.com/dipsubhro/subterm/issues) · [Request Feature](https://github.com/dipsubhro/subterm/issues)

</div>

---

## Why SubTerm?

SubTerm is an open-source, browser-based IDE designed for developers who want a powerful coding environment without local setup headaches. Each session runs in an isolated Docker container, providing security and consistency across environments.

<table>
<tr>
<td width="50%">

### For Developers
- **Instant Environment** — Start coding in seconds
- **Full Terminal Access** — Complete bash shell with PTY
- **VS Code Experience** — Monaco editor with IntelliSense
- **GitHub Integration** — Clone repos with one click

</td>
<td width="50%">

### For Teams
- **Real-Time Collaboration** — Edit together, see cursors live
- **Session Sharing** — Invite teammates instantly
- **Isolated Workspaces** — Sandboxed containers per session
- **Self-Hostable** — Deploy on your infrastructure

</td>
</tr>
</table>

---

## Features

| | Feature | Description |
|:---:|---------|-------------|
| **Editor** | Monaco | VS Code engine with syntax highlighting for 20+ languages |
| **Terminal** | Full PTY | Complete bash shell with command history |
| **Collab** | Real-Time | CRDT-powered sync with live cursor tracking |
| **Security** | Sandboxed | Isolated Docker containers per session |
| **Import** | GitHub | Clone public repositories directly |
| **Share** | Instant | One-click workspace sharing |

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/dipsubhro/subterm.git && cd subterm

# Start services
cd gateway && docker compose up -d

# Run the client
cd ../client && pnpm install && pnpm dev
```

Open `http://localhost:5173` and start coding.

---

## Architecture

```
┌─────────────┐     ┌─────────────┐     ┌─────────────────────────┐
│   Browser   │────▶│   Gateway   │────▶│   Docker Containers     │
│   (React)   │     │   (Node.js) │     │   (Isolated Sessions)   │
└─────────────┘     └──────┬──────┘     └─────────────────────────┘
                           │
                    ┌──────▼──────┐
                    │    Redis    │
                    │  (Sessions) │
                    └─────────────┘
```

---

## Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Node.js-20-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis" />
  <img src="https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socket.io&logoColor=white" alt="Socket.IO" />
  <img src="https://img.shields.io/badge/Yjs-CRDT-6366f1?style=for-the-badge" alt="Yjs" />
</p>

---

## Documentation

| Document | Description |
|----------|-------------|
| [**Architecture**](https://github.com/dipsubhro/subterm/blob/main/docs/architecture.md) | System design, services, and data flow |
| [**Deployment**](https://github.com/dipsubhro/subterm/blob/main/docs/deployment.md) | Production setup and configuration |
| [**Collaboration**](https://github.com/dipsubhro/subterm/blob/main/docs/collaboration.md) | Real-time editing with Yjs |
| [**Execution Engine**](https://github.com/dipsubhro/subterm/blob/main/docs/execution-engine.md) | Container orchestration and PTY |

---

## Contributing

Contributions are welcome! Whether it's bug fixes, new features, or documentation improvements.

1. Fork the repository
2. Create your branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## License

Distributed under the MIT License. See `LICENSE` for more information.

---

<div align="center">

**[Repository](https://github.com/dipsubhro/subterm)** · **[Issues](https://github.com/dipsubhro/subterm/issues)** · **[Discussions](https://github.com/dipsubhro/subterm/discussions)**

<sub>Built with passion by <a href="https://github.com/dipsubhro">@dipsubhro</a></sub>

</div>
