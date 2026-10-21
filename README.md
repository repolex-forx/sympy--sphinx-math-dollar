# Repolex Knowledge Graph of sympy/sphinx-math-dollar

RDF knowledge graph data for [sympy/sphinx-math-dollar](https://github.com/sympy/sphinx-math-dollar), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download sympy/sphinx-math-dollar
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7739ecb1ee78a402f867c2adf5ea59ccfe5b86a8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7739ecb1ee78a402f867c2adf5ea59ccfe5b86a8
│           └── chunk-001.nq.gz
├── blob
│   ├── 07c0a2eb744dc4baebdb6e5a77d8c05a894bce53.nq.gz
│   ├── 1159e8544080811a0399632238feaf476e86a78e.nq.gz
│   ├── 1233b4c6879bd572f2777813bfbb8ad1564b6d67.nq.gz
│   ├── 1329a105b4c27f2aee7633f06cdf3db443effe47.nq.gz
│   ├── 2119f51099bf37e4fdb6071dce9f451ea44c62dd.nq.gz
│   ├── 2152688aeaf29be5cfdfd828dc57b5893595ff3e.nq.gz
│   ├── 29e5156048ca34d387b6e9cc9a20ab1627f9ae00.nq.gz
│   ├── 2d0fb6874828758b35ed686070f3960c977a712f.nq.gz
│   ├── 386aec157f5a78489211db5541a1b5006a4da681.nq.gz
│   ├── 39648b7f0e70720ef17aca8e464b6f961e6fe92f.nq.gz
│   ├── 41e41901326602ab1e4d6102be10c299165b59e3.nq.gz
│   ├── 4a978f7c43e1e56ff8f69ee40273a2d8a6d2d262.nq.gz
│   ├── 4b5816a354e04ba258dd46ce164b2a9fb225ce09.nq.gz
│   ├── 4e2af846dc07897bdb195ff916e659392f0859d2.nq.gz
│   ├── 4eb343ee2bc7f44ce0c9b57b764ec3854520db41.nq.gz
│   ├── 565b0521d0c2cdbfe493d19765b04d5c119fa7eb.nq.gz
│   ├── 655d6f98c3200c07f426a028581434cd2bf8227e.nq.gz
│   ├── 69c3b2b630b5571e0ce965c7485456a809253316.nq.gz
│   ├── 7c67f7030a39e44c84ba6971b65ba135f69841e7.nq.gz
│   ├── 8a1e62e5224079bce9363667849797f044e617ec.nq.gz
│   ├── 8e249ab3dd7d13f502a55b4165eb456a0ced18b8.nq.gz
│   ├── 8f32454e09b46c638e987c41d019ce84d06829ba.nq.gz
│   ├── a0cf84a0e32d91a553b0d4361e5ef5668fbae4d0.nq.gz
│   ├── b4cd1d6c7c66ac52c492f9722e069466106d62fb.nq.gz
│   ├── b50c24dc36e03e5913494cedd5afc4f18c13f803.nq.gz
│   ├── bba984899017d2496b32384cba488251246d9dd6.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── dbec6352a8f85743e432e4b26eb7b43253d07123.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7739ecb1ee78a402f867c2adf5ea59ccfe5b86a8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[sympy/sphinx-math-dollar](https://github.com/sympy/sphinx-math-dollar)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
