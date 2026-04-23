# Repolex Knowledge Graph of asimov-modules/asimov-modules.py

RDF knowledge graph data for [asimov-modules/asimov-modules.py](https://github.com/asimov-modules/asimov-modules.py), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download asimov-modules/asimov-modules.py
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 71aa4dba31a6b87643aea9e6ce5cee477557a383
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 71aa4dba31a6b87643aea9e6ce5cee477557a383.nq.gz
│   └── repolex
│       └── 71aa4dba31a6b87643aea9e6ce5cee477557a383
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c8702458ffff58f683157f8376f4b0c774e2622.nq.gz
│   ├── 17e1e83dfd1d4b6d8d20e2837126e3021dc780b4.nq.gz
│   ├── 19a31b4dae4983cccd2cf67abb335c2b819b239b.nq.gz
│   ├── 21a01787ca0a0abaf7a195033c8b9779a238953b.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 6f83656972dcf4cdabab996bd49dde3986bc10be.nq.gz
│   ├── 8b265cc167d538e85fcb9013e9488d98cd011ffe.nq.gz
│   ├── a11f3ae703f1fdd880f595d10bfb6619ed4968a4.nq.gz
│   ├── a55b903cdf9a8a80463bcd3d6f941fa53f2ca89b.nq.gz
│   ├── b2356fc1e346df3efa7bf4ed61c5411d5852b1a4.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── c32d29b038aca228c6527e02d6378d6d3f463bbb.nq.gz
│   ├── c483311580f7753c86b4323cd5b5f47220bd3253.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f7d08efa731bafe87b61018e6bc7016304458369.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 71aa4dba31a6b87643aea9e6ce5cee477557a383.nq.gz
├── filetree
│   └── 71aa4dba31a6b87643aea9e6ce5cee477557a383.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

## Source repository

[asimov-modules/asimov-modules.py](https://github.com/asimov-modules/asimov-modules.py)

---
*Parsed on 2026-04-23 by [repolex](https://repolex.ai)*
