# Repolex Knowledge Graph of pytest-dev/pytest-pastebin

RDF knowledge graph data for [pytest-dev/pytest-pastebin](https://github.com/pytest-dev/pytest-pastebin), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-pastebin
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 072ccbdb5a4ebbf1b41ff78f644880a3d0388291
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 072ccbdb5a4ebbf1b41ff78f644880a3d0388291
│           └── chunk-001.nq.gz
├── blob
│   ├── 050d2ad00966b3bc2199f2bcd569ec7d8a1115e6.nq.gz
│   ├── 15dbffbb6fcf221c03cb052e61a8523bacdc5e65.nq.gz
│   ├── 27a4aa34d5b9f83cdb727c81bcb162b25128b281.nq.gz
│   ├── 6c5886e04363a482ba04555c612e8520b3af7d33.nq.gz
│   ├── 852089cc79b847f1b904defd3cae7a090a76fb51.nq.gz
│   ├── 857cf69df8d8b39f1a13b5a32bb6674f38393e79.nq.gz
│   ├── 8ef554fa41589f064f67f8d2389f80c6bed9c346.nq.gz
│   ├── 949c02fd95bf592a95c5d92166b3247b3a247b2a.nq.gz
│   ├── 95f7ec2cc987337be5e0b7ae42a2ea0a16abb720.nq.gz
│   ├── bc711e55fefdd729816958fa0ce1563b55217c29.nq.gz
│   ├── e381e2618fa219e99f609f4aa1eaa9819b3c36b6.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 072ccbdb5a4ebbf1b41ff78f644880a3d0388291.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 19 files
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

[pytest-dev/pytest-pastebin](https://github.com/pytest-dev/pytest-pastebin)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
