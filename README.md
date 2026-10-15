# Repolex Knowledge Graph of astropy/pytest-astropy

RDF knowledge graph data for [astropy/pytest-astropy](https://github.com/astropy/pytest-astropy), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/pytest-astropy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 594ff8e150181aec1a9dd2445f64617cc442b033
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 594ff8e150181aec1a9dd2445f64617cc442b033
│           └── chunk-001.nq.gz
├── blob
│   ├── 09a667802e39b5d3855a016d255afcd0a22b9619.nq.gz
│   ├── 134b363ce39fd0068d0e3d33f596a509e8e06687.nq.gz
│   ├── 350c5a7a0c9e43cd81936abb9111ee560be2e979.nq.gz
│   ├── 44596a70eb27d2df7c3818cc3bf6e4360bc66a98.nq.gz
│   ├── 63f2a696de5d357385a75deaff42837f855382f8.nq.gz
│   ├── 66b0a061fb3cfd7afd90bff842fc35e1e43639bf.nq.gz
│   ├── 981962d883e64f93e1289f6160b9a04e54b8fd06.nq.gz
│   ├── b507b35474ebf2eb9aeb41a0a0b918e0c6c1464b.nq.gz
│   ├── b84cf0f43e2351f1f641d89bc5718c2829601f33.nq.gz
│   ├── bad7a41d3bd1b1281f01e13b4a412d6e7ec51483.nq.gz
│   ├── beda28e821662c8d9fdefee034d83a5d75f9c023.nq.gz
│   └── e417cf74d6dc6a2d986fa64ca1d6d5c896dff216.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 594ff8e150181aec1a9dd2445f64617cc442b033.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[astropy/pytest-astropy](https://github.com/astropy/pytest-astropy)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
