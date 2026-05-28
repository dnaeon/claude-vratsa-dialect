# claude-vratsa-dialect

A Claude Code skill that switches Claude's responses into the **northwest Bulgarian (Vratsa) dialect** — the speech of "пустиняците" and the comedy character **Гацо Бацо** (played by Краси Радков).

> Жик так, баце!

## What it does

When you invoke `/vratsa-dialect`, Claude starts replying in the Vratsa dialect for the rest of the session:

- **Pronouns**: "я" instead of "аз", "сакам" instead of "искам"
- **Future tense**: "че" instead of "ще" (NOT "ке" — that's a different dialect)
- **Verbs**: drop the "х" in ходя forms → "одиме", plus regional verbs like "зирна", "глъчим", "ландзим"
- **Word order**: subjects move to the end, pronouns reorder around the verb, hedges like "може би" / "едва ли не" get injected mid-sentence
- **Vocabulary**: рикия (not ракия), баце, ептем, пустиняк, клапавци, мачка, мундза, and ~50 more words
- **Persona**: warm, teasing, philosophical, slightly self-deprecating — the Гацо Бацо attitude

Technical accuracy is preserved; the dialect is a wrapper, not an excuse for vagueness.

## Install

### As a personal skill (recommended — works in all your projects)

```bash
git clone https://github.com/<your-username>/claude-vratsa-dialect ~/.claude/skills/vratsa-dialect
```

### As a project skill (works in one repo)

```bash
git clone https://github.com/<your-username>/claude-vratsa-dialect <your-repo>/.claude/skills/vratsa-dialect
```

Claude Code picks up the skill automatically — no restart needed if `~/.claude/skills/` already exists. If it doesn't, restart Claude Code once after creating it.

## Usage

```text
/vratsa-dialect
```

Claude confirms with "Жик так, баце — фанах те!" and stays in dialect for the rest of the session.

To switch back to standard language:

```text
/vratsa-dialect off
```

…or just ask Claude to stop, switch to English, etc.

## Files

- `SKILL.md` — main skill file (the rules Claude follows when activated)
- `vocabulary.md` — full vocabulary list, word-order patterns, Гацо Бацо persona, рикия culture

## Background

The Vratsa dialect is spoken in the Vratsa region of northwestern Bulgaria. Wikipedia describes it as "a transition between Sofia, Botevgrad and Danube Plain dialects" — masculine definite article ends in **-о** ("гърбо"), and uses "мги" instead of "им" for third-person plural dative.

**Гацо Бацо** is a beloved comedy character by Bulgarian actor Краси Радков — a satirical Vratsa footballer who speaks in the dialect and embodies the regional humor: simple pleasures, exaggerated bravado, fatalistic wisdom ("нема ли кръв, нема фал, я така играем").

## License

Do whatever you want with it, баце.
