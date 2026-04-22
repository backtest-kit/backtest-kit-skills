<img src="https://github.com/tripolskypetr/backtest-kit/raw/refs/heads/master/assets/decart.svg" height="55px" align="right">

# 🧿 backtest-kit-skills

> **Claude Code skill and Mintlify documentation source for the backtest-kit framework** — AI-assisted strategy writing, debugging help, and full API reference in one place.

![screenshot](https://raw.githubusercontent.com/tripolskypetr/backtest-kit/HEAD/assets/screenshots/screenshot16.png)

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/tripolskypetr/backtest-kit)
[![npm](https://img.shields.io/npm/v/backtest-kit.svg?style=flat-square)](https://npmjs.org/package/backtest-kit)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue)]()
[![License](https://img.shields.io/npm/l/backtest-kit.svg)](https://github.com/tripolskypetr/backtest-kit/blob/master/LICENSE)

---

## 🤖 Claude Code Skill

The `skills/backtest-kit/` folder (installed under `~/.claude/skills/backtest-kit/`) is a Claude Code agent skill that provides:

- **Strategy generation** — complete TypeScript files with all schema registrations and runner setup
- **Debugging help** — catches common mistakes (missing `await`, wrong TP/SL direction, top-level commit calls)
- **API reference** — all schemas, commit functions, event listeners, LLM integration, graph pipelines, and persistence adapters
- **Baseline recommendation** — always points to the `example/` folder when something isn't working

### Skill structure

```
skills/backtest-kit/
├── SKILL.md              # Core patterns, mental model, common mistakes
├── evals/
│   └── evals.json        # 8 test prompts with expected outputs
└── references/
    ├── schemas-api.md        # add*/override*/list*/get* for all schema types
    ├── runners.md            # Backtest / Live / Walker class methods
    ├── commit-functions.md   # Partial exits, trailing, breakeven, DCA
    ├── event-listeners.md    # All listeners + Once variants table
    ├── llm-integration.md    # json-inference, 12 providers, RAG/Memory
    ├── graph.md              # DAG indicator pipelines (@backtest-kit/graph)
    ├── cli-and-broker.md     # CLI flags, IBroker interface, broker adapter
    ├── global-config.md      # setConfig parameters and setLogger
    └── persistence.md        # Custom persistence adapters, crash recovery
```

---

## 📖 Documentation Source

The `source/` folder contains the Mintlify documentation site for backtest-kit. Run it locally with:

```bash
npm install -g mint
cd source
npm start
```

---

## 🧩 Ecosystem

| Package | Description |
|---------|-------------|
| [`backtest-kit`](https://www.npmjs.com/package/backtest-kit) | Core engine — temporal context via `AsyncLocalStorage`, exchange adapters, risk management, signal lifecycle |
| [`@backtest-kit/ui`](https://www.npmjs.com/package/@backtest-kit/ui) | Full-stack dashboard — candlestick charts, signal tracking, PnL analytics, trailing stops visualization |
| [`@backtest-kit/signals`](https://www.npmjs.com/package/@backtest-kit/signals) | 50+ technical indicators across 4 timeframes, order book depth, AI-ready markdown reports |
| [`@backtest-kit/ollama`](https://www.npmjs.com/package/@backtest-kit/ollama) | Multi-provider LLM wrapper (OpenAI, Claude, DeepSeek, Grok, Mistral, Ollama, 10+) with structured output |
| [`@backtest-kit/pinets`](https://www.npmjs.com/package/@backtest-kit/pinets) | Run TradingView Pine Script v5/v6 locally — 1:1 syntax, 60+ built-in indicators |
| [`@backtest-kit/graph`](https://www.npmjs.com/package/@backtest-kit/graph) | Typed DAG execution for multi-timeframe strategies — parallel source nodes, serializable to DB |
| [`@backtest-kit/cli`](https://www.npmjs.com/package/@backtest-kit/cli) | CLI for scaffolding AI agent trading projects with `CLAUDE.md` skill contracts |

---

## 🔗 Links

- 📖 [Documentation](https://backtest-kit.github.io/documents/article_07_ai_news_trading_signals.html)
- 💻 [GitHub Repository](https://github.com/tripolskypetr/backtest-kit)
- 🎯 [Reference Implementation](https://github.com/tripolskypetr/backtest-kit/tree/master/example)
- 🤖 [DeepWiki](https://deepwiki.com/tripolskypetr/backtest-kit)

---

<sub>MIT © <a href="https://github.com/tripolskypetr">tripolskypetr</a></sub>
