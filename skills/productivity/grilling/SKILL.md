---
name: grilling
description: Grill the user relentlessly about a plan, decision, or idea. Use when the user wants to stress-test their thinking, or uses any 'grill' trigger phrases.
---

Interview me relentlessly about every aspect of this until we reach a shared understanding. Walk down each branch of the decision tree, resolving dependencies between decisions one-by-one. For each question, provide your recommended answer.

Ask the questions one at a time, waiting for feedback on each question before continuing. Asking multiple questions at once is bewildering.

In Pi, ask each user-facing decision with the `ask_user_question` tool instead of plain chat. Use one question per tool invocation unless multiple independent decisions must be answered together. Provide 2-4 concrete options, put the recommended option first, and label it `(Recommended)`. Keep option labels short and include a clear description of the trade-off. Do not add custom "Other", "Type something", or "Chat about this" options; the tool provides escape hatches automatically.

If a *fact* can be found by exploring the environment (filesystem, tools, etc.), look it up rather than asking me. The *decisions*, though, are mine — put each one to me and wait for my answer.

Do not act on it until I confirm we have reached a shared understanding.
