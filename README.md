# Literature In-Depth Reading <img src="./image.png" alt="Literature In-Depth Reading" height="32" />

A reusable prompt that makes any LLM read academic papers deeply, using a first-principles, domain-expert framework. Works with ChatGPT, Claude, Gemini, local models, or Claude Code as a native plugin.

## Use

Install once per platform. After that, just send the paper — no more copy-paste.

### Claude Code

Inside Claude Code, run:

```
/plugin marketplace add XuananLu/literature-In-depth-reading-skill
/plugin install literature-in-depth-reading@xuananlu
```

The skill then auto-triggers whenever you hand Claude Code a paper.

### Other platforms

Copy the body of [`skills/literature-in-depth-reading/SKILL.md`](skills/literature-in-depth-reading/SKILL.md) (everything below the `---` frontmatter) and paste it into the platform's persistent-instruction slot — once:

- **Claude.ai** — create a Project → paste into Project instructions.
- **ChatGPT** — create a Custom GPT → paste into Instructions.
- **Gemini** — create a Gem → paste into Gem instructions.
- **Any API** — put it in the `system` field of your requests.

From then on, every chat / call inside that Project / GPT / Gem already knows the framework. Just send the paper.

> One-off try without setup: paste the prompt body as the first message in a fresh chat, then send the paper.

## Supported inputs

- Pasted text
- PDF file (upload or drag in, if your platform supports it)
- arXiv or other paper URL (if your platform can fetch URLs)

## Example prompts

Any language, the output matches your language.

- `analyze this paper`
- `what's the novelty here`
- `break down the motivation`
- `分析这篇论文`

## What you get

A structured analysis in six sections:

1. **Task** — the problem, stated formally.
2. **Challenge** — why it is hard and where prior methods fail.
3. **Insight & Novelty** — Inspiration → Insight → Novelty, with each novelty written as `[problem] → [insight] → [design]`.
4. **Potential Flaw** — where the setting is too narrow, what data would break it, and which flaw is worth a follow-up paper.
5. **Motivation** — the author's idea reconstructed as first-principles questions.
6. **Code** — link to the official repo and a walkthrough of the code that implements the core novelty.

## Ground rules

- Every claim about the paper is traceable to the paper.
- Outside knowledge is labeled: "Based on established knowledge…".
- If the paper does not cover something, the prompt says so instead of guessing.
- Code is only discussed when it is verifiable — from the repo or the paper itself.
