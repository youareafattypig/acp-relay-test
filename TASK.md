# TASK.md - ACP Agent Relay State

## Current Agent
- **Agent:** DONE ✅ relay test complete
- **Model:** —
- **Workspace:** —

## Relay Order
1. `codex-business` — Codex 5.4 extra-high, 商業空間 ← **YOU ARE HERE**
2. `codex-personal` — Codex 5.4 extra-high, 個人空間
3. `claude-opus`    — Claude Code Opus 4.6

## Handoff Protocol
When token quota is low (or task segment done):
1. Update this file: set next agent in "Current Agent"
2. Write a clear "Next Steps" section below
3. `git add -A && git commit -m "handoff: codex-business -> codex-personal [reason]"`
4. `git push`
5. Switch workspace: `bash ~/.codex/codex-switch.sh personal` (or open Claude Code)
6. New agent: `git pull`, read TASK.md, continue

## Task Log
| Agent | Commit | Summary |
|-------|--------|---------|
| - | init | repo created, TASK.md initialized |
| codex-business | 41edbac | add hello.py, handoff to codex-personal |
| codex-personal | 0cc0df0 | add hello2.py, handoff to claude-opus |
| claude-opus | TBD | add hello3.py, relay test complete |

## Next Steps
✅ Relay test complete. All 3 agents handed off successfully via git.

## Notes
- This is a relay test. No real task assigned yet.
- Prove the handoff mechanism works cleanly.
