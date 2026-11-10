# Repolex Knowledge Graph of reem/rust-ordered-float

RDF knowledge graph data for [reem/rust-ordered-float](https://github.com/reem/rust-ordered-float), parsed by [repolex](https://repolex.ai).

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
rlex download reem/rust-ordered-float
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── aa4c4f2deb34472828e27c61218e6a60abe42c86
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── aa4c4f2deb34472828e27c61218e6a60abe42c86
│           └── chunk-001.nq.gz
├── blob
│   ├── 39892cb6a08b5a961862e3d1157b265060da3a3e.nq.gz
│   ├── 3d0334642c444acd54b751f1279a8d1e9ee7276d.nq.gz
│   ├── 5ae333d96ade51ff956b93283c50ef9919e3f8b5.nq.gz
│   ├── 6dd94868be248e6f0797d69e33e197d5aa99d54b.nq.gz
│   ├── 781fffa416c4c8c38485f4606cdc855e17835565.nq.gz
│   ├── 81ef046da847dcadc70e15429f9cb89bbe88f98f.nq.gz
│   ├── 8b352de4e5e14f76095cce7afe920402761fe893.nq.gz
│   ├── 917e89c9e9794e7cceb5bad697b96c6b79e5c611.nq.gz
│   ├── b3b7cf91032fd2d546fd917b51ee5ac1f64b4757.nq.gz
│   ├── c8e0f5ec7a510d34578abc9a1bd8adbb1b7c089c.nq.gz
│   └── e333edc9dbbe4aa5453552cd435a7bd445919708.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── aa4c4f2deb34472828e27c61218e6a60abe42c86.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[reem/rust-ordered-float](https://github.com/reem/rust-ordered-float)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
