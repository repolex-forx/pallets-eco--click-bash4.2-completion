# Repolex Knowledge Graph of pallets-eco/click-bash4.2-completion

RDF knowledge graph data for [pallets-eco/click-bash4.2-completion](https://github.com/pallets-eco/click-bash4.2-completion), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/click-bash4.2-completion
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b0fcf111ad59422b024a5a4e2737040f70f06eff
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b0fcf111ad59422b024a5a4e2737040f70f06eff
│           └── chunk-001.nq.gz
├── blob
│   ├── 047c0f2664845beb8ba4a2c2ef913dce67d98dbd.nq.gz
│   ├── 1a053ebfe21b190c9bac6d31fa3d713b7165eac8.nq.gz
│   ├── 79b5c98940f780910ceddc8bd4fbd02af6b9fbfc.nq.gz
│   ├── 8ddfdd73bf890a0e91b23fca34ec4268814866ea.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   └── c9133d67eee5e43c80f19530a12dd6df0fbf4db4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b0fcf111ad59422b024a5a4e2737040f70f06eff.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 14 files
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

[pallets-eco/click-bash4.2-completion](https://github.com/pallets-eco/click-bash4.2-completion)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
