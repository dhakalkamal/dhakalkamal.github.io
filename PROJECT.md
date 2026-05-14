# PROJECT.md

Shared portfolio instructions.

## Portfolio site

Personal portfolio deployed to GitHub Pages at https://dhakalkamal.github.io.
Static HTML/CSS/JS. No framework, no build step.

## What this site is

A landing page plus a case study page for each of my projects. The
goal is for someone scanning for 30 seconds to understand what I make
and want to look closer.

## Hero, about, and education (final, do not modify)

Hero:

  Hi, I'm Kamal. I came to machine learning the long way around: an
  electrical engineering degree from Aalto, an electronics one from
  Metropolia, eight years building production AI systems across
  medical imaging, NLP, computer vision, speech, and agentic systems
  at companies in Helsinki including MVision AI, GE Healthcare, and
  MDS Finland.

  I work end to end on machine learning projects, taking them from
  prototype to production. Training models, the data pipelines
  underneath, deployment, monitoring. I think about ML the way an EE
  thinks about a circuit: what's the failure mode, where does signal
  degrade, how do you instrument it.

  Now in the US. Looking for ML engineering work in the Bay Area.

About:

  Based in the US. Open to ML engineering roles in New York and the SF
  Bay Area.

  Reach me at kamaldhakal01@gmail.com.

Education:

  MSIS, Robinson College of Business, Georgia State University (2026)
  MS Electrical Engineering, Aalto University (2023)
  BS Electronics, Metropolia University of Applied Sciences (2018)

## Projects

Each project below has a GitHub repo as the canonical reference.
Some projects may also exist locally for read-only reference. Do NOT
modify files in those repos. Only write to this portfolio repo.

### 1. CORI - Counterparty Risk Intelligence
- Repo: https://github.com/dhakalkamal/counter-party-risk-intelligence (public)
- Case study slug: `cori`
- Description: Sanctions and financial-crime screening platform for
  community banks. PU learning, twelve-gate leakage validation
  framework, ICIJ network graph for hidden exposure traversal,
  Bronze/Silver/Gold medallion architecture, SHAP explainability,
  role-based React frontend. 1.83 million entities scored.
- Weight: heaviest. First on the landing page. ~1500-2000 word case study.
- Assets: alert-list.png, alert-detail-shap.png, role-views.png,
  network-graph.png, entity-detail.png in /assets/cori/.
- Has a separately published paper that the case study links to.

### 2. smriti - Long-memory companions for local LLMs
- Repo: https://github.com/dhakalkamal/smriti (active development)
- Case study slug: `smriti`
- Description: Local-first memory layer that turns short-context
  local LLMs into long-running companions. User-defined scopes for
  bounded memory partitioning. Memory archived, embedded with
  nomic-embed-text in Postgres + pgvector, retrieved via
  multi-component scoring (similarity, recency, importance,
  reinforcement, frequency). Single memory service exposed via both
  a FastAPI/React UI and an MCP server.
- Weight: middle. Second on the landing page. ~700-900 word case study.
- Landing page card includes a "Collaborate" mailto action in
  addition to the case study link.
- Asset: animated GIF or short screen recording of the chat UI in
  /assets/smriti/ (placeholder for now).

### 3. SoundSense
- Backend repo: https://github.com/dhakalkamal/SoundSense (private)
- Frontend local path only (not in a public repo yet; will be
  consolidated into the backend repo as a monorepo later, out of
  scope for this portfolio).
- Case study slug: `soundsense`
- Description: Real-time phone-native sound awareness for the deaf
  and hard of hearing. PANNs CNN14 + 527-to-10 label mapping +
  11-rule deterministic temporal reasoning + LLM language layer.
  React Native iOS/Android client.
- Weight: third. ~700-900 word case study. Hero is a YouTube embed
  of the demo video (placeholder for now, I'll provide URL).
- Source link is to the backend repo only. Mention the mobile client
  exists; do not link to it.

### 4. Bounded Governance AI
- Repo: https://github.com/dhakalkamal/bounded-governance-ai (public)
- Case study slug: `bounded-governance-ai`
- Description: Governance analysis platform using bounded agentic
  workflows for board-minute and governance-document analysis.
  Multi-agent orchestration with scoped document access,
  evidence-linked findings, reviewer correction loops, RBAC,
  and full audit trails. Next.js frontend, FastAPI backend,
  async SQLite substrate.
- Weight: fourth. ~600-800 word case study. Position as active
  prototype / active development, not a finished enterprise system.
- Assets: dashboard-overview.png,
  findings-evidence-review.png,
  audit-trail.png,
  governed-chat-citations.png in
  /assets/bounded-governance-ai/.
- Links to source repo and architecture document.

## Conventions

- Plain HTML/CSS. No React, no Tailwind, no build tooling, no npm.
- One shared stylesheet at /styles.css.
- Each case study at /projects/<slug>/index.html.
- Assets per project at /assets/<slug>/.
- Mobile-responsive.
- Deploy by pushing to main. GitHub Pages auto-builds.

## Style

- Editorial / minimal. Confident typography, generous whitespace,
  single accent color.
- Writing should sound like a person, not a marketing page. No
  "passionate," no "synergy," no buzzwords. Plain, specific sentences.
- NO EM-DASHES anywhere on the site. Use colons, commas, semicolons,
  or sentence breaks instead. This is a hard rule.

## What to ask me before doing

- Before adding any dependency or build tool.
- Before changing the overall page structure (new top-level sections,
  navigation changes).
- Before changing the hero, about, or education section copy. Those are final.
- Before writing prose for case studies that goes beyond what I have
  explicitly provided. I supply the case study text; do not generate
  new prose without asking.

## What to do without asking

- Implement HTML and CSS for case study content I provide.
- Make styling improvements consistent with the aesthetic above.
- Fix bugs, broken links, accessibility issues.
- Insert clearly-marked placeholders for assets I haven't provided
  yet (HTML comments with TODO and a description of what should
  go there).

## Adding a new project later

1. Add a new `### N. ProjectName` section below following the same shape.
2. If a local repo is needed, ask me for the local path and use it as
   read-only reference only.
3. If Claude Code local read access is needed, add the local path to
   `.claude/settings.json` under `additionalDirectories`.
4. Add the landing-page card, case-study page, assets folder, and
   CASE-STUDIES.md source entry.
5. Do not modify external project repos.

## Workflow expectations

- Prefer small, reviewable edits.
- Preserve the current visual language and spacing system.
- Do not redesign the portfolio unless explicitly requested.
- Summarize changed files after implementation.
- Prefer minimal diffs over broad rewrites.
