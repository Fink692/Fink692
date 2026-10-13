# Project catalog

A guide to my original projects and experiments. Status was reviewed on 12 October 2026 against the available repositories and project records. A working demo does not establish production use or adoption. Private source remains private.

[Back to profile](README.md)

## Apps and AI systems

### Evidence Board

A research workspace that connects claims, sources, evidence, and open questions. Ten native WebMCP tools let a compatible browser agent inspect research and propose changes. A person reviews each proposal; the tool interface cannot approve its own changes.

- **Implementation:** React, TypeScript, Zod, Drizzle, SQLite, a hosted Worker, and Playwright.
- **Status:** public editable sample with device-local persistence; separate authenticated account workspaces.
- **Evidence:** [source](https://github.com/Fink692/evidence-board), [sample](https://evidence-board-judging.fink692.chatgpt.site/?guest=1), [walkthrough](https://evidence-board-judging.fink692.chatgpt.site/walkthrough.html), [architecture](https://github.com/Fink692/evidence-board/blob/main/docs/architecture.md), [tool contracts](https://github.com/Fink692/evidence-board/blob/main/docs/webmcp-tools.md).
- **Boundary:** native tool tests and scripted demonstrations do not measure an external model's reasoning or tool-selection accuracy.

### Context

An offline relationship-memory app for remembering people and conversations. Includes selected-contact import, editable memory drafts, QR contact sharing, backups, and optional on-device inference.

- **Implementation:** Expo, React Native, TypeScript, Swift/Objective-C bridges, an optional LiteRT-LM model, and a macOS wrapper.
- **Status:** native and cross-platform project with screenshots and release documentation; store availability is not asserted here.
- **Maintenance:** [Dependency status](https://github.com/Fink692/context-memory-aid/blob/main/docs/DEPENDENCY_STATUS.md). Application and iOS diagnostics pass; the audit gate retains unresolved upstream advisories.
- **Evidence:** [source](https://github.com/Fink692/context-memory-aid), [product tour](https://github.com/Fink692/context-memory-aid#product-tour), [privacy model](https://github.com/Fink692/context-memory-aid/blob/main/PRIVACY.md), [deployment](https://github.com/Fink692/context-memory-aid/blob/main/docs/DEPLOYMENT.md).
- **Decision:** relationship data stays local; generated records remain editable and require review before saving.

### BlockScore

A native SwiftUI iOS app for address-level housing and trip research across Canada. Includes confirmed-address search, source-labelled reports, saved homes, comparisons, and report-grounded questions.

As founder and product lead, I lead a five-person team and direct product strategy, data sourcing, partnerships, team coordination, and pre-launch execution.

- **Status:** in development; source is private. Production evidence sources require explicit approval and coverage records.
- **Evidence:** [Canadian Rental Data Sources](https://github.com/Fink692/canadian-rental-data-sources) is the public companion.
- **Decision:** national baseline coverage and richer Toronto data are presented separately. Missing data remains visible; nearby or regional context is not presented as proof about a unit.
- **Release:** this catalog does not claim an App Store launch.

### Project Hope

A charity operations workspace connecting contacts, volunteers, programs, documents, schedules, and grants. Includes reviewed spreadsheet migration, organization-scoped access, audit history, and optional local AI.

- **Implementation:** Django API and workers, React web client, Electron desktop, and Ollama adapters.
- **Status:** installable desktop preview with a fictional local sample; shared charity use requires separately hosted infrastructure. Installers are unsigned.
- **Evidence:** [source](https://github.com/Fink692/project-hope), [website and downloads](https://project-hope-charities.vercel.app), [build status](https://github.com/Fink692/project-hope/blob/main/docs/full-build-status.md), [deployment](https://github.com/Fink692/project-hope/blob/main/docs/operations/production-deployment.md).
- **Decision:** core operations remain useful with AI disabled. Consequential model outputs stay reviewable.

### WildGap

A biodiversity survey tool that compares observation coverage across H3 cells, adds weather context, and builds portable field missions.

- **Implementation:** TypeScript, React, Next.js/Vinext, H3, MapLibre, GBIF, and Open-Meteo.
- **Status:** working public demo; missions use device-local storage and validated share links.
- **Evidence:** [source](https://github.com/Fink692/wildgap), [demo](https://wildgap-habitat-2026.fink692.chatgpt.site), [verification record](https://github.com/Fink692/wildgap/blob/main/docs/TEST_RESULTS.md).
- **Boundary:** an observation gap is not evidence of population decline or habitat health.

### Clearcoat Quote Studio

A vehicle-photo quoting workspace for auto detailing. Browser checks assess image quality; selected conditions become transparent CAD line items and review actions.

- **Implementation:** Next.js, TypeScript, a shared deterministic quote engine, and API routes.
- **Status:** public quote-only MVP with sample inspections. Production storage, authentication, notifications, and trained visual inference remain integration work.
- **Evidence:** [source and screenshots](https://github.com/Fink692/clearcoat-quote-studio), [quote engine](https://github.com/Fink692/clearcoat-quote-studio/blob/main/lib/quote-engine.ts).
- **Decision:** insufficient photo evidence routes to review rather than a confident quote.

## Research and data

### AgriStress

A multispectral semantic-segmentation research platform for agricultural stress, weeds, and field anomalies. Dataset adapters produce provenance-aware manifests; training and evaluation retain field/source boundaries. Prediction exports masks, uncertainty, and GeoJSON regions for review.

As co-founder and lead developer, I work with University of Manitoba Plant Sciences researchers to incorporate longitudinal wheat and canola drone imagery. That collaboration is ongoing; it does not establish completed external validation.

- **Implementation:** Python, NumPy, optional PyTorch training, geospatial exports, and local dashboards.
- **Status:** functional research workflows; code is private. External farm, crop, season, and sensor validation remains incomplete.
- **Boundary:** public-dataset and synthetic experiments do not establish field diagnosis or agronomic treatment recommendations.

### Quant Systems Lab

A Python research platform centered on chronological, queue-aware market-making replay. Additional modules cover options, reinforcement learning, portfolio optimization, credit, and systemic risk.

- **Evidence:** [source](https://github.com/Fink692/quant-systems-lab), [executed notebook](https://github.com/Fink692/quant-systems-lab/blob/main/notebooks/start_here_market_making.ipynb), [sample study](https://github.com/Fink692/quant-systems-lab/blob/main/reports/market_making_sample/study.md), [assumptions](https://github.com/Fink692/quant-systems-lab/blob/main/docs/ASSUMPTIONS_AND_LIMITATIONS.md).
- **Recorded result:** the public sample processes 301,587 synchronized messages/book states. All five tested policies lose money.
- **Boundary:** one demonstration session validates a pipeline; it does not demonstrate persistent alpha or live trading performance.

### UFC Predictor

A historical fight-outcome pipeline using rolling pre-fight features, chronological evaluation, probability calibration, and reporting.

- **Implementation:** Python, pandas, scikit-learn, command-line workflows, and spreadsheet reports.
- **Recorded benchmark:** 8,547 trainable fights; latest 20% held out; 1,709 test fights; 148 active benchmark features; 63.55% accuracy, 0.6441 log loss, and 0.6695 ROC AUC.
- **Evidence:** [source](https://github.com/Fink692/ufc-predictor), [results](https://github.com/Fink692/ufc-predictor/blob/main/docs/RESULTS.md), [model card](https://github.com/Fink692/ufc-predictor/blob/main/docs/MODEL_CARD.md).
- **Boundary:** fixture odds and synthetic stake simulations are not realized returns or verified betting performance.

### Quant Research Lab

A separate local Python framework for portfolio risk, pairs research, macro regimes, volatility surfaces, and transaction-cost-aware backtesting.

- **Status:** reusable package and command-line workflows. Provider failures can use deterministic fallback data.
- **Evidence:** [source](https://github.com/Fink692/Quant-Research-Lab), [methodology](https://github.com/Fink692/Quant-Research-Lab/blob/main/docs/methodology.md), [limitations](https://github.com/Fink692/Quant-Research-Lab/blob/main/docs/limitations.md).
- **Relationship:** this repository is distinct from Quant Systems Lab. It is not a second name for the same project.

### Topology Gate

Typed Python research infrastructure for adaptive forgetting, recursive learning, causal replay, and model-promotion controls.

- **Status:** research alpha with synthetic studies and historical paper diagnostics. No broker or order submission.
- **Evidence:** [source](https://github.com/Fink692/topology-gate), [architecture](https://github.com/Fink692/topology-gate/blob/master/docs/architecture.md), [research status](https://github.com/Fink692/topology-gate/blob/master/docs/research-status.md).
- **Boundary:** final adjusted public history is not point-in-time market evidence. Historical returns do not establish live performance.

### Public Procurement Transparency Engine

An OCDS ingestion and analysis service that preserves source records and computes deterministic procurement signals for analyst review.

- **Implementation:** Python, FastAPI, SQLAlchemy, PostgreSQL, and Alembic.
- **Status:** public code with tests and a local Compose workflow.
- **Evidence:** [source](https://github.com/Fink692/public-procurement-transparency-engine), [rules](https://github.com/Fink692/public-procurement-transparency-engine/blob/main/app/rules.py).
- **Decision:** a signal is a review lead, not an accusation.

### Civic Compiler

Municipal-data software connecting addresses, permits, notices, parcels, zoning, and rules to sourced answers and monitoring workflows.

- **Status:** private repository with customer-app, API, worker, and deployment infrastructure. The hosted preview uses labelled synthetic records.
- **Boundary:** preview coverage does not establish a deployed municipal intelligence service.

### Canadian Rental Data Sources

A public directory of official Canadian housing, municipal, tenancy, and ownership research sources with dated checks and coverage limits.

- **Status:** maintained documentation and machine-readable CSV; a dependency-free validator checks structure.
- **Evidence:** [source](https://github.com/Fink692/canadian-rental-data-sources), [methodology](https://github.com/Fink692/canadian-rental-data-sources/blob/main/docs/methodology.md).
- **Decision:** area statistics and official records are context, not proof that a listing is legitimate or a property is safe.

## Developer tools and engineering

| Project | Scope | Status and access |
| --- | --- | --- |
| **Hookwatch** | Observes what changes during a software install, including lifecycle hooks, folder-open tasks, Git hooks, and MCP configuration. | Developer-tool alpha documented in my October project showcase; no public source link verified. |
| **AccessPath CI** | Playwright flow replay with axe-core findings, screenshots, focus evidence, and traces. | Prototype on the default branch; [source and setup](https://github.com/Fink692/accesspath-ci). Build, five unit tests, and dependency audit passed; no packaged release. |
| **BOREAL-E** | Preliminary electric-aircraft engineering models, requirements traceability, thermal/energy screening, Monte Carlo studies, and CAD work. | Private digital prototype. No physical aircraft performance is verified; the current program is paused. |
| **Minecraft AutoBuild** | Java/Fabric automation around selected schematics, preflight checks, and a modified Baritone controller. | Private experimental development build. Controlled gameplay tests are documented; current installable packaging remains blocked. |

## Business software and earlier experiments

| Work | Scope | Status |
| --- | --- | --- |
| **Lake of the Woods Water Co.** | Ordering site with refill estimates, map-based route estimates, and lead capture. | Private Next.js repository. Temporary hosted SQLite storage is not durable production persistence. |
| **Gear Garage** | Founded and ran a commission-based student uniform resale business in 2024–2025; managed sourcing, pricing, promotion, and customers. | Approximately 300 uniform items and 1,000+ followers. No public software repository verified. |
| **Precision Auto Detailing** | Quoting software for a local detailing business. | Quoting software sold, as recorded in my October project showcase; no revenue total claimed here. |
| **AutomataCo** | Business automation experiments, including an appointment-waitlist optimizer. | Earlier project work; no current repository or deployment verified. |
| **Who Said It?** | Quote-guessing game concept with solo and streamer modes. | Earlier project plan; no current repository or deployment verified. |
| **Protein design** | Computational exploration. | Research experiment documented in my October showcase; no validated biological result claimed. |
| **Obsidian Academic Knowledge System** | Source/topic/argument templates, traceable research notes, and retrieval-practice workflows. | Private vault project. |
| **Paper Trader** | Paper-only prediction-market trading and a dashboard. | Private experiment; no live order placement. |
| **Roof Genius** | React/Vite roofing-business website prototype. | Earlier private prototype with placeholder business content; not an AI roofing model. |
| **Story Maker test videos** | Local narration and caption-rendering experiments. | Private test artifacts. |

Forked resource directories are third-party work, not original portfolio projects. Empty test repositories and the GitHub collaboration sandbox are omitted from the featured work.

## Education and leadership

- **Education:** St. John's-Ravenscourt, Winnipeg; Grade 12 honours student; expected graduation June 2027.
- **Certification:** IBM SkillsBuild Artificial Intelligence Fundamentals.
- **Recognition:** second place in an RRC Polytech business competition.
- **SJR Chess Club:** co-founder and organizer; teach 40+ students and organize club activities.
- **CanSkate and youth debate:** volunteer instructor; 200+ volunteer hours over three years, as recorded in my résumé.
- **Debate:** national and provincial British Parliamentary competitions, with evidence-based cases and timed oral advocacy.
- **Royal Lake of the Woods Yacht Club:** seasonal waterfront operations and member service in summers 2024–2025.
- **Athletics:** hockey and ultimate team captain; track and field athlete; completed a 42.2 km marathon.

The experience details above come from my current scholarship résumé. Project implementation and release status are documented separately in the linked repositories.
