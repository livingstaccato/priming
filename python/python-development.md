---
timestamp: 2025-02-09 10:06
iteration: 01
topic: Python Development Priming
---

1.  Shebangs and File Comments:
    -   All executable files (those containing `if __name__ == "__main__":`) *must* start with `#!/usr/bin/env python3`.
    -   The second line of *every* file *must* be a comment indicating the file's path relative to the project root (e.g., `# pyvider/core/__init__.py`).

2.  `attrs` Usage:
    -    Prefer `attrs` for defining classes, especially when immutability, validation, or advanced features are needed.  Use `attrs.define`, `attrs.field`, and appropriate validators.

3.  Logging:
    -   Use the Pyvider Logging Emoji Matrix (from previous interactions) for structured logging.
    -   Include *detailed* debug logging statements throughout the code to trace execution flow and variable values.  Use `logger.debug()`.
    -   Log key events, function entry/exit, and significant data transformations.

4.  Exception Handling:
    -   Use `try...except...finally` blocks comprehensively.
    -   Catch specific exceptions.
    -   Raise custom exceptions (derived from the Pyvider exception hierarchy) when appropriate.
    -   Include context in exception messages.
    -   Ensure proper resource cleanup in `finally` blocks.

5.  Inline Comments:
    -   Use concise inline comments to explain *why* code is written a certain way, *not* what it's doing (the code should be self-documenting in that regard).
    -   Focus on clarifying non-obvious logic or design decisions.
