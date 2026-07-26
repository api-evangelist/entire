---
name: Entire Skills
description: >-
  Provider-published, cross-agent Agent Skills that help coding agents use Entire
  context from Checkpoints, sessions, and git history to search past work, explain
  code, and hand off sessions.
api: none  # Entire exposes no public REST API; skills operate via the Entire CLI
source: https://github.com/entireio/skills
install: npx skills add https://github.com/entireio/skills --all
operations: []  # CLI-grounded, not OpenAPI operationIds
---

# Entire Skills (published by Entire)

These are the official cross-agent skills shipped by Entire, captured verbatim from
`github.com/entireio/skills`. Install all with `npx skills add https://github.com/entireio/skills --all`,
or a single skill with `npx skills add https://github.com/entireio/skills --skill <name>`.

Each skill drives the Entire CLI (`entire ...`) against a repo that has Entire capture
enabled (`entire enable`) and an authenticated session (`entire login`).

## search
Finds prior work in Entire history by topic, repo, branch, author, or time window.

## explain
Looks up the session behind a function, file, or line to explain the requirements and
decisions that produced it.

## what-happened
Traces the latest change to a file line or range using git blame plus Checkpoint context.

## session-handoff
Reads saved or active session context so another agent can pick up task state where the
last one left off.

## review
Reviews code changes on the current branch using Checkpoint transcripts to understand
developer/agent intent behind the diff.

## using-entire
Orchestrator skill for codebase exploration that routes user intent to the appropriate
sub-skill above.

## session-crosslink
Links agent sessions that ran outside the repo to the affected Entire-enabled repos'
HEAD commits.
