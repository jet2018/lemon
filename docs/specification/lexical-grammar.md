# Lexical grammar

Status: pending design.

Source-file extensions: `.lemon`, `.l`, `.🍋`.

Before implementation, decide Unicode normalization, identifier syntax, whitespace, comments, numeric literals, string interpolation and reserved words.

## Proposed rules for the hello examples

Read source as UTF-8. Outside strings, skip spaces, tabs, line breaks and
line comments beginning with `//`. A line comment ends at a line break or
the end of the file.

For this draft, an identifier starts with an ASCII letter or underscore and
continues with ASCII letters, digits or underscores. Match the whole identifier
before checking for the case-sensitive keywords `class`, `static` and `void`.
Names such as `Main`, `Console` and `println` are ordinary identifiers.

A string_literal is enclosed in double quotes and may contain Unicode text,
including 🍋. The draft excludes raw line breaks, backslashes and double quotes
from the contents. Escape sequences and interpolation remain open for review.
