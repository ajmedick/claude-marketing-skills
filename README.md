# Claude Marketing Skills

Custom [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skills for marketers. Generate platform-ready ad copy, campaigns, and more — directly from your terminal or VS Code.

## Skills

### Ad Generator

Generate ad copy for Facebook, Google, LinkedIn, and X (Twitter) in one command. Each platform gets properly formatted output with character limits respected.

**What you get per platform:**
- 3 headline variations (within platform character limits)
- Body copy / descriptions
- 2 CTA options

**Supported platforms:**

| Platform | Headlines | Body | Tone |
|---|---|---|---|
| Facebook / Instagram | 40 chars | 125 chars visible | Conversational, scroll-stopping |
| Google Ads (RSA) | 30 chars | 90 chars | Direct, intent-matching |
| LinkedIn | 70 chars | 150 chars visible | Professional but human |
| X (Twitter) | — | 280 chars | Punchy, opinionated |

**Usage:**

```
/ad-generator "Your product or offer description"
```

**Tone modifiers:**

```
/ad-generator "Your product" --bold      # Provocative, pattern-interrupt
/ad-generator "Your product" --minimal   # Ultra-short, understated
/ad-generator "Your product" --data      # Numbers and proof points
/ad-generator "Your product" --story     # Narrative, before/after framing
/ad-generator "Your product" --urgent    # Scarcity-driven
```

## Installation

**1. Clone this repo:**

```bash
git clone https://github.com/ajmedick/claude-marketing-skills.git ~/claude-marketing-skills
```

**2. Symlink the skills you want into your Claude Code skills directory:**

```bash
# Create the skills directory if it doesn't exist
mkdir -p ~/.claude/skills

# Symlink ad-generator
ln -s ~/claude-marketing-skills/ad-generator ~/.claude/skills/ad-generator
```

**3. That's it.** Open Claude Code (VS Code extension or CLI) and the skills are available immediately. No restart needed.

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (VS Code extension or CLI)

## Updating

Pull the latest changes and your symlinked skills update automatically:

```bash
cd ~/claude-marketing-skills && git pull
```

## Contributing

To add a new skill, create a folder with a `SKILL.md` file:

```
your-skill-name/
  SKILL.md
```

The `SKILL.md` needs YAML frontmatter with at minimum a `name` and `description`, followed by the skill instructions in markdown. See [ad-generator/SKILL.md](ad-generator/SKILL.md) for an example.
