---
name: ad-generator
description: Generate ad copy for any platform with headline variations, body copy, and CTAs optimized per placement
argument-hint: "[product]"
---

# Ad Generator

Write ads that don't sound like ads. Generates platform-optimized ad copy
for Facebook, Google, LinkedIn, and X (Twitter).

## Usage

```
/ad-generator <product or offer description>
```

The user provides a product, service, or offer. You produce ready-to-use ad
copy for each platform.

## Process

1. **Parse the input** — Identify the product/service, key value prop, target
   audience (if stated), and tone (if stated). If critical info is missing,
   ask one clarifying question before generating.

2. **Generate per platform** — For each of the four platforms below, produce:
   - 3 headline variations (within character limits)
   - 1 body copy block (within character limits)
   - 2 CTA options

3. **Output format** — Use the template in the Output Template section below.

## Platform Specs

### Facebook / Instagram
- **Primary text**: 125 characters visible (up to 1,000 before truncation)
- **Headline**: 27 characters visible (max 40)
- **Description**: 27 characters visible (max 30)
- **Tone**: Conversational, scroll-stopping, benefit-led
- **Tips**: Lead with a hook or question. Avoid corporate speak. Use social
  proof when possible.

### Google Ads (Responsive Search)
- **Headlines**: 30 characters each (provide 3)
- **Descriptions**: 90 characters each (provide 1-2)
- **Tone**: Direct, intent-matching, keyword-aware
- **Tips**: Front-load value. Include numbers or specifics. Match likely
  search intent.

### LinkedIn
- **Introductory text**: 150 characters visible (up to 600 before truncation)
- **Headline**: 70 characters max
- **Tone**: Professional but human. Thought-leadership angle.
- **Tips**: Speak to the job-to-be-done. Reference industry pain points.
  Avoid buzzwords.

### X (Twitter)
- **Post text**: 280 characters max
- **Tone**: Punchy, opinionated, native to the feed
- **Tips**: Write like a person, not a brand. One strong idea per ad. CTAs
  should feel natural, not forced.

## Writing Principles

- **No corporate fluff** — Cut "leverage", "synergy", "best-in-class",
  "revolutionize". Write like a human.
- **Benefit over feature** — Don't say what it does. Say what changes for
  the reader.
- **One idea per ad** — Each variation should hammer one clear point.
- **Platform-native** — Each platform has its own voice. A LinkedIn ad should
  never read like a tweet and vice versa.
- **Specificity wins** — Numbers, timeframes, and concrete outcomes beat
  vague promises.

## Output Template

```markdown
## Facebook / Instagram

**Headline 1:** [headline]
**Headline 2:** [headline]
**Headline 3:** [headline]

**Body:**
[primary text — conversational, benefit-led, 1-3 short sentences]

**CTA 1:** [cta]
**CTA 2:** [cta]

---

## Google Ads

**Headline 1:** [headline — 30 chars max]
**Headline 2:** [headline — 30 chars max]
**Headline 3:** [headline — 30 chars max]

**Description 1:** [description — 90 chars max]
**Description 2:** [description — 90 chars max]

---

## LinkedIn

**Headline 1:** [headline]
**Headline 2:** [headline]
**Headline 3:** [headline]

**Body:**
[introductory text — professional but human, pain-point aware]

**CTA 1:** [cta]
**CTA 2:** [cta]

---

## X (Twitter)

**Ad 1:** [full tweet — 280 chars max, includes CTA naturally]

**Ad 2:** [full tweet — 280 chars max, includes CTA naturally]

**Ad 3:** [full tweet — 280 chars max, includes CTA naturally]
```

## Tone Modifiers

If the user specifies a tone, adjust all copy accordingly:

| Modifier | Effect |
|----------|--------|
| `--bold` | Confident, slightly provocative, pattern-interrupt |
| `--minimal` | Ultra-short, whitespace-heavy, understated |
| `--data` | Lead with numbers, stats, proof points |
| `--story` | Narrative-driven, before/after framing |
| `--urgent` | Time-bound, scarcity-driven (use sparingly) |

Default tone when none specified: conversational and benefit-led.
