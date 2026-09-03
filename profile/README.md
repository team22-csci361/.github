<h1 align="center">CSCI 361 — Team 22</h1>
<p align="center"><i>Software Engineering Project Documentation</i></p>

<p align="center">
  <a href="#project-structure">Project Structure</a> •
  <a href="#workflow">Workflow</a> •
  <a href="#branching-strategy">Branching</a> •
  <a href="#commit-convention">Commits</a> •
  <a href="#issues">Issues</a> •
  <a href="#pull-requests">Pull Requests</a>
</p>

---

## Project Structure

The system is split across three repositories, each owning a distinct layer of the platform.

| Repository | Responsibility | Documentation |
|---|---|---|
| [`backend`](../backend) | API, business logic, database | [Backend docs](../backend#readme) |
| [`frontend`](../frontend) | Web application | [Frontend docs](../frontend#readme) |
| [`mobile`](../mobile) | Mobile application | [Mobile docs](../mobile#readme) |

Each repository maintains its own README with setup instructions, architecture notes, and module-level detail. This page only covers how we work **across** repositories as a team.

---

## Workflow

All work is tracked on the **Master Board**. No code should be written for a task that isn't represented there — if it's not on the board, it doesn't exist.

| Column | Meaning |
|---|---|
| `To Do` | Ready to be picked up this sprint |
| `In Progress` | Actively being worked on (max 1–2 cards per person) |
| `In Review` | PR is open and waiting for approval |
| `Done` | Merged into `dev` and verified |

**Rules of thumb:**
- Move your card to `In Progress` the moment you start, not after you finish.
- A card only moves to `In Review` once a PR actually exists and is linked to it.
- Nobody moves someone else's card except to `Done`, after confirming the PR is merged.

---

## Branching Strategy

| Branch | Purpose |
|---|---|
| `main` | Production-ready code only. Protected — no direct pushes. |
| `dev` | Integration branch. All feature work merges here first. |
| `feature/<short-description>` | New functionality, branched from `dev` |
| `bugfix/<short-description>` | Non-urgent fixes, branched from `dev` |
| `hotfix/<short-description>` | Urgent production fixes, branched from `main` |
| `testing/<short-description>` | Experimental or QA-only branches |

**Naming examples:**
```
feature/user-authentication
bugfix/fix-null-pointer-on-login
hotfix/patch-payment-crash
```

`dev` merges into `main` only at release points, and only after testing passes.

---

## Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <short description>
```

| Type | Use for |
|---|---|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `style` | Formatting, no logic change |
| `refactor` | Code change that's neither a fix nor a feature |
| `test` | Adding or fixing tests |
| `chore` | Build process, tooling, dependencies |

**Example:**
```
feat(auth): add JWT token refresh endpoint
fix(cart): resolve incorrect total calculation
```

Keep commits small and focused — one logical change per commit.

---

## Issues

Every task starts as an issue, created from the **Issue Template**. Do not skip fields.

**Title format:** `[TYPE] Short, clear summary`
Example: `[FEATURE] Add password reset flow`

**Template sections:**
- **Description** — what needs to be done and why
- **Acceptance Criteria** — a checklist defining "done"
- **Related Board Card** — link to the Master Board card
- **Labels** — type (`feature`, `bug`, `docs`, etc.) and priority

_Once created, assign yourself, add it to the Master Board, and move it to `To Do` or `In Progress`._

---

## Pull Requests

**Before opening a PR:**
1. Branch from the correct base (`dev` for regular work, `main` only for hotfixes).
2. Rebase or merge the latest `dev` into your branch to avoid conflicts.

**PR description template:**
- **Summary** — what this PR does, in one or two sentences
- **Related Issue** — `Closes #<issue-number>`
- **Changes** — bullet list of what changed
- **Testing** — how you verified it works

_Once you created PR, assign it to the corresponding issue that this PR closes._

**Review rules:**
- At least **one approval** is required before merging.
- No self-merging, even for small changes.
- All review comments must be resolved or discussed before merge.
- Use **Squash and Merge** to keep history clean.
- Delete the branch after merging.

---

<p align="center"><sub>Maintained by Team 22 — CSCI 361</sub></p>
