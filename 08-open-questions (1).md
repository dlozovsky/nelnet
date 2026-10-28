# Open Questions Tracker

Updated 2026-10-28. Labels (Eric 2, Dave 4, Expert 3) are what the gate plan and build plan refer to. Record sanitized answers only: counts, dates, field names, rules, yes or no. No ticket text, no names beyond Eric and Dave.

**Priority:** Critical = decides scope, acceptance, or feasibility. High = shapes the build. Secondary = refines build and handoff.
**Rule:** an unanswered question escalates to Eric on Teams at its cutoff. A recommendation is a proposal, never a build rule. The dependent step holds until the owner answers.

## Open items with cutoffs
Dates are placeholders until Eric emails the clock start (T0), then rebaseline.

| Open item | Blocks | Recommendation to put forward | Owner | Ask by | If unanswered |
|---|---|---|---|---|---|
| S0: is building during onboarding, before the clock starts, authorized, and does scaffolding before the expert walk-through fit the ticket's Phase 0 rule? | Every build step before T0 | Scaffolding with synthetic data only; real rules wait for the expert | Eric | Today | Nothing before T0 starts. Documentation steps A1 to A5 and A7 continue |
| Does a US-only first release qualify, or does Eric require NULSC for acceptance? (He did not answer on Oct 27) | N1, the NULSC half of the structure report, the acceptance bar | Get written approval that US-only qualifies, with NULSC validated and added only when access allows. If NULSC is required, N1 moves to week 1 and both slices wait on authorization | Eric | Today | Ask again; blocker on Teams Nov 6 |
| Is this laptop, the Confluence destination, and the email recipient list authorized for NULSC information? | Anything NULSC | Written confirmation from Eric or the security owner of what may be handled where. No NULSC data touches the laptop, Confluence, or email until then | Eric, with the security owner | Today | Blocker on Teams Nov 6. Everything NULSC stays out of the build and gate evidence |
| Who is notified for a finding (assignee, else reporter, else initiative owner), and is the fix deadline one week or two? | B2, notifier template, notifier dry run | Assignee, else reporter, with two weeks. A proposal for the expert and Eric, not a build rule | Expert, Eric settles a disagreement | Through the expert by Nov 3 | Escalate to Eric Nov 6. Notifier build holds. Page and rules continue |
| Access: Jira read, search and comment on the report projects; Confluence space and parent page; send-as for the team mailbox | S12, S13 in week 1; real send in week 3 | Personal accounts for the gate, service accounts later. Send-as for my own account | Eric and the automation team | Requests out today. Chase Oct 30 and Nov 2 | Blocker on Teams Nov 4 if Jira and Confluence are not in hand. Raise send-as with Eric by Nov 11 |
| Which Confluence Data Center space and parent page do real runs publish to? | S13, real publish in week 2 | Data Center is the gate path (Dave). Build the DC client first; Cloud stays a setting | Dave | Today | Blocker on Teams Nov 4 if no test space and parent page |
| Does Eric approve the sent-messages limitation (duplicate delivery possible if the process stops between delivery and recording)? | First real send, week 3 | Accept it, with uncertain-send reconciliation steps in the maintenance guide | Eric | Nov 6 | First real send holds. The expert sends our drafts and that is recorded |

## Answered or closed
| Question | Answer | Source | Date |
|---|---|---|---|
| Which two automations? | Option (a): AUTO-188 Phase 1 weekly check and Phase 3 structure notifier. AUTO-56 out of the gate | Eric | 2026-10-27 |
| What does deployed mean? | Working off a Nelnet laptop. No hosting, runner, or unattended service identity | Eric | 2026-10-27 |
| What does in use mean? | Eric's team uses the output (page and emails) while Daniel runs it. Negotiable for each phase | Eric | 2026-10-27 |
| Who maintains after handoff? | Daniel first, then Eric's team including Dave | Eric | 2026-10-27 |
| When does the clock start and how is it recorded? | Eric emails the date after security training. Keep the email | Eric | 2026-10-27 |
| Where does code live? | The team's GitLab group | Eric | 2026-10-27 |
| Can a script call Claude? | Enterprise API access exists. Key route open (Eric 5). Not on the gate path | Eric | 2026-10-27 |
| Which Confluence? | Data Center now. Cloud move Q1 2027. Cloud sandbox for dev and testing only | Dave | 2026-10-27 |
| Build language | Python 3.13 from the company software portal | Daniel | 2026-10-26 |
| Does the automation team's runner question matter now? | Not on the gate path. Runner reach goes to the team that already uses a runner with Jira; secrets go to the automation team | Eric | 2026-10-27 |

## Eric
| # | Question | Priority | Answer | Answered by | Date |
|---|---|---|---|---|---|
| Eric 1 | Gate pair | Critical | Closed: option (a) | Eric | 2026-10-27 |
| Eric 2 | What evidence of use does Eric want for "in use" (how many people, how often, how recorded) and who signs off? | Critical | Partly answered: his team uses the output while I run it. Final bar is Eric's. [TBD] | | |
| Eric 3 | Is a US-only first release acceptable, and is the second page set the federal side? | Critical | Partly answered: nearly everything touches NULSC, build US first. Acceptance still open | | |
| Eric 4 | Does November 20 still stand? | Critical | Clock start answered. The November 20 line was cut off in the reply. [TBD] | | |
| Eric 5 | How do I get a Claude API key, and who approves it? (The two slices do not need one.) | Secondary | | | |
| Eric 6 | Is deterministic automation enough for the gate, or should AI show in it? | High | Implied by option (a): no model call. [TBD: confirm] | | |
| Eric 7 | Is Python acceptable? The ticket's estimate assumed Java. | High | | | |
| Eric 8 | Do you confirm the ticket's design: one message per team lead, and each report keeps its Confluence page? | High | | | |
| Eric 9 | Are we running sprints, is status daily or weekly, and does the weekly 1:1 stand? | Secondary | | | |
| Eric 10 | When is the hosting meeting, and is there a dev or test Jira project? | Secondary | | | |
| Eric 11 | When is the Jira cloud migration expected? | Secondary | | | |

## Dave
| # | Question | Priority | Answer | Answered by | Date |
|---|---|---|---|---|---|
| Dave 1 | Jira emails go to my personal address. Who switches that to my Nelnet address, and when? | High | | | |
| Dave 2 | Can you introduce me to the Jira administrator, the owner of the Confluence space, and the owner of the shared team mailbox? I need the access list from the ticket, starting with the SharePoint instructions folder and read access to the team directory project. | Critical | | | |
| Dave 3 | Does Jira Data Center use personal tokens or service accounts? (Also asked of the automation team, Auto 1) | Critical | | | |
| Dave 4 | Can you introduce me to the expert for the weekly, structure, and risk reports and get me an hour with them? | Critical | | | |
| Dave 5 | Which address will the notifier send from? (Eric is submitting send-as.) | Critical | | | |
| Dave 6 | Are a meeting-assistant app and phone photos of the screen allowed? What should I use for call notes? Which AI tools are approved for Nelnet work? | High | | | |
| Dave 7 | Is there a project-to-team-lead list, and where does it live? | High | | | |
| Dave 8 | Who owns Power Automate, and can it reach Jira Data Center? | Secondary | | | |
| Dave 9 | Who is the contact for the Windows server that would host a UI later? | Secondary | | | |

## Automation team (7 questions, Eric said ok)
Auto 1 to 3 block the first runs. Auto 4 to 7 are for later, when this runs unattended.

| # | Question | Priority | Answer | Answered by | Date |
|---|---|---|---|---|---|
| Auto 1 | Where may I store a personal token for Jira and Confluence on my laptop for a pilot (environment variable, credential manager, something else)? Does Jira Data Center accept personal access tokens, or only service accounts? | Critical | | | |
| Auto 2 | What is the preferred way to send email from an automation (SMTP relay, Graph, Power Automate), and how is send-as on a shared mailbox granted? | Critical | | | |
| Auto 3 | Can I install pytest on the laptop from pip or a package mirror? | Critical | | | |
| Auto 4 | How do I request a service account for Jira and Confluence Data Center? Who approves, what is the lead time, and which scopes (read, comment, create page)? | Secondary | | | |
| Auto 5 | Can a GitLab runner reach Jira, Confluence, and email? If not, what request is needed? | Secondary | | | |
| Auto 6 | Where should a scheduled Python automation live (Windows server, AWS, shared runner), who approves it, and where are secrets stored for scheduled runs? | Secondary | | | |
| Auto 7 | What monitoring or alerting is expected, and where do failures get reported? | Secondary | | | |

## Report owner (Program Office), for the weekly, structure, and risk reports (after the intro)
The owner's own 8 questions are merged in. Overlaps: their 1 is Expert 7 (with Expert 4), 2 is Expert 8, 3 is Expert 3, 4 is Expert 9, 5 is Expert 10, 6 is Expert 6, 7 is Expert 11, 8 is Expert 12.
| # | Question | Priority | Answer | Answered by | Date |
|---|---|---|---|---|---|
| Expert 1 | Who reads the weekly required-fields results, and what do they do when a validator fails? | Critical | | | |
| Expert 2 | What is the structure report's US scope, and what is the required-field check for CAB approval? | Critical | | | |
| Expert 3 | When is the next scheduled send, and when are the next two structure sends and the next weekly run? How many hours does a run take today? | Critical | | | |
| Expert 4 | How do you decide today which lead gets which finding, and where does that list live? | Critical | | | |
| Expert 5 | What should happen to a finding with no known lead? | High | | | |
| Expert 6 | For the weekly report: which filters and required fields does it use, where is the saved filter defined, and where is it published? | Critical | | | |
| Expert 7 | Who receives the notification for each flagged item: assignee, reporter, or initiative owner? Many items are unassigned. This blocks slice 2 (C5). | Critical | | | |
| Expert 8 | Does the notification state one week or two to fix? The page says one, the email says two. | High | | | |
| Expert 9 | How does the page find the first linked child, and what is the not-available value? A script must reproduce it through the Jira API, and counts must match the page's. | High | | | |
| Expert 10 | Which teams count as program-reporting teams for epics and stories, and where does that list live? | High | | | |
| Expert 11 | Which recent run can the output be compared against for the parallel run? | High | | | |
| Expert 12 | Where do the automated pages live on Confluence Data Center (space and parent page), and who can view them? | Critical | | | |

## Parked
- Monthly defect report expert: after the gate. Next real run December 1.
- Phase 5 AI summary: depends on Phase 2 and a Jira administrator adding approval statuses. Out of the gate.
- Claude API key, service accounts, runner, hosting, monitoring: later phase.
- Old newsletter, NIST, and tech-writer questions (October 19 list): ask only if one of those candidates returns.

## What each answer unlocks
- **S0** unlocks all scaffolding before T0. **Eric 3 and the US-only row** decide whether N1 moves to week 1.
- **Access row, Dave 2, Dave 4** are the calendar-time items and the critical path.
- **Auto 3** decides whether the tests can run at all (pytest).
- **Expert 11** picks the run for S14 and the slice 2 parallel run. **Expert 12** gives the S13 target and the page audience (also asked of Dave 2).
- **Expert 1 to 12** become the rules file and the test cases.
