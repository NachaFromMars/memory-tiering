# memory-tiering — HOT / WARM / COLD three-tier memory management

> Keep agent context lean without losing what matters. Active work stays HOT, stable facts settle into WARM, and distilled history archives to COLD.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
memory-tiering brings structured three-layer memory management to OpenClaw agents. Each tier has its own file, clear promotion/demotion rules, and a distinct lifecycle. The workflow audits incoming information, redistributes it across tiers, prunes completed work, and verifies nothing important is lost — preventing context bloat while preserving continuity.

## Features
| Tier | File | Holds | Lifecycle |
|---|---|---|---|
| 🔥 HOT | `memory/hot/HOT_MEMORY.md` | Current session, active tasks, immediate goals | Prune aggressively when done |
| 🌡️ WARM | `memory/warm/WARM_MEMORY.md` | User preferences, stable configs, recurring interests | Update when preferences change |
| ❄️ COLD | `MEMORY.md` | Long-term archive, decisions, milestones, lessons | Summaries only |

**Workflow:** ingest & audit → redistribute tiers → prune & summarize → verify no loss
- Move to HOT: needed in next 2–3 turns
- Move to WARM: new permanent facts
- Move to COLD: completed high-level summaries

## Trigger Keywords (OpenClaw)
organize memory, memory compaction, memory loss, context full, tier memory, hot warm cold memory

## Related Skills
- [openclaw-mem](https://github.com/NachaFromMars/openclaw-mem) — session-first memory curator
- [context-budgeting](https://github.com/NachaFromMars/context-budgeting) — context window management

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
