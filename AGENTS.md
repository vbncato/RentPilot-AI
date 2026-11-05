# AGENTS.md — RentPilot AI

## Project purpose
Read `docs/PROJECT_CHARTER.md` first. It is the authoritative product mandate.
The first deliverable is a private, personal rental assistant for use in Poland.
Only after it works, is tested, and is documented should it be prepared for public use.

## Team roles
- Founder / Product Owner: the user. The user approves product scope and material changes.
- ChatGPT: CTO / architect; prepares specifications and reviews architectural consistency.
- Claude Code: primary implementation agent.
- Codex: independent reviewer and code explainer. Default to review/read-only work; do not silently modify implementation during an audit.

## Non-negotiable rules
1. Do not invent requirements. Identify assumptions and mark them as assumptions.
2. Do not make unapproved architectural changes. Changes to module boundaries, database schema, dependencies, security model, data sources, deployment model, or public API require a written proposal and explicit user approval before implementation.
3. Every implementation task must have: scope, allowed files, prohibited changes, acceptance criteria, and tests.
4. Before editing, inspect the relevant existing code and documentation. Do not replace or rewrite unrelated files.
5. Prefer small, reviewable changes over broad rewrites.
6. Never claim tests passed unless they were actually run; report exact commands and results.
7. Do not invent data from listings. Unknown costs or fields must remain explicitly unknown.
8. Preserve source attribution and respect source access rules and terms. Do not bypass access controls.
9. Never expose, print, commit, or request secrets. Keep tokens, API keys, `.env`, Telegram session files, and personal data out of Git.
10. Explain material changes in plain Russian so the beginner owner can understand and discuss them in an interview.

## Workflow for implementation agents
1. Read this file and the relevant documents in `docs/`.
2. Inspect repository status and current implementation.
3. Produce a concise plan before making changes.
4. If the task touches an approval-gated area, stop and request approval.
5. Implement only the approved scope.
6. Run relevant tests and quality checks available in the repository.
7. Summarize changed files, behavior, commands run, results, known limitations, and follow-up risks.

## Workflow for Codex review
- Review the proposed diff independently against the task and project documentation.
- Prefer findings with severity, file path, line reference, impact, and reproduction or reasoning.
- Separate confirmed defects from suggestions and uncertain concerns.
- Do not edit files during a review unless the user explicitly changes the task from review to implementation.
- Check correctness, edge cases, error handling, security, data integrity, test coverage, and architectural drift.

## Beginner-friendly communication
- Use Russian unless the user asks otherwise.
- Explain unfamiliar concepts briefly and concretely.
- Do not overwhelm the user with multiple setup steps at once.
- Distinguish what is complete, what is proposed, and what remains unverified.

## Current project status
- This repository is a scaffold only. No application architecture or framework has been approved yet.
- Do not add frameworks, services, dependencies, or deployment infrastructure without a task specifying why they are needed.
