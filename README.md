# AngeL · NerTzhuLz

<p align="center">
  <strong>Real-time systems · Automation · DevOps · Protected AI tooling</strong><br/>
  Building software that makes state, evidence and operational boundaries visible.
</p>

<p align="center">
  <a href="https://github.com/NerTzhuLz/NerTzh"><img src="https://img.shields.io/badge/flagship-NerTzh-0ea5e9?style=for-the-badge" alt="NerTzh"/></a>
  <a href="https://devpost.com/software/nertzh"><img src="https://img.shields.io/badge/OpenAI-Build%20Week-8b5cf6?style=for-the-badge" alt="OpenAI Build Week"/></a>
  <a href="https://github.com/NerThzBottZq"><img src="https://img.shields.io/badge/org-NerThzBottZq-22c55e?style=for-the-badge" alt="NerThzBottZq"/></a>
</p>

## At a glance

| Area | What I build |
| --- | --- |
| Real-time engineering | Market data, event pipelines, reconciliation and stateful services |
| Backend & DevOps | Python, FastAPI, PostgreSQL, Docker, runbooks and health checks |
| AI-assisted development | Explicit GPT-5.6/Codex boundaries, local context and reproducible evidence |
| Automation | Discord/community tooling, APIs and operational workflows |
| Quality | Small measurable fixes, tests, audit trails and safe demo environments |

## Flagship: NerTzh Metrics Control Plane

<a href="https://github.com/NerTzhuLz/NerTzh"><img align="right" width="360" src="https://github.com/NerTzhuLz/NerTzh/raw/main/assets/branding/logo.png" alt="NerTzh"/></a>

An evidence-first local control plane for Bybit spot metrics, Context Bridge
state and optional protected GPT-5.6/Codex-assisted analysis.

- FastAPI judge surface on `:8081` with a responsive monitoring UI.
- Optional attended Bybit demo engine isolated on `:8082`.
- PostgreSQL for engine state; DuckDB + Markdown for local context.
- Read-only by default; no automatic model calls or live execution.
- Reconciliation across market, database and exchange state.

**[Open the repository →](https://github.com/NerTzhuLz/NerTzh)** ·
**[Watch the Build Week release →](https://github.com/NerTzhuLz/NerTzh/releases/tag/v0.1.0-build-week)** ·
**[Read the Devpost entry →](https://devpost.com/software/nertzh)**

## System design

```mermaid
flowchart LR
  M[Market data] --> E[Optional attended engine]
  E --> P[(PostgreSQL)]
  P --> V[FastAPI control plane]
  C[Context Bridge\nDuckDB + Markdown] --> V
  V --> U[Judge-facing UI]
  V -. protected request .-> G[GPT-5.6 / Codex]
```

## Selected work

- **Trading infrastructure:** NerTzh, Adjudicator/Bybit research, TSM exchange
  formulas and state-reconciliation experiments.
- **Developer platforms:** FastAPI services, Python automation and local agent
  tooling.
- **Community automation:** Discord bots and operational tools dating back to
  2020.
- **Organization:** [NerThzBottZq](https://github.com/NerThzBottZq) for shared
  experiments and developer tooling.

Private or historical projects remain private until their dependencies,
licenses, credentials and reproducibility are reviewed.

## Engineering principles

1. Reconcile market, database and exchange state before acting.
2. Prefer a small, measurable correction over a large rewrite.
3. Keep credentials and private community data out of public repositories.
4. Make automation observable, attended and reversible.
5. Document the boundary between evidence, inference and execution.

## Technical surface

Representative technologies and public code surfaces from the active systems:

| Layer | Technologies / APIs |
| --- | --- |
| Languages | Python, SQL, JavaScript/TypeScript, HTML/CSS, Shell |
| Backend | FastAPI, Uvicorn, aiohttp, Pydantic, SQLAlchemy |
| Storage | PostgreSQL, DuckDB, JSON/JSONL, SQL migrations |
| Market connectivity | Bybit V5 REST, WebSocket orderbook/trades, HMAC signing, retry and reconciliation |
| Operations | Docker Compose, Make, systemd diagnostics, health checks, GitHub Actions, FFmpeg/Playwright |
| AI tooling | Codex, GPT-5.6 protected routes, Context Bridge, MCP, Qwen web/desktop experiments |
| Frontend | Native responsive HTML/CSS/JS, Chart.js, SVG/canvas visualizations |

Representative classes, functions and routes include `BybitV5Client`,
`BybitMcpSession`, `ConfigSettings`, `MarketData`, `Orderbook`, `Trade`,
`MetricSnapshot`, `BalanceSnapshot`, `ThresholdSnapshot`, `GPTClient`,
`MLPrediction`, `ChatIn`, `agent_context`, `bridge_status`, `agent_chat`,
`build_spot_order_body`, `create_order`, `cancel_order`, `amend_order`,
`order_realtime`, `order_history`, `get_open_orders`, `train_from_rows`,
`predict`, `compute_indicators`, and `combined_from_weights`.

### Nautilus Trader — evaluation track

Nautilus Trader is **not installed or referenced in the current `_Metrics_`
runtime**. It is an evaluation target for adapting the existing metrics and
reconciliation layer to a more formal event-driven trading architecture. The
intended study areas are adapters, `Actor`/`Strategy` lifecycle, data and order
events, execution clients, and backtest/live parity. No Nautilus production or
performance claim is made until a dedicated prototype is implemented and
tested.

## Contact and links

- [GitHub organization](https://github.com/NerThzBottZq)
- [NerTzh documentation](https://github.com/NerTzhuLz/NerTzh/tree/main/docs)
- [Build Week project](https://devpost.com/software/nertzh)
