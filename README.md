# fpf-simple-skill

AI coding agent skill for the [First Principles Framework (FPF)](https://github.com/ailev/FPF) by [Anatoly Levenchuk](https://github.com/ailev).

FPF is a transdisciplinary reasoning architecture for systems engineering, knowledge coordination, and mixed human/AI teams. This skill splits the 56,000-line FPF specification into a two-level hierarchy (20 directories, 224 files) so an agent loads only the ~300-line sub-section it needs instead of the entire spec.

## Install

```bash
npx skills add CodeAlive-AI/fpf-simple-skill -g
```

## Structure

```
sections/
  04-part-a-kernel-architecture-cluster/
    _index.md                          # TOC with descriptions of all sub-sections
    01-a-0---onboarding-glossary.md    # 137 lines
    02-a-1---holonic-foundation.md     # 185 lines
    ...                                # 19 sub-sections total
  08-part-c-kernel-extensions-specifications/
    _index.md
    ...                                # 30 sub-sections
  ...                                  # 20 directories total
```

The agent reads `_index.md` first, picks the right sub-section file, and loads only that.

## Sections

| # | Section | Sub-sections |
|---|---------|:---:|
| 01 | Title page | 0 |
| 02 | Table of Content | 0 |
| 03 | Preface | 17 |
| 04 | Part A — Kernel Architecture | 19 |
| 05 | A.IV.A — Signature Stack & Boundary | 18 |
| 06 | A.V — Constitutional Principles | 29 |
| 07 | Part B — Trans-disciplinary Reasoning | 24 |
| 08 | Part C — Kernel Extensions | 30 |
| 09 | Part D — Ethics & Conflict | 1 |
| 10 | Part E — Constitution & Authoring | 0 |
| 11 | E-I — FPF Constitution | 29 |
| 12 | Part F — Unification Suite | 0 |
| 13 | F.I — Context of Meaning | 19 |
| 14 | UTS Layout A | 0 |
| 15 | UTS Layout B | 1 |
| 16 | Part G — SoTA Patterns Kit | 15 |
| 17 | Part H — Glossary | 0 |
| 18 | Part I — Annexes | 0 |
| 19 | Part J — Indexes | 0 |
| 20 | Part K — Lexical Debt | 2 |

## Regenerating sections

If the upstream FPF spec changes, pull the submodule and re-run the splitter:

```bash
git submodule update --remote
python3 scripts/split_spec.py
```

## Credits

- **FPF specification**: [Anatoly Levenchuk](https://github.com/ailev) — [github.com/ailev/FPF](https://github.com/ailev/FPF)
- **Skill packaging**: [CodeAlive-AI](https://github.com/CodeAlive-AI)

## License

MIT
