# idea-to-mvp

**A Claude skill for entrepreneurship ideation coaching.**

Guides founders from a vague idea to a validated, scoped MVP plan — in one structured conversation.

---

## What it does

This skill turns Claude into a practical entrepreneurship coach covering three phases in sequence:

| Phase | Goal | Output |
|-------|------|--------|
| 1 — Idea Refinement | Excavate the real problem beneath the solution | Idea Health Scorecard + problem statement |
| 2 — Validation Design | Design the smallest experiment to prove the hypothesis | Validation experiment plan |
| 3 — MVP Scoping | Define the smallest thing worth building | MVP plan with Hook design |

---

## When it triggers

Any message with entrepreneurial intent — including:

- "I have an idea for a startup"
- "I want to build something for X"
- "Is this a good business idea?"
- "I'm thinking of quitting my job to..."
- "What should my MVP look like?"
- "How do I validate this?"
- "I'm working on a side project"

Claude does not wait for an explicit coaching request. If there's entrepreneurial intent, the skill activates.

---

## Key frameworks integrated

- **Idea Health Scorecard** — 6-dimension scoring (problem clarity, customer specificity, founder-problem fit, competitive gap, timing, conviction)
- **Why now?** — Sequoia's timing question, applied as a Phase 1 gate
- **Mom Test principles** (Rob Fitzpatrick) — life-centric customer interview questions
- **Validation ladder** — 5 levels from worthless to definitive signal
- **Pre-mortem** — surfaces the riskiest assumption before customer conversations
- **Beachhead market** — start with the 100 most desperate users, not the total addressable market
- **Hook Model** (Nir Eyal, *Hooked*) — Trigger → Action → Variable Reward → Investment, built into MVP scoping
- **Manipulation Matrix** — ethical gate before finalizing product design
- **Build/buy/skip filter** — no-code first, feature discipline
- **Minimalist MVP** (Sahil Lavingia) — manual → processized → productized

---

## File structure

```
idea-to-mvp/
├── SKILL.md                    ← Main skill instructions (loaded into context)
├── README.md                   ← This file
└── references/
    ├── frameworks.md           ← Deep-dive: JTBD, Mom Test, Lean Canvas, Hook Model, Traction Channels
    └── common-mistakes.md      ← 10 ideation traps with how to address each
```

Reference files are loaded on demand when the user raises a topic that needs more depth. They are not loaded by default.

---

## Phase outputs

### Phase 1 — Idea Health Scorecard
```
[Problem statement]

| Dimension          | Score |
|--------------------|-------|
| Problem clarity    | 🟢    |
| Customer specificity | 🟡  |
| Founder-problem fit | 🔴   |
| Competitive gap    | 🟡    |
| Timing (why now?)  | 🟢    |
| Founder conviction | 🟢    |
```

### Phase 2 — Validation Experiment
```
Hypothesis:         ...
Method:             ...
Who:                ...
Number:             ...
Timeline:           ≤ 2 weeks
Success looks like: ...
Failure looks like: ...
```

### Phase 3 — MVP Plan
```
What it does:       ...
Who it's for:       ...
How it works:       ...
Tools used:         ...
Price:              ...
Ship date:          ...
First 3 customers:  ...
Success metric:     ...

Hook design:
  Internal trigger: ...
  Core action:      ...
  Variable reward:  ...
  Investment:       ...
```

---

## Design decisions

**Why phases are enforced in order:** A weak problem statement makes everything downstream wrong. The skill refuses to scope an MVP before validation, and refuses to validate before the problem is sharp. Every shortcut at the ideation stage costs 10x in execution.

**Why the Hook Model is in Phase 3, not a separate skill:** Retention design should inform feature selection, not follow it. Building the habit loop into the MVP plan ensures it's not an afterthought.

**Why the Manipulation Matrix is a hard gate:** The ethics check is structural, not optional. If the founder is a Dealer (wouldn't use it, doesn't improve lives), the skill stops and names it.

**Why the Idea Health Scorecard replaces a plain problem statement:** Founders need a verdict they can act on, not a sentence to admire. Two or more 🔴 items is a hard stop.

---

## Complementary skills

This skill is upstream of:
- `validate-idea` — deeper validation methodology
- `mvp` — deeper MVP execution guidance
- `first-customers` — finding and converting the first 100 customers
- `marketing-plan` — content and audience strategy post-product-market fit
