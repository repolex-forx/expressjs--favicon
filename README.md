# Repolex Knowledge Graph of expressjs/favicon

RDF knowledge graph data for [expressjs/favicon](https://github.com/expressjs/favicon), parsed by [repolex](https://repolex.ai).

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
lexq download expressjs/favicon
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9293f8902a87024c15a98a8c3c0738eec7c02e4f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9293f8902a87024c15a98a8c3c0738eec7c02e4f.nq.gz
│   └── repolex
│       └── 9293f8902a87024c15a98a8c3c0738eec7c02e4f
│           └── chunk-001.nq.gz
├── blob
│   ├── 02e42ef53c532aaff57b89836e9417880e5fcab9.nq.gz
│   ├── 054e9da8353e56c90b0ecc19fcd6854fc2d0d342.nq.gz
│   ├── 29c15b08432d05cdf6bdc4b9cd1dbd78348408d5.nq.gz
│   ├── 3cd27afdb6d88edd8bd83ee7adbc7313084a48e7.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 727013d06c90c0e162fa76b188f222e93d0164a1.nq.gz
│   ├── 76ef782a27140537110fe51e05dc54d1890805e4.nq.gz
│   ├── 895fc96a76b68b4924f1c51d022e1b82fa0f461f.nq.gz
│   ├── 90cf24ff2497d281fa03f6ba76a21d10a3ad18d2.nq.gz
│   ├── a30a7c6b96d04a6d1ca556a502316681c362ef9f.nq.gz
│   ├── c27eeac8eae2ccf5dcd23af9c1f896a2fb90db17.nq.gz
│   ├── c6faeef98d5f985fe76f4ad9eacbb4241a0537b3.nq.gz
│   ├── d5d459aad90b802993efa3582a893c059f425bfe.nq.gz
│   └── e3578aadfd3a97c6ef9d74f46e07314d775c9c61.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9293f8902a87024c15a98a8c3c0738eec7c02e4f.nq.gz
├── filetree
│   └── 9293f8902a87024c15a98a8c3c0738eec7c02e4f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 24 files
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

[expressjs/favicon](https://github.com/expressjs/favicon)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
