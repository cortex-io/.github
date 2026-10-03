<img src="https://raw.githubusercontent.com/cortex-io/.github/main/profile/banner.svg" width="100%" alt="Cortex: multi-agent AI infrastructure orchestration. Archived.">

> [!NOTE]
> **Cortex is archived.** It is no longer under active development and no fixes or features are planned. Everything here is kept as a working record: explore, fork and borrow freely.

## What Cortex was

An experiment in letting AI agents run DevOps end to end. **Cortex Prime** set direction, a **COO orchestrator** routed work, and **five master agents** each led a team of specialized workers: writing code and opening PRs, scanning for and fixing vulnerabilities, tracking assets, and running CI/CD. Nine background daemons kept it healthy, on budget and coordinated, and everything shipped to K3s through GitOps.

<img src="https://raw.githubusercontent.com/cortex-io/.github/main/profile/numbers.svg" width="100%" alt="5 master agents, 7 worker types, 9 daemons, 94% worker success rate, 200k tokens per day budget">

## How it was wired

<img src="https://raw.githubusercontent.com/cortex-io/.github/main/profile/architecture.svg" width="100%" alt="Cortex architecture: Prime, COO orchestrator, five master agents with their workers, infrastructure, and daemons">

Code flowed one way only: **code → container → registry → ArgoCD → K3s**. No manual `kubectl apply`; Git history was the audit trail.

## The exhibits

| | Repo | What's inside |
|---|---|---|
| 🧠 | [cortex](https://github.com/cortex-io/cortex) | The core: multi-agent orchestration, the observability pipeline, the daemons |
| 🧩 | [cortex-platform](https://github.com/cortex-io/cortex-platform) | Monorepo of services, MCP servers and shared libraries |
| 🚢 | [cortex-gitops](https://github.com/cortex-io/cortex-gitops) | ArgoCD-managed manifests for every K3s deployment |
| ☸️ | [cortex-k3s](https://github.com/cortex-io/cortex-k3s) | Cluster docs: Wazuh security, KEDA autoscaling, monitoring |
| 📚 | [cortex-docs](https://github.com/cortex-io/cortex-docs) | Obsidian knowledge base: architecture decisions and runbooks |
| 🏗️ | [cortex-construction-hq](https://github.com/cortex-io/cortex-construction-hq) | Roadmap, phase tracking and build-session logs |
| 🖥️ | [infrastructure-docs](https://github.com/cortex-io/infrastructure-docs) | The homelab underneath: Proxmox, K3s, networking |

**Stack:** TypeScript · Python · K3s · ArgoCD · Redis · PostgreSQL · Qdrant · Claude API · MCP · Elastic APM

## Still building

The builder behind Cortex is still at it:

- **[ry-ops](https://github.com/ry-ops)**: MCP servers for Proxmox, UniFi, K3s, Cloudflare and more
- **[git-fabric](https://github.com/git-fabric)**: composable fabric apps for Git-native infrastructure
- **[m5stack-lab](https://github.com/m5stack-lab)**: ESP32 firmware for M5Stack hardware

<p align="center"><sub>Built with Claude · deployed on K3s · managed by ArgoCD · now resting</sub></p>
