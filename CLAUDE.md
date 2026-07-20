# Working Preferences

## Delivery

- **Paste solutions as code blocks in chat.** Do not edit the notebook files unless explicitly asked to.
- Keep every `# TODO:` comment from the exercise stub in the pasted answer.
- Give one exercise at a time, in full — the complete cell including the stub lines above and below the TODO, so it can be pasted over the cell as-is.

## Code style

- **No explanatory comments.** The only comments in a solution are the ones the stub already had.
- **Explicit `for` loops with `append()`** rather than list comprehensions.
- Keep each numbered task/requirement as its **own distinct step** — one construct should not do double duty across two requirements (e.g. don't reuse a single dict comprehension to satisfy both "compute averages" and "build the averages dict").
- Meaningful `snake_case` names.
- f-strings for formatted output (`:.2f` for display), `print("Label:", value)` for plain values.

## Match the notebook's house style

These notebooks have their own conventions — follow them over generic Python defaults:

- Type hints on every function/method signature: `def average(self) -> float`, `def __init__(self, name: str, scores: list)`.
- Plain `ValueError` for validation, not custom exception classes. Messages end with a period. Catch as `except ValueError as error: print("Validation error:", error)`.
- Validation helpers return the validated value, so callers read `self.name = validate_name(name)`.
- Chained comparisons: `if not 0 <= score <= 100`.
- Ternary for simple two-way returns: `return "Passed" if self.average() >= 60 else "Failed"`.
- Blank line before a `return` that follows a `raise` or a loop block.
- One blank line between methods, two between top-level definitions.
- Read file contents into a `content` variable before printing rather than chaining calls inline.
- Don't add guards for inputs the exercise never produces (e.g. empty-list checks).

## Verification

- Run the code before presenting it; confirm the output matches the exercise's stated **Expected output** exactly.
- Watch for cells that depend on stale kernel state or undefined variables.

## Context

Tuwaiq Python course — large Jupyter exercise workbooks, solved as a student and handed in. Comment-free, one-step-per-task code is easier to read, map to the assignment, and submit.
