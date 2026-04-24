# Literature In-Depth Reading <img src="./image.png" alt="Literature In-Depth Reading" height="32" />

A reusable prompt that makes any LLM read academic papers deeply, using a first-principles, domain-expert framework. Works with ChatGPT, Claude, Gemini, local models, or Claude Code as a native plugin.

## The prompt

The full prompt lives in [`skills/literature-in-depth-reading/SKILL.md`](skills/literature-in-depth-reading/SKILL.md). Copy the body (everything below the `---` frontmatter) and use it however your platform allows.

## Use

### Option 1 — Any chat app (ChatGPT, Claude.ai, Gemini, …)

Paste the prompt body as a custom instruction, system prompt, or first message. Then send the paper.

### Option 2 — Any LLM API

Use the prompt body as your `system` message. Send the paper as the `user` message.

### Option 3 — Claude Code (native plugin)

Clone into the plugin directory. The skill loads on next launch:

```bash
git clone https://github.com/XuananLu/literature-In-depth-reading-skill.git ~/.claude/plugins/literature-in-depth-reading
```

## Supported inputs

- Pasted text
- PDF file (upload or drag in, if your platform supports it)
- arXiv or other paper URL (if your platform can fetch URLs)

## Example prompts

English or Chinese — the output matches your language.

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
