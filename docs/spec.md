# GNU C coding standards — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses chapter 5 of the **GNU Coding Standards** ("Making The Best Use of C") as a grounded IDD graph: each major section is a `user_requirement`, and every individual rule is a `system_requirement` that `implements` its section. The standards reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `cgnu:SR-0001`, never by section name. This is the GNU C convention, one of two orthogonal C-style choices; it is not the Linux kernel style.

It carries
<!-- tl:count type == 'user_requirement' -->
9
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
55
<!-- tl:end --> style rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — C code follows one consistent GNU house style, readable and portable** — `intent`, status `approved`

> Chapter 5 of the GNU Coding Standards, "Making The Best Use of C", exists so that C across GNU programs shares one house style: a consistent visual layout, disciplined comments, clean use of C constructs, meaningful names, and portability across system types and CPUs. The point is that any GNU contributor can read, search and safely change code they did not write, and that a program built to run first on GNU/Linux still ports cleanly elsewhere. This is the GNU brace-and-space convention specifically, and is deliberately one of two orthogonal C-style choices; it is not the Linux kernel style.

**source_ref**: GNU Coding Standards
<!-- tl:end -->

## Formatting Your Source Code

<!-- tl:item UR-0001 -->
**UR-0001 — Formatting Your Source Code** — `user_requirement`, status `approved`

> Rules governing line length, brace placement, function layout, indentation, line splitting and spacing of GNU C source.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: Formatting
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: Formatting') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Keep source lines to 79 characters or less |
| SR-0002 | system_requirement | approved | Put the open-brace of a function body in column one |
| SR-0003 | system_requirement | approved | Do not put an opening bracket in column one inside a function |
| SR-0004 | system_requirement | approved | Start a function definition's name in column one |
| SR-0005 | system_requirement | approved | Split an over-long argument list onto aligned continuation lines |
| SR-0006 | system_requirement | approved | Put struct and enum braces in column one unless they fit on one line |
| SR-0007 | system_requirement | approved | Indent a compound statement's braces two spaces and its body further |
| SR-0008 | system_requirement | approved | Put a space before an open-parenthesis and after each comma |
| SR-0009 | system_requirement | approved | Split an expression before an operator, not after it |
| SR-0010 | system_requirement | approved | Add extra parentheses so indentation shows the nesting |
| SR-0011 | system_requirement | approved | Format a do-while statement in the GNU brace style |
<!-- tl:end -->

## Commenting Your Work

<!-- tl:item UR-0002 -->
**UR-0002 — Commenting Your Work** — `user_requirement`, status `approved`

> Rules governing what to comment, the language and sentence form of comments, and comments on functions, static variables and preprocessor conditionals.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: Comments
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: Comments') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0012 | system_requirement | approved | Begin the main program's file with a comment saying what it is for |
| SR-0013 | system_requirement | approved | Begin each source file with its name and purpose |
| SR-0014 | system_requirement | approved | Write comments in English |
| SR-0015 | system_requirement | approved | Comment each function's behaviour, arguments and return value |
| SR-0016 | system_requirement | approved | Write complete sentences with two spaces after each period |
| SR-0017 | system_requirement | approved | Do not capitalise a lower-case identifier at the start of a sentence |
| SR-0018 | system_requirement | approved | Refer to an argument value in upper case |
| SR-0019 | system_requirement | approved | Comment each static variable |
| SR-0020 | system_requirement | approved | Comment every non-trivial |
<!-- tl:end -->

## Clean Use of C Constructs

<!-- tl:item UR-0003 -->
**UR-0003 — Clean Use of C Constructs** — `user_requirement`, status `approved`

> Rules governing declarations, local variables, nested if/else bracing, and avoiding assignments inside if-conditions.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: Clean Use of C Constructs
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: Clean Use of C Constructs') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0021 | system_requirement | approved | Explicitly declare the types of all objects |
| SR-0022 | system_requirement | approved | Do not add casts or wrappers merely to placate a static checker |
| SR-0023 | system_requirement | approved | Group forward and external declarations near the file's top |
| SR-0024 | system_requirement | approved | Declare a distinct, well-named local variable for each purpose |
| SR-0025 | system_requirement | approved | Do not shadow a global identifier with a local or parameter |
| SR-0026 | system_requirement | approved | Do not spread multiple variable declarations across lines |
| SR-0027 | system_requirement | approved | Always brace an if-else nested inside another if |
| SR-0028 | system_requirement | approved | Write a nested if in an else as else-if or in its own braces |
| SR-0029 | system_requirement | approved | Declare a structure tag separately from its variables or typedefs |
| SR-0030 | system_requirement | approved | Avoid assignments inside an if-condition |
<!-- tl:end -->

## Naming Variables, Functions, and Files

<!-- tl:item UR-0004 -->
**UR-0004 — Naming Variables, Functions, and Files** — `user_requirement`, status `approved`

> Rules governing meaningful names, abbreviations, word separation, letter case and the naming of option flags and files.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: Naming
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: Naming') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0031 | system_requirement | approved | Choose global names that convey meaning |
| SR-0032 | system_requirement | approved | Keep local variable names short but clear |
| SR-0033 | system_requirement | approved | Limit abbreviations in symbol names |
| SR-0034 | system_requirement | approved | Separate words in a name with underscores |
| SR-0035 | system_requirement | approved | Use lower case, reserving upper case for macros and enum constants |
| SR-0036 | system_requirement | approved | Name an option flag after its meaning, not its letter |
| SR-0037 | system_requirement | approved | Define integer constants with enum rather than |
<!-- tl:end -->

## Portability between System Types

<!-- tl:item UR-0005 -->
**UR-0005 — Portability between System Types** — `user_requirement`, status `approved`

> Rules governing which system portability matters, use of Autoconf, feature-test macros and avoiding non-portable names.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: System Portability
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: System Portability') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0038 | system_requirement | approved | Treat GNU/Linux as the primary target, other Unix ports as optional |
| SR-0039 | system_requirement | approved | Use Autoconf to achieve system portability |
| SR-0040 | system_requirement | approved | Define the _GNU_SOURCE feature-test macro |
| SR-0041 | system_requirement | approved | Do not reuse the names of GNU extension functions for other meanings |
| SR-0042 | system_requirement | approved | Do not abbreviate Windows as "win" |
<!-- tl:end -->

## Portability between CPUs

<!-- tl:item UR-0006 -->
**UR-0006 — Portability between CPUs** — `user_requirement`, status `approved`

> Rules governing assumptions about integer and pointer sizes, byte order and casting pointers to integers.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: CPU Portability
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: CPU Portability') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0043 | system_requirement | approved | Assume int is at least 32 bits |
| SR-0044 | system_requirement | approved | Do not assume long is as wide as a pointer or size_t |
| SR-0045 | system_requirement | approved | Do not assume an int's address is that of its least-significant byte |
| SR-0046 | system_requirement | approved | Avoid casting pointers to integers |
<!-- tl:end -->

## Calling System Functions

<!-- tl:item UR-0007 -->
**UR-0007 — Calling System Functions** — `user_requirement`, status `approved`

> Rules governing use of standard interfaces, not redeclaring system functions and leaning on Gnulib for portability.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: System Functions
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: System Functions') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0047 | system_requirement | approved | Use standard C and POSIX interfaces where possible |
| SR-0048 | system_requirement | approved | Never write your own declaration of a system function |
| SR-0049 | system_requirement | approved | Use Gnulib to paper over library portability gaps |
<!-- tl:end -->

## Internationalization

<!-- tl:item UR-0008 -->
**UR-0008 — Internationalization** — `user_requirement`, status `approved`

> Rules governing use of GNU gettext and writing translatable message strings.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: Internationalization
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: Internationalization') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0050 | system_requirement | approved | Wrap user-visible strings in gettext for translation |
| SR-0051 | system_requirement | approved | Do not assemble sentences from conditional fragments |
| SR-0052 | system_requirement | approved | Use ngettext for plural forms |
<!-- tl:end -->

## Character Set and Quote Characters

<!-- tl:item UR-0009 -->
**UR-0009 — Character Set and Quote Characters** — `user_requirement`, status `approved`

> Rules governing the source character set, encoding, and quotation characters in program output.

*Derives from:* INT-0001

**source_ref**: GNU Coding Standards: Character Set and Quotes
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('GNU Coding Standards: Character Set and Quotes') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0053 | system_requirement | approved | Prefer plain 7-bit ASCII in source |
| SR-0054 | system_requirement | approved | Use one encoding, preferably UTF-8, for non-ASCII characters |
| SR-0055 | system_requirement | approved | Use plain ASCII quotes in the C locale |
<!-- tl:end -->

