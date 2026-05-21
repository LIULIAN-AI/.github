<div align="center">

# LIULIAN · 流联

### *A studio for time-series forecasting.*

#### From dataset to dashboard, with an agent that holds the chalk.

<br>

[![demo](https://img.shields.io/badge/▶_try_the_web_demo-E20613?style=for-the-badge&labelColor=131313)](https://liulian-ai.github.io/liulian-web/web-demo.html)
[![docs](https://img.shields.io/badge/📖_federation_docs-131313?style=for-the-badge)](https://github.com/liulian-ai/liulian-docs)
[![python](https://img.shields.io/badge/🧪_ML_core-E20613?style=for-the-badge&labelColor=131313)](https://github.com/liulian-ai/liulian-python)

<br>

</div>

---

## What is LIULIAN

**A research-grade ML platform for time-series & spatio-temporal forecasting** — built around an editorial-Swiss BI canvas, anchored by an AI agent that proposes panels, drafts reports, and lets you sketch a chart and watch it materialise.

Think *Power BI for ML researchers*, but the agent speaks from where you look, not from a corner sidebar. Six "fused-mode" principles (**F1** spatial anchoring · **F2** predictive prefetch · **F3** bidirectional spec sync · **F4** visible reasoning · **F5** reversible by default · **F6** shared cursor) shape every interaction.

---

## See it

<div align="center">

### The Doorway · entrance

![Doorway · entrance hero](https://raw.githubusercontent.com/liulian-ai/.github/main/profile/assets/doorway.png)

*Four entry cards · agent chat · keyboard shortcuts. 20 seconds to a useful next click.*

<br>

### Today · the daily landing

![Today · morning note + attention / in-flight / continue](https://raw.githubusercontent.com/liulian-ai/.github/main/profile/assets/today.png)

*Agent has drafted a morning note. Three columns surface what needs your eyes, what's running, and what to pick back up.*

<br>

### Forecast · live Q05–Q95 fan

![Forecast · live fan + KPIs + alerts](https://raw.githubusercontent.com/liulian-ai/.github/main/profile/assets/forecast.png)

*PatchTST on the Aare river · 72-hour discharge · backtest MAE 8.42 m³/s · `</> spec` reveals the JSON the agent edits.*

</div>

---

## The 9-repo federation

LIULIAN is an intentional multi-repo split. Each repo owns one technology stack and one concern — no monolith.

| Repo | Stack | What it owns |
|---|---|---|
| [**liulian-web**](https://github.com/liulian-ai/liulian-web) ★ | Next.js · TypeScript | the BI canvas · web demo · redesign rounds |
| [**liulian-python**](https://github.com/liulian-ai/liulian-python) ★ | Python · NumPy · PyTorch | ML core: datasets · models · runtime · experiments |
| [**liulian-docs**](https://github.com/liulian-ai/liulian-docs) ★ | mkdocs-material | federation hub: ADRs · user stories · agile templates · platform blueprint |
| [**liulian-api**](https://github.com/liulian-ai/liulian-api) ★ | Python · FastAPI | REST surface over the ML core |
| [**liulian-agent**](https://github.com/liulian-ai/liulian-agent) ★ | Python · FastAPI · SSE | LLM gateway + BI agent · tool registry |
| [**liulian-mobile**](https://github.com/liulian-ai/liulian-mobile) ★ | Swift · Kotlin · ArkTS | native iOS / Android / HarmonyOS apps |
| [liulian-design-system](https://github.com/liulian-ai/liulian-design-system) | TS / JS | design tokens · reference designs · UI audit checklist |
| [liulian-dev-env](https://github.com/liulian-ai/liulian-dev-env) | shell · docker · slurm | local 3-tier stack · UBELIX cluster setup |
| [liulian-ops](https://github.com/liulian-ai/liulian-ops) | Python · click · helm | deploy CLI · runbooks · cost ledger |
| [liulian-ingest](https://github.com/liulian-ai/liulian-ingest) | Python · FastAPI | scheduled crawlers · manifests |

★ = recommended pinned items (the 6 most useful for a first visitor).

---

## Where to start

| If you are a … | Open … |
|---|---|
| **First-time visitor** | the [single-file web demo](https://liulian-ai.github.io/liulian-web/web-demo.html) — no install, just download + open |
| **ML researcher** | the [Python core](https://github.com/liulian-ai/liulian-python) — adapter contract + manifest spec + datasets catalog |
| **Product / advisor reviewer** | the [user stories](https://github.com/liulian-ai/liulian-docs/tree/main/docs/user-stories) — six codenamed flows (Doorway · Annotated Drop · First Light · Pencil · Graft · Easel), each in three modes |
| **Infra / DevOps** | [`liulian-dev-env`](https://github.com/liulian-ai/liulian-dev-env) (local stack) and [`liulian-ops`](https://github.com/liulian-ai/liulian-ops) (deploy + cost ledger) |
| **Designer / brand contributor** | [`liulian-design-system`](https://github.com/liulian-ai/liulian-design-system) (tokens · 12-platform reference designs · UI audit) |

---

## Design language

- **Fonts:** [Fraunces](https://fonts.google.com/specimen/Fraunces) (display, with WONK axis) · [Switzer](https://www.fontshare.com/fonts/switzer) (body) · [JetBrains Mono](https://www.jetbrains.com/lp/mono/) (numbers · code)
- **Palette:** warm bone canvas `#FBFBFA` · UniBe red `#E20613` as the single accent · 1 px hairlines · max 2 reds per viewport
- **Charts:** [ECharts](https://echarts.apache.org/) as the engine · [Vega-Lite](https://vega.github.io/vega-lite/) grammar for portable specs · custom Q05-Q95 fan + multi-model overlay + correlation matrix + severity ribbon
- **Editor:** [draw.io](https://github.com/jgraph/drawio) embedded as the vector canvas for chart annotation
- **Mode-C "fused" interactions:** the six principles above (F1–F6) — distilled in [`liulian-docs/docs/user-stories/index.md`](https://github.com/liulian-ai/liulian-docs/blob/main/docs/user-stories/index.md)

The brand anchor is UniBe red — the official red of the [University of Bern](https://www.unibe.ch/), where the project was born. ADR 0004 in [`liulian-docs/docs/strategy/adr/`](https://github.com/liulian-ai/liulian-docs/tree/main/docs/strategy/adr) tells the story.

---

## Status

| Surface | State |
|---|---|
| Web demo (this profile's screenshots) | ✅ shipping |
| `/forecast` canvas in Next.js | ✅ R8 design lock implemented · real swiss-river-1990 data |
| Federation CI | ✅ green across all 6 CI-enabled repos · see [ci-skips ledger](https://github.com/liulian-ai/liulian-docs/blob/main/docs/agile/ci-skips-2026-05-21.md) for IOUs |
| Mobile parity | 🚧 iOS Swift snapshots in place · Android / HarmonyOS WIP |
| Save & share dashboards | 🚧 spec'd (R8 §11) · endpoint stub |
| Drawio twin-track editor | 🚧 spec'd (R7) · iframe protocol drafted |

---

## License

All public repos are MIT licensed unless otherwise stated.

<sub>Built by [Linlin Jia](https://github.com/jajupmochi) at the University of Bern, with Claude as design + coding partner.</sub>
