# Skill Efficiency Reviewer

A reusable Codex skill for reviewing, scoring, improving, and optionally updating other Codex skills.

Use it when you want a clear systems audit of a skill before you trust it, share it, or make it part of your daily workflow.

## What It Does

Skill Efficiency Reviewer checks a Codex skill for:

- clarity
- reusability
- workflow logic
- practicality
- output quality
- scalability
- maintainability
- update potential

It returns a concise, operator-friendly review with a score out of 10 and a clear update decision.

## Who It Is For

This is useful if you:

- build your own Codex skills
- install skills from other people
- want to improve a weak skill
- want to make a skill more reusable
- want a quick quality check before sharing a skill publicly

## Install

1. Download or clone this repository.
2. Copy the skill folder into your Codex skills directory:

```bash
mkdir -p "$HOME/.codex/skills/skill-efficiency-reviewer"
cp ./skill.md "$HOME/.codex/skills/skill-efficiency-reviewer/SKILL.md"
cp -R ./agents "$HOME/.codex/skills/skill-efficiency-reviewer/" 2>/dev/null || true
```

3. Restart Codex.
4. Search for `Skill Efficiency Reviewer` in your skills list.

## Important File Note

This repo uses `skill.md` for simple GitHub browsing.

Codex expects the installed skill file to be named:

```txt
SKILL.md
```

That is why the install command copies `skill.md` into your Codex skills folder as `SKILL.md`.

## Example Prompt

```txt
Use $skill-efficiency-reviewer to review this skill:

/Users/you/.codex/skills/website-safety-auditor/SKILL.md
```

You can also paste a full skill directly into Codex and ask:

```txt
Review this Codex skill for efficiency, clarity, workflow quality, and update potential.
```

## Review Output

The skill returns a compact audit:

- overall rating
- quick verdict
- strengths
- weaknesses
- efficiency summary table
- key problems
- recommended improvements
- upgrade potential
- update decision

See [examples/sample-review-output.md](examples/sample-review-output.md).

## Updating Reviewed Skills

The skill does **not** update another skill automatically.

At the end of every review, it asks:

```txt
Would you like this skill to be updated?

1. Yes — Rewrite and improve the skill
2. No — Keep current version
3. Suggest changes first
```

It only edits the reviewed skill if the user clearly approves the update.

## License

MIT License. See [LICENSE](LICENSE).
