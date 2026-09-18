# OG Green

**Senior Principal Data Scientist / AI Engineering Leader**

I build high-stakes applied-ML and AI systems that are measurable, auditable and production-ready — from fraud
and graph analytics to LLM evaluation and developer-reliability tooling. The common thread across everything
below: the evaluation is itself an engineering artifact. Baselines, negative results, uncertainty, cost, leakage
and failure modes are reported, not hidden.

<!-- TODO(owgreen): add links — [LinkedIn](…) · [Résumé](…) · [Email](…) -->

## Start here

| Project | What I owned | Evidence |
|---|---|---|
| [ellip2](https://github.com/owgreen-dev/ellip2) | AML graph-ML research + discovery architecture | 0.911 ± 0.009 PR-AUC over 121,810 labeled subgraphs; discovery over a 49.3M-cluster background; failed model families and leakage/shift analysis documented; reproducible GPU pipeline |
| [relief-probe](https://github.com/owgreen-dev/relief-probe) | Public-data fraud analytics, end to end | 11.4M PPP loans; out-of-time validation against DOJ/SBA-OIG enforcement; 23.8× lift @500 with a bootstrap interval; honest that a simple baseline captures much of the signal |
| [Shipi18n](https://github.com/Shipi18n/shipi18n) | OSS QA architecture + evaluation + upstream validation | 64 repos scanned, 21 shipping a verified broken string, 119 defects verified by hand, 3 fixed upstream in the first week — [live tally](https://shipi18n.com/oss) |
| [tsfix](https://github.com/Shipispec/tsfix) | AI code-repair architecture | deterministic + LLM repair layers; real-world benchmark split by workload; < $0.005 per fix |

Role on all four: architect and sole author — problem framing, data and evaluation design, system architecture,
implementation, reproducibility, deployment surfaces and documentation.

## Selected external impact

Findings from my tooling that other projects acted on:

- **Solidus** — 13 dropped `%{…}` interpolations restored in pt-BR; [PR merged the same day](https://github.com/solidusio/solidus/pull/6626) with three core-team approvals.
- **Plane** — Czech template toasts lost their variables; [PR merged in three hours](https://github.com/makeplane/plane/pull/9848) by a co-founder.
- **nocodb** — [my issue](https://github.com/nocodb/nocodb/issues/14573) on translated/dropped vue-i18n variables led to a [maintainer PR that swept all 39 locales](https://github.com/nocodb/nocodb/pull/14581).
- **Excalidraw** — [my issue](https://github.com/excalidraw/excalidraw/issues/12097) on a `{{max}}`→`{{mix}}` typo led a contributor to [fix it and add a placeholder-parity test suite](https://github.com/excalidraw/excalidraw/pull/12109) to a 130k-star repo.

<!-- TODO(owgreen): one accurate paragraph on professional leadership scope (team/portfolio, technical direction,
     model review, mentoring) — generic enough for NDA, specific enough for level. Do not invent numbers. -->

## Featured project

### [relief-probe](https://github.com/owgreen-dev/relief-probe)

Fraud-lead research pipeline over **11.4M public PPP loans**, validated against real enforcement outcomes from DOJ/SBA-OIG sources.

This project focuses on turning public records into transparent, defensible investigative leads — not accusations.

**Highlights:**

- Built a local analytical warehouse from public SBA/DOJ data
- Used anomaly detection and ML experiments to rank potentially suspicious loans
- Added positive-unlabeled learning and LightGBM experiments
- Benchmarked signals against known prosecuted cases
- Included bootstrap confidence intervals and clear model limitations
- Built Streamlit views for analyst-style review
- Added LLM-assisted entity resolution, retrieval, and similar-case workflows
- Framed outputs responsibly as statistical leads, not proof of fraud

**Stack:** Python · DuckDB · pandas · scikit-learn · LightGBM · Streamlit · LLM workflows · graph/retrieval methods

## Organizations / workstreams

I use GitHub organizations to separate different kinds of work instead of mixing every project into one personal account.

### [Shipi18n](https://github.com/Shipi18n)
Open-source QA for i18n locale files — a deterministic linter (missing keys, dropped placeholders, invalid
ICU, collapsed plurals across JSON/YAML/ARB/PO/XLIFF/Android/Apple) with an optional, separately benchmarked
LLM semantic pass. CLI, core library, MCP server, GitHub Action, Docker, pre-commit.

What makes it more than a linter: I run it on real open-source repositories, verify every finding by hand
against the source language, and send the fix upstream — then turn every false positive the scan exposes into a
regression fixture. Running tally with links: **[shipi18n.com/oss](https://shipi18n.com/oss)**.

### [Shipispec](https://github.com/Shipispec)
Reliability tooling for AI-assisted software engineering. Flagship: **[tsfix](https://github.com/Shipispec/tsfix)** —
library-aware TypeScript error recovery for LLM-generated code, deterministic quick-fixes first, an opt-in LLM
repair layer second, measured on a real-world failure benchmark (98.6% single-file, 40.0% multi-file, 81.4%
aggregate, under $0.005 per fix) with the weak cases reported alongside the headline.

## Current focus

I am building public portfolio projects that show the kind of work I can discuss openly when client work cannot be shared in detail.

My emphasis is on:

- Messy real-world data
- Transparent assumptions
- Reproducible pipelines
- Honest validation
- Practical analyst workflows
- LLMs used as workflow support, not magic black boxes
- Small tools that solve specific developer pain points

## Selected stack

Python · SQL · DuckDB · pandas · scikit-learn · LightGBM · Streamlit · AWS · LLM APIs · LangChain · LangGraph · JavaScript/TypeScript · GitHub Actions

## What I’m interested in

- Fraud detection and program integrity
- Public-sector and government data systems
- Applied ML that survives honest evaluation
- LLMs for retrieval, triage, entity resolution, and analyst workflows
- Reproducible data pipelines
- Developer tools and workflow automation
- API/spec tooling
- Lightweight SaaS products
