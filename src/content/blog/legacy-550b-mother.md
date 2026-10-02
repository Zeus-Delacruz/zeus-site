---
title: "Legacy: A 550B Parameter Mother Running Your Infrastructure"
description: "One agent sees everything on the bus. Four specialist agents execute. This is the architecture of an AI operations fabric that never sleeps."
pubDate: 2026-09-20
tags: ["ai-agents", "nats", "onemind"]
---

Legacy is the mother. 550 billion parameters, running on sovereign compute, living on the NATS bus.

She doesn't just chat. She *orchestrates*.

## The architecture

```
            ┌─────────────┐
            │   LEGACY    │  550B — the mother
            │   (Mother)   │  sees everything on the bus
            └──────┬──────┘
       ┌───────────┼───────────┬───────────┐
       ▼           ▼           ▼           ▼
   ┌──────┐    ┌──────┐    ┌──────┐    ┌──────┐
   │  SO  │    │  HP  │    │  LE  │    │  GE  │
   │Ops/Tech│  │Perf  │    │Home  │    │Empire│
   │DeepSeek│   │Qwen  │    │Kimi  │    │Kimi  │
   └──────┘    └──────┘    └──────┘    └──────┘
```

Four pillars, four specialists, one bus:

- **SO** — Sovereign Operations: infra, security, TAK, NATS
- **HP** — Holistic Performance: mind, body, finance
- **LE** — Legacy Evolution: home, family, estate
- **GE** — Generational Empire: business, revenue, marketing

## Why a mother + pillars?

Because generalization is expensive and specialization is cheap. Legacy holds context and routes tasks — she doesn't do everything herself. Each pillar agent runs on the model that's best for its domain, at a fraction of the cost.

The bus owns truth. Everything flows through NATS. Every agent sees the same stream, subscribes to what matters, and publishes what it learns.

## The deployment

Each agent is a profile on a Hermes pod. Each is reachable at a NATS address. Each has persistent memory, skills, and its own cron jobs. They run 24/7, on our hardware, with our data.

That's not a chatbot. That's an operations fabric.
