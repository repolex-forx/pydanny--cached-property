# Repolex Knowledge Graph of pydanny/cached-property

RDF knowledge graph data for [pydanny/cached-property](https://github.com/pydanny/cached-property), parsed by [repolex](https://repolex.ai).

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
rlex download pydanny/cached-property
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c032196d9afdf4b21d041c7d1492c95f5d1d6740
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c032196d9afdf4b21d041c7d1492c95f5d1d6740
│           └── chunk-001.nq.gz
├── blob
│   ├── 0bcaa1aaa90a93c494ad3237e6a96cbbf17c4a8c.nq.gz
│   ├── 152dfc28781d49c6081786839ac4ebaba2b85494.nq.gz
│   ├── 1df1886df8c8820090b6cc4602860d7eea76179c.nq.gz
│   ├── 2446d517f1e14f18cd72abcf9380460c76dd5e82.nq.gz
│   ├── 24e1f793cbe848ac6a028680dc346693888c8a90.nq.gz
│   ├── 29758fdc058850cfe465f6eb39aad42a23fd1bdb.nq.gz
│   ├── 387699d3c963d9494626a5246cc66b32c2fa81ac.nq.gz
│   ├── 75454c8052e14ec47bd62ca8e7c863408b28ffe8.nq.gz
│   ├── 75d8df9759b2fb0ea3a23862711c63e30de9901f.nq.gz
│   ├── 837806a52243c6eecc7f2a2639c8ea6dbfcf1186.nq.gz
│   ├── 9aecff9a27188ff9df8e9949e096b5cc437ecf01.nq.gz
│   ├── a181761ca55c8ca4601cf3143c220c12f547d9b0.nq.gz
│   ├── b0df7f7c2e9b412a5d54b9f55af83ca7e38e2d9e.nq.gz
│   ├── e6336c8a6d3776b4ddbddc25bf1f65fed0cdf71b.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e83ad16b2204acc965c696f2bb66b2f9780df199.nq.gz
│   ├── e83ecca8bf918b9dcd98005f60dad74ef3744b10.nq.gz
│   ├── e8faca3c0397ac9fcd3eae8671dce3ddf7a56f18.nq.gz
│   └── efa122992589d0239f4091796d99f0e08a52db62.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c032196d9afdf4b21d041c7d1492c95f5d1d6740.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[pydanny/cached-property](https://github.com/pydanny/cached-property)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
