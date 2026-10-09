# Repolex Knowledge Graph of NousResearch/hermes-homeassistant

RDF knowledge graph data for [NousResearch/hermes-homeassistant](https://github.com/NousResearch/hermes-homeassistant), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-homeassistant
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ba30cb0cf86c52bdb5cde98974bc062e97966529
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ba30cb0cf86c52bdb5cde98974bc062e97966529
│           └── chunk-001.nq.gz
├── blob
│   ├── 2265a89fba0d26c83eb64c797a7f68a2bc04d148.nq.gz
│   ├── 298178cfdaf629a02c387903635d8f48c55a73b6.nq.gz
│   ├── 29bf04456c783dbf7b81081012e2892b6cd7a4c0.nq.gz
│   ├── 318ca509b90415b37a4761a935e551c865503f68.nq.gz
│   ├── 4c9a851f7a1e18cb87e285c66ca4b857aaa99216.nq.gz
│   ├── 5700b997827973cb0eb6d84a2782bb08a5872434.nq.gz
│   ├── 618a043defe2b051fd86ae05b1c06d152adc2e56.nq.gz
│   ├── 8d027a6332312bc25a27b5a10fbbea98b4714685.nq.gz
│   ├── a8cfe8da7a82f74bd222c2ceab8ad61d5877cd87.nq.gz
│   ├── b2d45497a62a9b2c23a38198801d33bb6d72d4a9.nq.gz
│   ├── c2e57ae0ae7f8e01ba36a54d96fd3601e3fecd41.nq.gz
│   ├── d2eae0bf6c668a3fcf2b454fe52054ca8305c6e5.nq.gz
│   └── e4512bd08880e5dadf6170bb73951b264c13d547.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ba30cb0cf86c52bdb5cde98974bc062e97966529.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[NousResearch/hermes-homeassistant](https://github.com/NousResearch/hermes-homeassistant)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
