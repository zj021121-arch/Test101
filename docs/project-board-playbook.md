# Project Board Playbook

This repository follows the AI-human board workflow used in GitHub Projects:

- Start execution only from `To Do`
- Validate readiness before `In Progress`
- Use `Pull Request` and `Review` for feedback cycles
- Move to `Testing` after integration
- Move to `Done` only after verification
- Move to `Blocked` immediately when external dependencies stall progress

## Status Rules

1. Human board moves are authoritative signals.
2. If required inputs are missing, request clarification and do not start coding.
3. Treat review comments as a concrete action checklist.
4. Re-check issue edits before major implementation changes.

## Suggested View Tabs (Manual UI setup)

GitHub API currently does not expose view creation mutations for Project V2, so create these tabs once in the UI:

### AI-Human Task Pipeline
- `TP-Task Board` (Board, grouped by Status)
- `TP-Ready Queue` (Status=To Do, Lane=Intake)
- `TP-Review & QA` (Status in Pull Request/Review/Testing)
- `TP-Blocked` (Status=Blocked)

### AI-Human Information Hub
- `IH-Knowledge Base` (Lane in Requirements/References)
- `IH-Decision Log` (Lane=Decisions)
- `IH-Actionable Info` (Status=To Do)

### AI-Human Communication Desk
- `CD-Clarification Queue` (Lane=Clarifications, Status!=Done)
- `CD-Feedback Tracker` (Lane=Feedback)
- `CD-Broadcast Notes` (Lane=Announcements)