# weatheragent-505

Claude Code (cloud) working repo for INT 505 weather forecasting work. Companion to — not a replacement for — the existing production "Weather Agent" (GAS + Cowork, Script ID `1J799jggM5jOqJ0vQpWtMSsXi-x4YW_jIi6GInbxZ8O1F46dNxqpuWEO-`), which runs daily unattended and is the current source of truth for monitoring. This repo is presently used for ad-hoc/manual briefs and architecture assessment only (status: Option A — keep the existing system, this repo not yet a standing service; see SESSION_LOG.md).

## Fleet CTO Office

This repo participates in Martin's AI fleet (~22 projects). Standing practice for every session working here:

**1. Who coordinates.** The Fleet CTO Office is a separate Claude project — the fleet's architecture/standards/review function. It coordinates, it does not manage: stays out of everyday work, steps in only for cross-project or fleet-level matters. It is not live — it answers when Martin opens it or at its Fleet Weekly Review, so never block on it; continue everything that doesn't depend on its answer. Martin decides WHAT; this project and the office decide HOW — never make Martin a relay, editor or tester.

**2. When to involve the office.** Send a request for: a new agent/project; adding a scheduler, an outbound message channel (mail, Telegram), a credential, or a dependency on another project; a change to a shared fleet component; a hard-to-undo or cross-project-impact action; a technical practice you'd otherwise invent (deploy, install, notifications, verification). Do not send anything for everyday internal work.

**3. Channel** — Google Drive folder `CTO_Office_Exchange` (id `17WVYXzsNa5zU52BnUvF6WaLI5h6yF6kc`). Project name = `weatheragent-505` (repo name).
   - You → office: `CTOREQ_weatheragent-505_<YYMMDD>_<topic>.md` — question/proposal, context, what was already checked, what happens absent a reply, the exact decision needed.
   - Office → you: `CTOREPLY_weatheragent-505_<YYMMDD>_<topic>.md`, plus fleet-wide notices. Check the folder at session start and whenever a request is open, for a matching CTOREPLY and newer fleet notices. Treat a CTOREPLY as a ruling and implement it.
   - To Martin, only when something genuinely needs him: `ATTN_weatheragent-505_<YYMMDD>_<topic>.md`.
   - Session log: at the end of every turn, overwrite `SESSIONLOG_weatheragent-505.md` in that same Drive folder, and copy it to `SESSION_LOG.md` in this repo root and commit. Sections: (1) Goal and decisions so far, (2) What was found and where (Drive files, repo paths), (3) Open items and what each waits on, (4) The exact next step.
   - Fleet facts (Registry, Policy Index, Status Board) live in the Agent Learnings Exchange folder `1Idh9F2GY7WHbF_zkbSgUSR0QIuHGv-cJ` — read the newest version before relying on any fleet fact.
   - If Drive write is unavailable, name the missing tool in the reply and fall back to repo files only.

**4. Standing rules.**
   - Apps Script code changes go through the fleet installer (`Install_Queue`, id `102sHMcmDxnzTUfBXU2k8vL7Q6IpSO3w9`) — never through Chrome or Martin.
   - No secrets in any file.
   - Drive first, Chrome last — design so nothing depends on Martin's desktop/Chrome or presence. Request every permission once, at the scope of the repeating task; do everything up to the click, then one link and one word.
   - Scheduled tasks: completion notifications off by default; approval mode decided when the task is created.
   - Numbered lists only. Complete replacement texts, never fragments. UI labels in English. Versions as `YYMMDD_vN.n`.
   - Every reply/run that reports work ends with 1–2 plain sentences to Martin and `ACTION NEEDED: None` or `ACTION NEEDED: Yes` + minimal numbered steps only he can do. Name the specific missing tool before writing "Yes".

Full instruction text: see `CTOREQ_weatheragent-505_260928_onboarding.md` in the Exchange folder for the message this section was distilled from, and `SESSIONLOG_weatheragent-505.md` for current state.
