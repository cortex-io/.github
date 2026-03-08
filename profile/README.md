<div align="center">

# Cortex

**An AI-powered autonomous DevOps platform built on K3s.**

Cortex was a multi-agent system for autonomous infrastructure management — master-worker agents, neural routing, self-healing daemons, and a full observability pipeline.

---

> **This project is archived.** Cortex is no longer under active development. What you see is what you get — explore freely, but no new features or fixes are planned.

---

</div>

## Repositories

| Repo | Description |
|------|-------------|
| [cortex](https://github.com/cortex-io/cortex) | Core platform — multi-agent orchestration, observability pipeline, daemons |
| [cortex-platform](https://github.com/cortex-io/cortex-platform) | Monorepo — services, MCP servers, shared libraries |
| [cortex-gitops](https://github.com/cortex-io/cortex-gitops) | GitOps manifests — ArgoCD-managed K3s deployments |
| [cortex-k3s](https://github.com/cortex-io/cortex-k3s) | K3s cluster docs — Wazuh, KEDA autoscaling, monitoring |
| [cortex-layer-stack](https://github.com/cortex-io/cortex-layer-stack) | Helm chart — scale-to-zero AI service stacks with distillation |
| [cortex-docs](https://github.com/cortex-io/cortex-docs) | Knowledge base — Obsidian vault, architecture decisions |
| [cortex-construction-hq](https://github.com/cortex-io/cortex-construction-hq) | Project management — roadmap, phase tracking, metrics |
| [infrastructure-docs](https://github.com/cortex-io/infrastructure-docs) | Homelab infrastructure documentation |

## Architecture

```
                    ┌─────────────────────────────────────────┐
                    │           Cortex Prime (Meta)           │
                    └──────────────────┬──────────────────────┘
                                       │
                    ┌──────────────────┴──────────────────────┐
                    │              COO Orchestrator            │
                    └──┬─────┬─────┬──────┬──────┬───────────┘
                       │     │     │      │      │
                ┌──────┴┐ ┌──┴──┐ ┌┴────┐ ┌┴───┐ ┌┴────┐
                │Coord. │ │Dev  │ │Sec  │ │Inv │ │CI/CD│
                │Master │ │Master│ │Master│ │Master│ │Master│
                └───┬───┘ └──┬──┘ └──┬──┘ └──┬──┘ └──┬──┘
                    │        │       │       │       │
               Workers   Workers  Workers  Workers  Workers
```

<div align="center">
<sub>Built with Claude, deployed on K3s, managed by ArgoCD.</sub>
</div>
