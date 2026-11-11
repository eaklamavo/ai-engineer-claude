# Claude Certification — Hands‑On Study Plan

A project‑based, beginner‑to‑intermediate study program covering **all four Claude Certification exams** published by Anthropic (Version 1.0, effective July 2026). Each credential gets its own **track** of runnable Jupyter notebooks organized into phases, culminating in a real‑world **capstone project** you complete unaided when you are exam‑ready.

> Built from the official exam guides in [`../exam-resources-guides`](../../exam-resources-guides). Every lesson is grounded in a published blueprint domain or task statement. Where a precise API detail could change, notebooks point you to the official docs to verify rather than guessing.

---

## What's in this study plan

**110 Jupyter notebooks** (106 lessons + 4 capstones), organized into **4 tracks × 5 phases + a capstone**. Every notebook is valid `nbformat` and runs **offline without an API key** (live Anthropic API cells are guarded with mock fallbacks).

| Track | Credential | Notebooks | Capstone |
|-------|-----------|-----------|----------|
| [associate-foundations](./associate-foundations/) | Associate (CCAO‑F) | 26 | Design & run a Claude Project for a business workflow |
| [developer-foundations](./developer-foundations/) | Developer (CCDV‑F) | 27 | Production‑style Claude support agent |
| [architect-foundations](./architect-foundations/) | Architect – Foundations (CCAR‑F) | 30 | Build & harden a production Claude system |
| [architect-professional](./architect-professional/) | Architect – Professional (CCAR‑P) | 27 | Architect, evaluate & govern an enterprise solution |

Each track's 5 phases map **one‑to‑one to the exam blueprint domains**. Every lesson follows the same rhythm — objectives → concepts → code‑along steps → a `# TODO:` exercise → key takeaways → next‑lesson link — and produces a tangible artifact (a prompt, tool schema, config file, validator, or eval harness).

---

## The four credentials in this program

| Track | Credential | Exam code | Items | Time | Fee | Who it's for |
|-------|-----------|-----------|-------|------|-----|--------------|
| [associate-foundations](./associate-foundations/) | Claude Certified **Associate** – Foundations | CCAO‑F | 60 | 120 min | $99 | Business/productivity users (ops, marketing, PM, education) |
| [developer-foundations](./developer-foundations/) | Claude Certified **Developer** – Foundations | CCDV‑F | 53 | 120 min | $125 | Developers building with the API, tools, MCP, Agent SDK |
| [architect-foundations](./architect-foundations/) | Claude Certified **Architect** – Foundations | CCAR‑F | 60 | 120 min | $125 | Solution architects building agentic systems |
| [architect-professional](./architect-professional/) | Claude Certified **Architect** – Professional | CCAR‑P | 63 | 120 min | $175 | Senior architects designing enterprise solutions |

All four exams: multiple‑choice/multiple‑response, proctored (online or test center via Pearson VUE), passing score **720 on a 100–1,000 scale**, valid **12 months**.

**New to Claude?** Start with **Associate**. **Write code?** Take **Developer**. **Design production agentic systems?** Take **Architect – Foundations**, then **Professional**. The tracks share foundational ideas but are independent — do them in any order.

---

## Prerequisites

Install once, use for every track:

- **Python 3.10+** and **Jupyter** — `pip install notebook` (or `pip install jupyterlab`)
- **Anthropic Python SDK** — `pip install anthropic`
- An **Anthropic API key** — set `ANTHROPIC_API_KEY` in your environment ([get a key](https://console.anthropic.com/))
  - *Notebooks are written to run without a key too:* live API cells are guarded and fall back to a printed mock response, so you can study offline.
- **Claude Code** (Developer & Architect tracks) — [install guide](https://code.claude.com/docs/en/overview)
- Prior knowledge: Associate assumes none; Developer/Architect assume ~6 months hands‑on Claude experience and basic Python.

```bash
pip install notebook anthropic
export ANTHROPIC_API_KEY="sk-ant-..."   # Windows PowerShell: $env:ANTHROPIC_API_KEY="sk-ant-..."
jupyter notebook
```

---

## How to use the notebooks

1. Open a track folder and start at **Phase 1, Lesson 1** (`phase-1-*/lesson-1.1-*.ipynb`).
2. Run every cell **top to bottom** — each builds on the one above it.
3. Read the markdown, run the code‑along steps, then complete the `# TODO:` **exercise** cell.
4. Finish a phase, then move to the next. After all phases, do the **capstone** without looking back.
5. When you can complete a track's capstone unaided, you are ready to book that exam.

Each lesson produces something tangible — a prompt, a tool schema, a config file, a validator, an eval harness — so you learn by building, not just reading.

---

## Tracks, phases & lessons

> Lesson files are generated into each track folder. The phase structure below maps directly to each exam's published blueprint domains. Open a track's folder to see its exact lesson files.

### Track 1 — Associate – Foundations (CCAO‑F)
Maps the 7 Associate domains (Output Evaluation is the heaviest at 21%).

| Phase | Focus | Blueprint domains |
|-------|-------|-------------------|
| [phase-1-foundations-and-prompting](./associate-foundations/phase-1-foundations-and-prompting/) | Prompting & task execution | D1 (14%) |
| [phase-2-output-evaluation](./associate-foundations/phase-2-output-evaluation/) | Evaluating & validating outputs, spotting hallucinations/bias | D2 (21%) |
| [phase-3-product-and-model-selection](./associate-foundations/phase-3-product-and-model-selection/) | Products, Haiku/Sonnet/Opus, context limits | D3 (12%) |
| [phase-4-workflow-and-configuration](./associate-foundations/phase-4-workflow-and-configuration/) | Workflow integration + Projects/knowledge config | D4 (16%) + D5 (12%) |
| [phase-5-governance-and-troubleshooting](./associate-foundations/phase-5-governance-and-troubleshooting/) | Responsible use + troubleshooting/optimization | D6 (15%) + D7 (10%) |
| [capstone](./associate-foundations/capstone/) | Design & run a Claude Project for a real business workflow | all |

### Track 2 — Developer – Foundations (CCDV‑F)
Maps the 8 Developer domains (Applications & Integration is heaviest at 33.1%).

| Phase | Focus | Blueprint domains |
|-------|-------|-------------------|
| [phase-1-api-and-llm-fundamentals](./developer-foundations/phase-1-api-and-llm-fundamentals/) | LLM basics, Messages API, model selection, cost | D5 (16.8%) + D2 |
| [phase-2-prompt-and-context-engineering](./developer-foundations/phase-2-prompt-and-context-engineering/) | Prompt & context engineering, output handling | D6 (11%) |
| [phase-3-tools-and-mcp](./developer-foundations/phase-3-tools-and-mcp/) | Tool use, MCP server development, customization | D8 (10.6%) |
| [phase-4-agents-and-claude-code](./developer-foundations/phase-4-agents-and-claude-code/) | Agents & workflows, Agent SDK, Claude Code | D1 (14.7%) + D3 |
| [phase-5-security-eval-debugging](./developer-foundations/phase-5-security-eval-debugging/) | Security & safety, eval, testing, debugging | D7 (8.1%) + D4 |
| [capstone](./developer-foundations/capstone/) | Build a production‑style Claude application | all |

### Track 3 — Architect – Foundations (CCAR‑F)
One phase per domain; lessons follow the guide's **task statements** and 4 preparation exercises.

| Phase | Focus | Blueprint domain |
|-------|-------|------------------|
| [phase-1-agentic-architecture-orchestration](./architect-foundations/phase-1-agentic-architecture-orchestration/) | Agentic loops, coordinator‑subagent, hooks, handoffs | D1 (27%) |
| [phase-2-tool-design-mcp](./architect-foundations/phase-2-tool-design-mcp/) | Tool interfaces, structured MCP errors, tool_choice | D2 (18%) |
| [phase-3-claude-code-config-workflows](./architect-foundations/phase-3-claude-code-config-workflows/) | CLAUDE.md, rules, skills, plan mode, CI/CD | D3 (20%) |
| [phase-4-prompt-engineering-structured-output](./architect-foundations/phase-4-prompt-engineering-structured-output/) | Explicit criteria, few‑shot, JSON schema, batch | D4 (20%) |
| [phase-5-context-management-reliability](./architect-foundations/phase-5-context-management-reliability/) | Context preservation, escalation, provenance | D5 (15%) |
| [capstone](./architect-foundations/capstone/) | Build & harden a production Claude system | all |

### Track 4 — Architect – Professional (CCAR‑P)
One phase per domain; integration (RAG, protocols, observability) is heaviest at 19%.

| Phase | Focus | Blueprint domain |
|-------|-------|------------------|
| [phase-1-solution-design-architecture](./architect-professional/phase-1-solution-design-architecture/) | Business→solution, patterns, orchestration, value pillars | D1 (17%) |
| [phase-2-models-prompting-context](./architect-professional/phase-2-models-prompting-context/) | Model trade‑offs, prompting, context, prompt reuse | D2 (13%) |
| [phase-3-integration](./architect-professional/phase-3-integration/) | RAG, retrieval, protocols, auth, observability | D3 (19%) |
| [phase-4-evaluation-testing-optimization](./architect-professional/phase-4-evaluation-testing-optimization/) | Metrics, eval datasets, A/B, diagnosis, optimization | D4 (16%) |
| [phase-5-governance-stakeholder-enablement](./architect-professional/phase-5-governance-stakeholder-enablement/) | Governance, compliance, stakeholders, enablement | D5+D6+D7 (35%) |
| [capstone](./architect-professional/capstone/) | Architect, evaluate & govern an enterprise Claude solution | all |

**Scope:** ~5 phases × 4–6 lessons per track + a capstone each. Allow roughly **20–35 hours per track** (20–40 minutes per lesson plus capstone time).

---

## Recommended Resources

### 📋 Official Specification / Exam Guide
| Resource | URL |
|----------|-----|
| Exam guides (this repo) | [../exam-resources-guides](../../exam-resources-guides) |
| Anthropic / Claude Academy (certification & courses) | https://academy.claude.com/ |
| Claude documentation home | https://platform.claude.com/docs/en/intro |

### 📚 Core Documentation
| Resource | URL |
|----------|-----|
| Intro to Claude | https://platform.claude.com/docs/en/intro |
| Messages API — working with messages | https://platform.claude.com/docs/en/build-with-claude/working-with-messages |
| Tool use (function calling) | https://platform.claude.com/docs/en/build-with-claude/tool-use |
| Models overview & selection | https://platform.claude.com/docs/en/docs/about-claude/models |
| Claude Code overview | https://code.claude.com/docs/en/overview |
| Model Context Protocol (MCP) | https://modelcontextprotocol.io/ |
| Claude Agent SDK | https://platform.claude.com/docs/en/api/agent-sdk/overview |
| Claude Managed Agents overview | https://platform.claude.com/docs/en/managed-agents/overview |

### 🎓 Training & Courses
| Resource | URL |
|----------|-----|
| Claude Academy (official courses) | https://academy.claude.com/ |
| AI Fluency: Framework & Foundations (free) | https://academy.claude.com/ |
| Anthropic Cookbook (hands‑on recipes) | https://github.com/anthropics/anthropic-cookbook |
| Anthropic Courses (GitHub) | https://github.com/anthropics/courses |

### 📝 Cheat Sheets & Quick Reference
| Resource | URL |
|----------|-----|
| Prompt engineering overview | https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview |
| Prompt library | https://platform.claude.com/docs/en/resources/prompt-library/library |
| API reference (Messages) | https://platform.claude.com/docs/en/api/messages |
| Claude Code CLI reference | https://code.claude.com/docs/en/cli-reference |

### 🛠️ Key Docs by Phase / Feature
| Area | Feature | URL |
|------|---------|-----|
| Associate P2 / Architect P4 | Reducing hallucinations & output validation | https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-hallucinations |
| Associate P5 / Architect‑Pro P5 | Projects, memory & knowledge | https://platform.claude.com/docs/en/intro |
| Developer P1 | Messages API & streaming | https://platform.claude.com/docs/en/build-with-claude/streaming |
| Developer P1 | Prompt caching (cost) | https://platform.claude.com/docs/en/build-with-claude/prompt-caching |
| Developer P1 / Architect P4 | Message Batches API | https://platform.claude.com/docs/en/build-with-claude/batch-processing |
| Developer P3 / Architect P2 | Tool use & tool_choice | https://platform.claude.com/docs/en/build-with-claude/tool-use |
| Developer P3 | MCP server development | https://modelcontextprotocol.io/docs |
| Developer P4 / Architect P1 | Agent SDK & agentic loops | https://platform.claude.com/docs/en/api/agent-sdk/overview |
| Developer P4 / Architect P3 | Claude Code configuration (CLAUDE.md, settings) | https://code.claude.com/docs/en/overview |
| Developer P5 / Architect‑Pro P5 | Safety, guardrails & mitigating jailbreaks | https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/mitigate-jailbreaks |
| Architect P4 | Structured/JSON output via tools | https://platform.claude.com/docs/en/build-with-claude/tool-use |
| Architect‑Pro P3 | Embeddings & retrieval (RAG) | https://platform.claude.com/docs/en/build-with-claude/embeddings |
| Architect‑Pro P2 | Context windows & token counting | https://platform.claude.com/docs/en/build-with-claude/token-counting |

### 🧪 Practice & Sandboxes
| Resource | URL |
|----------|-----|
| Anthropic Console (Workbench & prompt generator) | https://console.anthropic.com/ |
| Anthropic Cookbook (runnable notebooks) | https://github.com/anthropics/anthropic-cookbook |
| MCP example servers | https://github.com/modelcontextprotocol/servers |
| Claude Quickstarts | https://github.com/anthropics/claude-quickstarts |

### 🏘️ Community & Support
| Resource | URL |
|----------|-----|
| Anthropic Discord | https://www.anthropic.com/discord |
| Anthropic on GitHub | https://github.com/anthropics |
| Developer docs & support | https://platform.claude.com/docs/en/intro |
| Anthropic news / blog | https://www.anthropic.com/news |
| Certification support | certifications-support@anthropic.com |

> A few deep‑link paths above may shift as Anthropic reorganizes docs (docs.anthropic.com and docs.claude.com currently redirect to platform.claude.com). If a link 404s, search the term on https://platform.claude.com/docs.

---

## Capstone overview (per track)

- **Associate:** Configure and run a Claude **Project** for a real business workflow — instructions + knowledge sources, draft content, validate outputs for accuracy/bias, redact regulated PII, pick the right model, ship a deliverable.
- **Developer:** Build a **production‑style Claude application** — an agent using the Messages API + a custom tool + a small MCP server, structured output via JSON schema, a guardrail, token‑cost tracking, and error recovery.
- **Architect – Foundations:** **Build & harden a production Claude system** combining the guide's four preparation exercises — multi‑tool agent with escalation, Claude Code team config, extraction pipeline with validation/retry/batch, and a multi‑agent research pipeline with provenance.
- **Architect – Professional:** **Architect, evaluate & govern an enterprise solution** — discovery, a documented architecture decision, RAG + integration with auth & observability, an evaluation harness, cost/latency modeling, guardrails + compliance, and a stakeholder architecture doc.

---

## Study tips

- **Hands‑on beats reading.** Build and operate at least one real workflow/app per track.
- **Trust validation, not confidence.** A recurring exam theme: self‑reported model confidence is not an accuracy signal — verify claims, cite sources, and route uncertain cases to humans.
- **Match the tool to the job.** Model selection, API vs batch, workflow vs agent, built‑in tool vs custom tool vs MCP — the exams test *judgment about trade‑offs*, not trivia.
- **Use the sample questions** in each exam guide to calibrate difficulty before booking.

---

## Suggested starting point

1. **Install the tools** (once): `pip install notebook anthropic` — see [Prerequisites](#prerequisites).
2. **Pick your track** by role:
   - New to Claude / business user → **Associate**: [phase-1-foundations-and-prompting](./associate-foundations/phase-1-foundations-and-prompting/) → `lesson-1.1`
   - Developer → **Developer**: [phase-1-api-and-llm-fundamentals](./developer-foundations/phase-1-api-and-llm-fundamentals/) → `lesson-1.1`
   - Solution architect → **Architect – Foundations**: [phase-1-agentic-architecture-orchestration](./architect-foundations/phase-1-agentic-architecture-orchestration/) → `lesson-1.1`
   - Senior architect → **Architect – Professional**: [phase-1-solution-design-architecture](./architect-professional/phase-1-solution-design-architecture/) → `lesson-1.1`
3. **Run top to bottom**, do the exercise, then move to the next lesson.
4. **Finish with the capstone** — when you can complete it unaided, book your exam.

---

## How it was built

- **Grounded in the official guides.** All four exam PDFs in [`../exam-resources-guides`](../../exam-resources-guides) were extracted and parsed; every lesson maps to a published blueprint domain, task statement, or sample question — no invented objectives.
- **Phases mirror the blueprint.** Each track has one phase per exam domain, weighted toward the heaviest domains (e.g., Output Evaluation for Associate, Applications & Integration for Developer, Agentic Architecture for Architect – Foundations, Integration for Architect – Professional).
- **Consistent lesson template.** Objectives → concepts → code‑along steps → a `# TODO:` exercise → key takeaways → next‑lesson link, each producing a tangible artifact.
- **Runs offline.** Live Anthropic API cells are wrapped with guarded mock fallbacks, so notebooks work without an `ANTHROPIC_API_KEY`; set the key to see real responses.
- **Honest about change.** Where a model ID, price, or exact API parameter could drift, notebooks point to the official docs to verify rather than guessing.
- **Validated.** All 110 notebooks pass `nbformat` validation and every Python code cell is syntax‑checked; folder names and links are verified against the tables above.

---

## Bookmarks

- 📖 **Claude docs** — https://platform.claude.com/docs/en/intro
- 🎓 **Claude Academy** (official courses & certification) — https://academy.claude.com/
- 🧑‍🍳 **Anthropic Cookbook** (runnable recipes) — https://github.com/anthropics/anthropic-cookbook
- 🛠️ **Anthropic Console** (Workbench & prompt tools) — https://console.anthropic.com/
- 🔌 **Model Context Protocol (MCP)** — https://modelcontextprotocol.io/
- 💻 **Claude Code** — https://code.claude.com/docs/en/overview
- 💬 **Anthropic Discord** — https://www.anthropic.com/discord

Good luck — start with **Phase 1, Lesson 1** of your chosen track. 🎓
