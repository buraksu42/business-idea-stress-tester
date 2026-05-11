# Business Idea Stress Tester

A Claude Code / Claude.ai **skill** that puts new business or product ideas through a structured, brutally honest pre-mortem — Socratic dialogue, deep web research, devil's-advocate critique — across both **idea quality** and **founder/resource fit**, then ships a printable HTML verdict report.

It's not a brainstorming partner. It's not a friendly second opinion. It's the conversation you'd have with an experienced co-founder doing free office hours: sharp, honest, useful — designed to break the idea *now*, before money and time are committed.

## What it does

The skill runs a 6-phase stress test:

1. **Understand the problem** — interview until the persona, current behavior, and willingness to pay are concrete (not abstract)
2. **Founder & resource fit** — domain depth, distribution wedge, runway, build complexity vs capacity
3. **Devil's advocate** — pressure-test every load-bearing assumption, no escape ramps
4. **Deep research** — 6–10+ web searches: competitors, market size, post-mortems, macro risks
5. **Verdict synthesis** — three independent axes (Idea / Founder / Resources) → one of GO / PIVOT / WAIT / PARTNER / NO-GO with confidence %
6. **Visual report** — single-file HTML artifact, editorial or infographic style, print-ready

Built-in mechanics that keep it honest:

- **Insight Test**, **5 Names Test**, and **verbatim quote requirement** — dodge twice and the corresponding axis is automatically capped
- **On-screen unit economics** — when the user proposes "I'll add a contractor" / "AI handles it" / "VA on Upwork", the math is computed live with realistic local rates, not waved at abstractly
- **Pivot containment** — Phase 3 diagnoses, never offers exit doors; pivots only surface in the Phase 5 verdict
- **Macro risk audit** — platform / regulatory / commoditization / substitution / cycle-reversal, surfaced explicitly before the verdict
- **Local context aware** — adapts to the user's market (regulatory regime, payments, distribution channels, talent costs, sales cycle), responds in the user's language

## Triggers

The skill auto-activates when a user shares an idea for evaluation — phrases like *"I have an idea"*, *"I want to start a project"*, *"evaluate this idea"*, *"should I build this"*, *"is this worth pursuing"* — and even when the user just describes a concept conversationally without asking for validation explicitly.

It does **not** trigger for already-launched product feedback, marketing audits, or strategy on existing businesses. Pre-build / pre-launch ideas only.

## Install

### Claude Code (CLI)

Drop the skill into your skills directory:

```bash
git clone https://github.com/buraksu42/business-idea-stress-tester ~/.claude/skills/business-idea-stress-tester
```

That's it. Next time you start a Claude Code session and share an idea, the skill activates automatically.

To update later:

```bash
cd ~/.claude/skills/business-idea-stress-tester && git pull
```

### Claude.ai (web / desktop)

Download `business-idea-stress-tester.skill` from this repo, then upload it via your Claude settings → Skills page.

## Usage

Just talk to Claude about your idea. No slash command, no special invocation. Example openings that trigger the skill:

> *"I have an idea for a tool that helps freelancers track invoices…"*
>
> *"Thinking about building an AI assistant for…"*
>
> *"Should I start a SaaS for [niche]?"*

Claude will respond as the stress-tester: questions first, then research, then verdict, then HTML report. The whole flow takes 30–60 minutes of dialogue depending on how much pushback the idea survives.

## Output

A standalone HTML report (printable to PDF) with:

- Verdict banner (GO / PIVOT / WAIT / PARTNER / NO-GO + confidence %)
- Three score-meters (Idea / Founder / Resources)
- TL;DR, persona breakdown, market sizing, competitive landscape table
- Founder fit & capital reality, scored with reasoning
- Macro risk audit (5-box)
- Top 5–7 ranked risks with mitigations
- A specific named experiment to run **this week**, with an explicit success threshold
- All sources cited

Editorial style by default; ask for *"infographic-style"* / *"more visual"* / *"dashboard view"* to switch to the data-dense variant (radial gauges, 2×2 risk matrix, hero stats).

## Philosophy

> Honesty over politeness. Time over feelings.

A good idea executed by the wrong person, on the wrong capital structure, with the wrong distribution, fails just as hard as a bad idea. The cost of being too soft is the user spending 18 months on a dead idea. The cost of being too sharp is one uncomfortable conversation.

Ideas this skill is happy to crush early include yours. That's the point.

## License

No license. Use it, fork it, modify it, re-share it. Attribution appreciated but not required.

## Contributing

Issues and PRs welcome. The skill is intentionally a single SKILL.md file — keep it that way unless something genuinely needs reference material extracted (see "Notes & Roadmap" at the bottom of `SKILL.md`).
