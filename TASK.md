# TASK.md - ACP Agent Relay State

## Current Agent
- **Agent:** codex-personal
- **Model:** codex/gpt-5.4 (extra-high thinking)
- **Workspace:** personal

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
| codex-business | TBD | add hello.py, handoff to codex-personal |

## Next Steps
- [ ] 建立 hello2.py，內容：print("Hello from codex-personal")
- [ ] 更新 TASK.md，把 Current Agent 改成 claude-opus
- [ ] commit + push，然後開 Claude Code 接力

## Notes
- This is a relay test. No real task assigned yet.
- Prove the handoff mechanism works cleanly.
