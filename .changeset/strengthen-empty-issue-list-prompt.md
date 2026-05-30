---
"@ai-hero/sandcastle": patch
---

Strengthen the `simple-loop` and `sequential-reviewer` prompts so an empty pre-expanded `LIST_TASKS_COMMAND` result is treated as ground truth, not as a stale snapshot. The "do not re-query" hint now frames the filtered list as the sole source of truth, and the `# Done` completion criterion explicitly equates an empty list with completion. Prevents the agent from running its own unfiltered `gh issue list` when the filtered list is `[]`.
