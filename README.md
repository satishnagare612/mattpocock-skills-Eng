Engineering
The skills I use for code work every day.

User-invoked
These can be invoked only when you explicitly type the skill name.
(Claude Code: disable-model-invocation: true; Codex: policy.allow_implicit_invocation: false in agents/openai.yaml.)

ask-matt — Ask which skill or flow fits the current situation; this is the router for the repository’s user-invoked skills.

grill-with-docs — An interrogative interview that simultaneously builds the project’s domain model, refines terminology, and updates GLOSSARY.md and ADRs inline.

triage — Move issues forward through a triage-roles state machine.

improve-codebase-architecture — Scan the codebase for “deepening” opportunities, generate a visual HTML report, then continue grilling around the candidates you select.

setup-matt-pocock-skills — Configure the issue tracker, triage labels, and domain-docs layout that this repository needs for the engineering skills. Run once per repo.

to-spec — Turn the current conversation into a spec and publish it to the issue tracker.

to-tickets — Split a plan, spec, or conversation into tracer-bullet tickets. Each ticket declares blocking edges: represented as text in local files, and as native blocking links on a real tracker.

implement — Implement a piece of work based on a spec or ticket set, drive /tdd on pre-approved seams, and finish with /code-review before committing.

implement-spec — Implement the whole spec on a single integration branch. Treat tickets as a task graph, run implementer subagents in parallel on the ready frontier to maximize concurrency, and finish with /code-review.

wayfinder — Plan a large chunk of work that exceeds a single agent session as a shared map of decision tickets on the issue tracker, resolving them one by one until the road to the destination is clear.

retro — After a session ends, suggest improvements to the coding agent’s environment (navigation, automated checks, coding standards, steering files, tooling), with the most severe first.

Model-invoked
The model or the user can invoke these. Their descriptions contain rich enough trigger wording that the model can find them automatically.

prototype — Build a throwaway prototype to answer a design question: either a runnable terminal app that answers state/logic questions, or multiple switchable UI variants.

diagnosing-bugs — A disciplined diagnostic loop for tricky bugs and performance regressions: reproduce → minimize → hypothesize → instrument → fix → regression-test.

research — Research a question against high-confidence primary sources and save cited findings as Markdown files in the repo, running as a background agent.

tdd — Use a red-green-refactor loop for test-driven development; build features or fix bugs one vertical slice at a time.

domain-modeling — Proactively build and refine the project’s domain model: challenge terminology, stress-test it with scenarios, and update GLOSSARY.md and ADRs inline.

codebase-design — Shared discipline and vocabulary for designing deep modules: small interfaces, clear seams, and testing through interfaces.

code-review — Review the diff after a fixed point along two axes: Standards (does it follow the repo’s coding standards, plus the Fowler smell baseline?) and Spec (does it faithfully implement the source issue/PRD?), run as parallel sub-agents.

pr — The shape a PR body should take: explain the change with a minimal visual summary, include before/after evidence proving it works, then make a merge-risk judgment (one-way or two-way door, plus blast radius).

wizard — Generate an interactive Bash wizard that guides a person through steps only they can perform: provisioning infrastructure, setting credentials or CI secrets, walking through an unfamiliar third-party dashboard, or running a one-off migration or cutover.
