---
name: grill-me
description: Structured grilling for stress-testing plans or designs. Use when the user says "/grill-me", "grill me", wants to be interviewed, stress-test a plan, validate assumptions, decide tradeoffs, or asks for relentless questioning. In Pi, ask user-facing questions with the ask_user_question tool.
---

Interview me relentlessly about every aspect of this plan until we reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one by one.

## Operating rules

- If a question can be answered by exploring the codebase, explore the codebase instead.
- Ask exactly one user-facing question at a time.
- In Pi, use the `ask_user_question` tool for each user-facing question. Do not ask the question as plain text when the tool is available.
- Each `ask_user_question` call should contain one question with 2-4 concrete options.
- Put your recommended answer first and end its label with `(Recommended)`.
- Explain the tradeoff or consequence for each option in the option description.
- Do not add an "Other", "Type something", or "Chat about this" option; Pi provides those automatically.
- If the user chooses a custom answer, treat it as the decision and continue from there.
- Keep the interview state compact: settled decisions, unresolved branches, and why the next question matters.
