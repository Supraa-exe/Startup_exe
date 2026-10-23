# Startup_exe — VenturePulse AI Ecosystem

> **Autonomous multi-agent startup stress-testing, market simulation, and founder intelligence platform.**

`Startup_exe` is the unified parent repository linking the **VenturePulse AI frontend/orchestrator** (`Startup_Analyser`) and the **MiroFish simulation engine** (`mirofish-engine`).

---

## 🏗 Repository Architecture

This repository uses **Git Submodules** to organize its core services:

| Submodule | Description | Technology Stack | Repository |
| :--- | :--- | :--- | :--- |
| [`Startup_Analyser`](./Startup_Analyser) | Next.js 15 interactive dashboard, Gemma 4 analysis engine, multi-agent war room, SVG charts, and MongoDB archive | Next.js 15, React 19, TypeScript, Tailwind CSS | [Supraa-exe/Startup_Analyser](https://github.com/Supraa-exe/Startup_Analyser) |
| [`mirofish-engine`](./mirofish-engine) | Multi-agent sandbox simulation engine with GraphRAG, Zep graph memory, and LLM swarm dynamics | Python 3.10+, FastAPI, Zep, OpenAI SDK | [666ghj/MiroFish](https://github.com/666ghj/MiroFish) |

---

## 🚀 Cloning the Repository

Because this repository uses submodules, clone it with the `--recurse-submodules` flag:

```bash
git clone --recurse-submodules https://github.com/Supraa-exe/Startup_exe.git
cd Startup_exe
```

If you cloned without `--recurse-submodules`, initialize and fetch submodules with:

```bash
git submodule update --init --recursive
```

To update all submodules to their latest remote commits in the future:

```bash
git submodule update --remote --merge
```

---

## ⚡ Quick Start

### 1. Startup_Analyser (Frontend & Orchestrator)

```bash
cd Startup_Analyser

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env.local
# Edit .env.local with your API keys (Gemini, OpenAI, MongoDB, etc.)

# Start the development server
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) or [http://localhost:3001](http://localhost:3001) in your browser.

### 2. mirofish-engine (Backend Engine)

```bash
cd mirofish-engine

# Set up virtual environment
python -m venv venv
# On Windows:
.\venv\Scripts\activate
# On Linux/macOS:
# source venv/bin/activate

# Install dependencies
pip install -r backend/requirements.txt

# Configure environment variables
cp .env.example .env
# Edit .env with your LLM & Zep API keys

# Launch backend
python -m backend.main
```

---

## 🛡 Security & Environment

- Sensitive credentials (`.env`, `.env.local`, `.data/`, etc.) are ignored by `.gitignore` across all repositories.
- Use `.env.example` templates in each submodule to set up your local development environment.
- Never commit active API keys or production database credentials to Git.

---

## 📜 License

Refer to the individual licenses inside each submodule directory:
- `Startup_Analyser`: MIT
- `mirofish-engine`: Apache-2.0
