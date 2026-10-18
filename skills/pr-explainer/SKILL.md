---
name: pr-explainer
description: Explain a pull request's purpose, context, changes, and likely impact in clear, non-technical language. Use when someone wants to understand a PR before reviewing it, especially when the author or context is unfamiliar. Do not perform a nitpick-focused or line-by-line review unless separately asked.
---

# PR Explainer

Help the reader understand why a pull request exists and what it means, without requiring them to reconstruct the story from every changed line.

## How to work

1. Read the pull request title and description, then inspect the available diff, changed files, and relevant repository context. Look at linked issues, commits, or documentation when available and useful.
2. Identify the problem or need this change addresses. If the reason is not stated or cannot be supported by repository evidence, say that it is unclear; do not invent motivation.
3. Group the changes by purpose. Explain what changed and how the pieces fit together, using ordinary language and defining unavoidable technical terms.
4. Describe who or what may be affected, including user-visible behavior, APIs, data, configuration, deployments, or operations when relevant.
5. Call out meaningful risks, compatibility concerns, migrations, and unanswered questions. Distinguish directly observed facts from reasonable inferences.
6. Mention tests or checks only when their status is visible. Do not imply that a behavior was tested when the available evidence does not show it.

## Response format

Use this structure, omitting sections that genuinely do not apply:

### In one sentence
Summarize the change and its purpose.

### Why this PR exists
Explain the problem or goal. If the reason is not evident, say so plainly.

### What changes
Group the main changes into a short list. Describe their role, not every edited line.

### What this means
Explain likely effects for users, maintainers, or systems. Label inferences as inferences.

### Things to clarify
List only material unanswered questions, risks, or missing context that would help the reader assess the PR. If there are none apparent, say so.

### Checks
Summarize visible test and CI results, or say that their status was not available.

End with a short plain-language takeaway that helps the reader decide what to focus on next.

## Boundaries

- Prioritize purpose, context, and impact over review findings.
- Do not report style preferences, trivial formatting issues, or speculative defects as findings.
- Do not claim the change is correct, safe, or complete solely because checks pass.
- Do not infer that a change is safe to merge. The explanation supports the human review; it does not replace it.
- If the PR is too large or the available context is incomplete, explain what you could establish and what remains uncertain.
- Keep the explanation proportionate to the size and complexity of the change. Prefer a concise overview over a file-by-file inventory.
