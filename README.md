# Repolex Knowledge Graph of adamchainz/flake8-tidy-imports

RDF knowledge graph data for [adamchainz/flake8-tidy-imports](https://github.com/adamchainz/flake8-tidy-imports), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/flake8-tidy-imports
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7207cd25f9baa77542d2253e2fbf9dafb507c635
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7207cd25f9baa77542d2253e2fbf9dafb507c635
│           └── chunk-001.nq.gz
├── blob
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 2589a467fd01caf882e3e9d0757d625b3763ac4f.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 2ad62dfda8e993dbe8862309418e5cb6627e3c98.nq.gz
│   ├── 2aebe7a76dd8149674b9fde28e3608e8785b45f6.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40c1340c5e19a33ea6030dd19e4c417b1989b762.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 573d0696b1c0d0269724d9d30b85987e0b63efc7.nq.gz
│   ├── 663d6b920407c6318f1222445b39e30e44afa9d3.nq.gz
│   ├── 7808b5d337664266451079436bef66b2d726c371.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── 9d35ece0b38657d07bf67563cad8d3287946b793.nq.gz
│   ├── cbdda876cfa1cb646e4dd5d4e3ab43eed4677598.nq.gz
│   ├── cf4bca22e6d1dd6e79d5c283f94302e5483a0068.nq.gz
│   ├── e3a02c3753bb77ed0c6a6153888a92ce219523b0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f0a2abfa16717167b289159a2f38a41fde8a3457.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7207cd25f9baa77542d2253e2fbf9dafb507c635.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[adamchainz/flake8-tidy-imports](https://github.com/adamchainz/flake8-tidy-imports)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
