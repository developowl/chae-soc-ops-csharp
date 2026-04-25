<div align="center">

# 🎱 Soc Ops

### Social Bingo for in-person mixers — powered by Blazor WebAssembly & GitHub Copilot Agent Mode

[![.NET 10](https://img.shields.io/badge/.NET-10-512BD4?logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/download/dotnet/10.0)
[![Blazor WASM](https://img.shields.io/badge/Blazor-WebAssembly-7B2FBE?logo=blazor&logoColor=white)](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-24292e?logo=github&logoColor=white)](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

[🎮 **Play the Game**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/) &nbsp;•&nbsp; [📚 **Lab Guide**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/) &nbsp;•&nbsp; 🌐 [Português (BR)](README.pt_BR.md) | [Español](README.es.md)

</div>

---

## What is Soc Ops?

**Soc Ops** is a real-time Social Bingo game designed for conferences, workshops, and team mixers. Players find people who match fun questions — first to get **5 in a row** wins!

But it's more than a game: this repo is a **hands-on workshop** that teaches you how to build with **VS Code Agent Mode** and **GitHub Copilot**. Over ~1 hour you'll go from a bare-bones app to a polished, feature-rich experience guided by AI.

```
Find someone who...  →  mark their square  →  BINGO!
```

---

## 🎯 What You'll Build & Learn

| # | Skill | What you do |
|---|-------|-------------|
| 1 | **Context Engineering** | Teach AI your codebase with custom instructions |
| 2 | **Agentic Primitives** | Background agents, cloud agents, custom workflows |
| 3 | **Design-First Dev** | Let AI iterate on UI while you steer the vision |
| 4 | **Test-Driven Dev** | Ship new features with TDD agents (Red → Green → Refactor) |

---

## 📚 Lab Guide

| Part | Title | Time |
|------|-------|------|
| [**00**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=00-overview) | Overview & Checklist | — |
| [**01**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=01-setup) | Setup & Context Engineering | 15 min |
| [**02**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=02-design) | Design-First Frontend | 15 min |
| [**03**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=03-quiz-master) | Custom Quiz Master | 10 min |
| [**04**](https://dotnet-presentations.github.io/vscode-github-copilot-agent-lab/docs/step.html?step=04-multi-agent) | Multi-Agent Development | 20 min |

> 📝 Lab guides are also available in the [`workshop/`](workshop/) folder for offline reading.

---

## 🚀 Quick Start

### Prerequisites

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) or higher
- VS Code **v1.107+** with [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)

### Run locally

```bash
cd SocOps
dotnet run
```

Open [http://localhost:5166](http://localhost:5166) and start playing!

### Build

```bash
cd SocOps
dotnet build
```

### Open in GitHub Codespaces ☁️

The fastest way to get started — no local setup required:

1. Click **Use this template** → **Create a new repository**
2. Open your new repo → **Code** → **Codespaces** → **Create codespace on main**
3. Wait for the devcontainer to finish, then run:
   ```bash
   cd SocOps && dotnet run
   ```

---

## 🏗️ Architecture

```
SocOps/
├── Pages/Home.razor          # Main game page
├── Components/               # Bingo board, cards, modals
├── Services/
│   ├── BingoGameService.cs   # UI state & transitions
│   └── BingoLogicService.cs  # Game rules (wins, marking)
├── Models/                   # Domain types
└── Data/Questions.cs         # Bingo question bank
```

Blazor WASM runs entirely in the browser — no server round-trips during gameplay. Deploys automatically to **GitHub Pages** on every push to `main`.

---

## 🤝 Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) and review our [Code of Conduct](CODE_OF_CONDUCT.md) before opening a pull request.
