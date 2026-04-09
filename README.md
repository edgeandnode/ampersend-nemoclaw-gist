# ampersend x NeMo Claw — Quick Reference

## What is this?

ampersend adds an **economic control layer** to NVIDIA NeMo Claw agents — enabling payments, budgets, and spend observability for enterprise agent workflows.

> "Stripe + Guardrails + Observability" for agent economies

## The Gap

NeMo Claw agents can reason, orchestrate, and stay safe — but they can't natively handle:

- **How much** to spend
- **Who** to pay
- **When** to stop spending

ampersend solves this.

## How It Works

```
Agent (NeMo/Claw) → calls paid API
API returns 402 Payment Required
ampersend checks policy (budget / allowlist) → signs payment
Request retried with payment → API executes → result returned
```

## Built On Open Standards

| Standard | Purpose |
|----------|---------|
| [x402 (Coinbase)](https://github.com/coinbase/x402) | Payments |
| [A2A (Google)](https://github.com/google-agentic-commerce/a2a-x402) | Agent-to-agent communication |
| [MCP](https://modelcontextprotocol.io/) | Tool/API execution |

## Integration Points

- **Guardrails + Economic Policies** — max spend per task/day, allowed vendors, escalation on high-cost actions
- **Tool Usage (MCP/APIs)** — native pay-per-use, no custom billing logic
- **Multi-Agent Payments** — agent-to-agent payments, service monetization
- **Observability** — real-time dashboards, spend tracking, policy enforcement logs

## Links

- [ampersend overview](https://www.ampersend.ai/skill.md)
- [Full docs](https://docs.ampersend.ai/)
- [ampersend SDK](https://github.com/ampersend-ai/ampersend-sdk)
- [Demo repo](https://github.com/edgeandnode/ampersend-nemoclaw)
- [Loom walkthrough](https://www.loom.com/share/a4be92f174c7441c86032f64745f55fb)

## TL;DR

| Layer | Solves |
|-------|--------|
| NeMo | Reasoning + orchestration |
| Guardrails | Safety + constraints |
| ampersend | Payments + economic control |

**Together = production-ready autonomous agents**
