# Setting up Nelnet Claude (classic Projects)

Built from the files in this project. Nothing in the package contains Nelnet data, ticket text, or staff names beyond Eric and Dave. Refreshed 2026-10-28 for the settled gate pair and Eric's written answers.

## What is in this folder

| Item | Where it goes |
|---|---|
| `custom-instructions.txt` | Paste into the project's custom instructions box |
| `knowledge-to-upload/` (7 files) | Upload as project knowledge |
| `CLAUDE.md` | Goes in the root of the repo once it exists in the team's GitLab group, for Claude Code |
| `SETUP.md` | This page. Do not upload. |

## Upload list (you have not uploaded anything yet, so upload all seven)

| File | What it holds |
|---|---|
| `01-gate-brief.md` | Gate, Eric's definitions, execution model, constraints, history |
| `02-automation-candidates.md` | Rubric, scores, the settled pair, parked candidates |
| `03-decision-log.md` | Every decision, tagged SETTLED, PROPOSED, or SUPERSEDED |
| `04-templates.md` | Requirements, test plan, maintenance guide, weekly status templates |
| `08-open-questions.md` | Open items with cutoffs, plus the Eric, Dave, automation team, and expert lists |
| `09-gate-plan.md` | Slices, pass/fail criteria, week-by-week plan, Phase 0 steps, both prompts |
| `10-build-plan.md` | Design choices, interfaces, run states, steps S0 to S15 and N1, slice 2 rules |

If the interface only takes text, paste each file as a snippet titled with the file name.

## Steps: the Claude project

1. In Claude, open **Projects** and choose **Create project**. Name it "Gate Automation". Set it private if the option appears.
2. Open the project's instructions ("Set project instructions" or "Custom instructions"). Paste `custom-instructions.txt`. Save.
3. Under **Project knowledge**, choose **Add content** and upload the seven files.
4. Smoke test, in a new chat inside the project. All three should pass:
   - "What is the gate pair and what do deployed and in use mean?" Expect: AUTO-188 Phase 1 weekly check and Phase 3 structure notifier; deployed means runs from a laptop; in use means Eric's team uses the output while I run it; US-only acceptance still open.
   - Paste a step in the wrapper format using step S4 from file 10. Expect PASS or FAIL against the check, with UNKNOWN for guesses.
   - "Here is a ticket: [made-up line]." Expect it to stop you and apply the data rule.
5. If anything fails, tell me which one and I will tighten the instructions.

## Before you ask Nelnet's Claude to do real work
Dave 6 in file 08 asks which tools and data are approved. The instructions stay strict (sanitized only) until Eric or Dave answer. When they do, edit the `[TBD]` block in the instructions and the matching line in `CLAUDE.md`.

## Keeping it current
Classic project files are read-only for Claude. The loop:
1. Claude gives you a one-line decision log entry or an answer.
2. You add it to your local copy of `03-decision-log.md` or `08-open-questions.md`.
3. In the project, remove the old file and upload the new one. Do this when something settles, not every day.

When Eric answers an open item, move it to "Answered or closed" in file 08 and change any `[PROPOSED]` row in file 03 to `[SETTLED]`.

## Steps: Claude Code (when the repo exists)
1. Create the GitLab project in the team's group. Rewrite practice code there in Python 3.13. Do not copy the practice kit in. Pushing needs permission in the group.
2. Put `CLAUDE.md` in the repo root and commit it. Fill in the `[TBD]` lines.
3. Start Claude Code from the repo root. First prompt: "Read CLAUDE.md. Write the test plan for slice 1 before any code."

## What I left out, and why
- **Recruiter, staffing agency, contract, timesheet, and time-off details.** Not for Nelnet systems and irrelevant to the gate.
- **The line about what happens if the gate is missed.** Eric knows it.
- **Ticket text, staff names beyond Eric and Dave, and the phone photos.** Roles only. The fact-sheet prompt in file 09 is how you pull facts out of the ticket inside Nelnet.
- **Personal details about clearance or access status.** Not needed to build.
- **The practice kit.** Code stays out of Nelnet until rewritten there.
