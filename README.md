# Lao Da Skill

A Codex skill for cold, high-standard coaching inspired by Kobe Bryant's public Mamba Mentality material.

This skill is built for users who want:

- tougher feedback
- higher standards
- direct decision coaching
- setback recovery without self-pity
- process-first replies instead of vague motivation

It does **not** impersonate Kobe Bryant. It uses a Kobe-inspired coaching framework based on public interviews, speeches, and writing.

## What It Does

`laoda-skill` helps Codex respond like a demanding coach:

- blunt but not abusive
- intense but still safe
- focused on reps, standards, and execution
- better for action than comfort

It includes:

- a reusable skill definition in [SKILL.md](./SKILL.md)
- voice and phrase templates in [references/voice-templates.md](./references/voice-templates.md)
- few-shot examples in [references/few-shot-dialogues.md](./references/few-shot-dialogues.md)
- a distilled decision system in [references/decision-system.md](./references/decision-system.md)
- source manifests and collection outputs for corpus-building
- scripts for harvesting public pages and YouTube transcript sources

## Install

Copy the skill folder into your Codex skills directory:

```powershell
Copy-Item -Recurse .\laoda-skill "$HOME\.codex\skills\laoda-skill"
```

Or clone this repo and copy the folder:

```powershell
git clone https://github.com/GoSim7/laoda-skill.git
Copy-Item -Recurse .\laoda-skill "$HOME\.codex\skills\laoda-skill"
```

On this machine, the installed skill lives at:

`C:\Users\Administrator\.codex\skills\laoda-skill`

## How To Use

Ask Codex to use `laoda-skill` when you want stronger coaching.

Example prompts:

- `Use laoda-skill and review my plan.`
- `Use laoda-skill. Be harsher.`
- `Use laoda-skill in Lao Da mode and tell me what I'm doing wrong.`
- `Use laoda-skill to help me recover after failing a launch.`

Good use cases:

- productivity
- discipline
- business decisions
- creative consistency
- performance reviews
- failure recovery

## Modes

The skill supports several tones:

- `film-room`: analytical and precise
- `locker-room`: forceful and urgent
- `late-night reset`: steady and demanding
- `laoda`: the hardest safe mode

If you want maximum pressure, ask for:

- `Lao Da mode`
- `go harder`
- `be harsher`

## Corpus And Source Engineering

This repo also includes a lightweight source pipeline.

Main files:

- [references/source-manifest.json](./references/source-manifest.json)
- [references/source-notes.md](./references/source-notes.md)
- [references/collected-sources-v2.jsonl](./references/collected-sources-v2.jsonl)
- [scripts/harvest_public_sources.py](./scripts/harvest_public_sources.py)
- [scripts/discover_youtube_sources.py](./scripts/discover_youtube_sources.py)

Example:

```powershell
python .\scripts\harvest_public_sources.py .\references\source-manifest.json --output .\references\collected-sources-v2.jsonl
```

## Boundaries

This skill is intentionally constrained.

- It does not claim to be Kobe Bryant.
- It does not fabricate private memories or personal anecdotes.
- It avoids abusive or degrading language.
- It drops the hard-coach tone when safety matters.

## Repo

GitHub:

[https://github.com/GoSim7/laoda-skill](https://github.com/GoSim7/laoda-skill)
