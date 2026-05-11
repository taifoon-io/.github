# Taifoon

> *Mathematics rendered in light.*
>
> The blockchain operating system. 41 chains. One cryptographic root. Zero trust required.

[**taifoon.io**](https://taifoon.io) · [Builders Programme](https://taifoon.io/builders) · [OS Dispatch](https://taifoon.io/os/dispatch) · [License (TSUL)](https://taifoon.io/legal/tsul)

---

## What's here

A fleet of agents that maintain themselves, ship adapters under fair-code, and route a 49 bps on-chain donut to whoever ships the code that handles each settled call. **70% to the contributor, 20% to the reviewer agents, 10% to the ecosystem treasury** — perpetually, in whatever currency the upstream call settled in.

## The repos

**Open source** — read, fork, integrate freely under their respective licenses:

| Repo | Purpose | License |
|------|---------|---------|
| [`license`](https://github.com/taifoon-io/license) | Canonical TSUL + Apache 2.0 + MIT + CLA. **Single source of truth** — every repo references this one. | CC0 (metadata) |
| [`taifoon-solver`](https://github.com/taifoon-io/taifoon-solver) | 9-adapter UniversalOperator fleet. V5-proof-anchored fills. Submitted to Colosseum Frontier 2026. | Apache 2.0 |
| [`taifoon-sdk`](https://github.com/taifoon-io/taifoon-sdk) | `npm install @taifoon/sdk` — proof, gas, signals, executor, registry clients. | Apache 2.0 |
| [`taifoon-solver/rust/crates/taifoon-mcp-server`](https://github.com/taifoon-io/taifoon-solver/tree/main/rust/crates/taifoon-mcp-server) | MCP server — 5 tools: get_quote, explain_route, route_stats, protocol_health, solver_leaderboard. | Apache 2.0 |
| [`open-mamba`](https://github.com/taifoon-io/open-mamba) | MIT task bus — durable queue, agent dispatch, webhook + cron triggers. Self-hosted, no telemetry. | MIT |
| [`taifoon-design-system`](https://github.com/taifoon-io/taifoon-design-system) | CSS token system (`--tf-*`), fonts, motion spec — the "mathematics rendered in light" visual language. | CC-BY-4.0 |
| [`taifoon`](https://github.com/taifoon-io/taifoon) | Ecosystem overview and architecture map. | MIT |

**Fair-code under TSUL** — source-available, internal commercial use free, donut routing preserved:

| Repo | Purpose | License |
|------|---------|---------|
| `taifoon-eco` | On-chain contracts: BuildersRegistry (donut routing), BountyEscrow, NemotronBillingMeter. Adapter template under Apache 2.0 at [`taifoon-eco/templates/adapter-v1/`](https://taifoon.io/builders/template). | TSUL v1.0 |
| `taifoon-mamba` | Pro dispatcher tier on top of open-mamba — CostOptimizer routing, Builders Programme bounty scoper. | TSUL v1.0 |
| `taifoon-web` | Source of taifoon.io. Next.js 15, Tailwind v4. The site itself is the public surface. | TSUL v1.0 |

---

## V5 Proof System

Every fill is wrapped in a 6-layer MMR proof (L1 SuperRoot → L6 FinalityCommitment). 41 chains. 14 finality types. Assembled every 10 seconds. Verifiable on-chain via `TaifoonMMRVerifier`.

## Donut economics

49 bps on every settled adapter call → 70% creator / 20% reviewers / 10% ecosystem. Enforced by `BuildersRegistry.sol` — the contract is the license. Automatic. On-chain. No human intermediary.

## How to start

- Read a route, claim a route: [`taifoon.io/builders/bounties`](https://taifoon.io/builders/bounties)
- Run the canonical loop: `pnpm tsx examples/intent-to-fill.ts "1000 USDC eth → sol, fast"` ([taifoon-solver](https://github.com/taifoon-io/taifoon-solver/blob/main/examples/intent-to-fill.ts))
- Submit a route to the flywheel: [`taifoon.io/os/submit-job`](https://taifoon.io/os/submit-job)
- Watch the agent fleet in real time: [`taifoon.io/os/dispatch`](https://taifoon.io/os/dispatch)
- Read the license: [`github.com/taifoon-io/license`](https://github.com/taifoon-io/license)

License or commercial questions: **taifooon@proton.me** · Built fair-code: [faircode.io](https://faircode.io/).
