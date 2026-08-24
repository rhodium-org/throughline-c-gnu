# throughline-c-gnu

The **GNU Coding Standards** for C — chapter 5, "Making The Best Use of C" — expressed
as a [throughline](https://pypi.org/project/throughline/) **source**: a standalone,
grounded requirements graph that a consuming project composes with
[throughline-compose](https://github.com/rhodium-org/throughline-compose).

This repository holds no code. It is a directory of small YAML items with permanent
UIDs, validated by `tl check`. Consumers import it under a namespace and reference
its rules as `cgnu:SR-0001`.

## GNU C style — one of two orthogonal C conventions

This source captures the **GNU** C convention: braces on their own line indented two
spaces from their keyword, indentation in **spaces**, a space before every
open-parenthesis, and the GNU rules on comments, naming and portability. It is
**deliberately distinct** from `throughline-c-linux`, which captures the Linux kernel
style — the opposite choice on braces (K&R, at end of line) and indentation (tabs).
The two are mutually exclusive house styles for the same language; **do not compose
both**. Pick the one your project follows.

It is one of a family of **orthogonal** language and concern sources: compose it
alongside a concern source so a project's C code is grounded in both at once.

## Status

<!-- tl:count type == 'user_requirement' -->
9
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
55
<!-- tl:end --> style rules, published to [`docs/spec.md`](docs/spec.md):

- `INT-0001` — the root intent (why the standard exists), `normative: false`.
- Each major chapter-5 section as a `user_requirement` that `derives_from` the intent.
- Every individual rule as a `system_requirement` that `implements` its section,
  carrying the standards reference in `attrs.source_ref`.

The counts above are rendered from the live graph by the `tl:count` directive, so
they cannot drift.

## Editions — dated tags

The standards are a living document. A material revision is cut as a dated tag on this
repo (e.g. `v2026-08`); a consumer pins the ref it wants.

## Composing it

```toml
[[sources]]
namespace = "cgnu"
url = "https://github.com/rhodium-org/throughline-c-gnu"
ref = "v2026-08"
```

Then reference a rule from your own items:

```yaml
links:
- target: cgnu:SR-0002          # GNU Coding Standards: open-brace of a function body in column one
  type: satisfies
```

`tl-compose check` resolves the reference; bare `tl check` fails fast and points you
at `tl-compose`.

## Local checks

```sh
pip install throughline
tl check --strict     # the graph must stay sound
tl docs --check       # docs/spec.md must match the graph
```

## Provenance

The GNU Coding Standards are published by the Free Software Foundation under the GNU
Free Documentation License v1.3. See [NOTICE](NOTICE) and
https://www.gnu.org/prep/standards/standards.html. This repository is Apache-2.0 for
its structure and tooling; the reproduced rule text remains the FSF's.
