# Google AI Search Optimization Skill

An open Agent Skill for applying Google's official guidance on optimizing websites for generative AI features in Google Search, including AI Overviews and AI Mode.

This skill helps AI agents explain, audit, plan, and implement SEO work based on Google's current public recommendations. It focuses on practical Search fundamentals: crawlability, indexability, helpful non-commodity content, media SEO, structured data, ecommerce/local details, and agent-friendly site readiness.

Primary source: [Google's guide to optimizing for generative AI features on Google Search](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide).

## Try It Online

[![Try Google AI Search Optimization on Socialistic](https://socialistic.ai/api/embed/google-ai-search-optimization-73717e?lang=en)](https://socialistic.ai/en/skill/google-ai-search-optimization-73717e?utm_source=github&utm_medium=readme&utm_campaign=20260604-url-diagnostics-skill-builders&utm_content=badge)

Paste a page URL and get the audit back — no clone or install required.

## Install

Install with the open [`skills` CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add deepakness/google-ai-search-optimization
```

The CLI may ask whether to install for the current project or globally.

To force a global install:

```bash
npx skills add deepakness/google-ai-search-optimization --global
```

List available skills before installing:

```bash
npx skills add deepakness/google-ai-search-optimization --list
```

## Manual Install

You can also clone or download this repository and copy the skill folder directly.

Project-local install for agents that use the common `.agents/skills` path:

```bash
git clone https://github.com/deepakness/google-ai-search-optimization.git
mkdir -p .agents/skills
cp -R google-ai-search-optimization/skills/google-ai-search-optimization .agents/skills/
```

Global Codex install:

```bash
mkdir -p ~/.codex/skills
cp -R google-ai-search-optimization/skills/google-ai-search-optimization ~/.codex/skills/
```

Global Claude Code install:

```bash
mkdir -p ~/.claude/skills
cp -R google-ai-search-optimization/skills/google-ai-search-optimization ~/.claude/skills/
```

The folder you copy should contain `SKILL.md` at its root.

## What It Covers

- How Google AI Overviews and AI Mode relate to normal Google Search.
- Why SEO still matters for generative AI Search.
- Retrieval-augmented generation, query fan-out, and Search-index grounding.
- Helpful, reliable, people-first content.
- Non-commodity content and firsthand expertise.
- Crawlability, indexing, snippets, canonicalization, JavaScript SEO, and page experience.
- Image and video SEO for AI-era Search visibility.
- Structured data without treating schema as an AI-specific ranking trick.
- Ecommerce and local business details through Merchant Center and Business Profile.
- Myth-busting around AEO/GEO hacks, `llms.txt`, content chunking, fake mentions, and AI-only rewrites.
- Agent-friendly website readiness.

## Repository Structure

```text
.
├── README.md
└── skills
    └── google-ai-search-optimization
        ├── SKILL.md
        └── references
            ├── audit-playbook.md
            └── google-ai-search-principles.md
```

## Usage Examples

Ask your AI agent:

```text
Use the google-ai-search-optimization skill to audit this product page for Google AI Search readiness.
```

```text
Use the google-ai-search-optimization skill to turn this SEO advice into a prioritized implementation plan.
```

```text
Use the google-ai-search-optimization skill to check whether adding llms.txt helps with Google AI Overviews.
```

## Notes

This skill summarizes and operationalizes public Google guidance, but it is not a replacement for the live docs. For current policy-sensitive advice, verify against the official Google sources linked inside the skill references.

The `skills` CLI may collect anonymous install telemetry. To opt out:

```bash
DISABLE_TELEMETRY=1 npx skills add deepakness/google-ai-search-optimization
```
