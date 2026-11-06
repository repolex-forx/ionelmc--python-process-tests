# Repolex Knowledge Graph of ionelmc/python-process-tests

RDF knowledge graph data for [ionelmc/python-process-tests](https://github.com/ionelmc/python-process-tests), parsed by [repolex](https://repolex.ai).

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
rlex download ionelmc/python-process-tests
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f92208195f08a9b934a7eec0c369b062df9d8ee4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f92208195f08a9b934a7eec0c369b062df9d8ee4
│           └── chunk-001.nq.gz
├── blob
│   ├── 0234f7ee8353e4ac95eb7719f006ce41bb2ec2a1.nq.gz
│   ├── 2201f97431cfcc056c9d9ec0428f69607f57507c.nq.gz
│   ├── 252fba5459e501b29dd5e07354fde9fe864480d2.nq.gz
│   ├── 583f25bc883ec3bcd83616df4d3cd635681958b1.nq.gz
│   ├── 586c7367de1cff5d362be309c0a4014b0905edb1.nq.gz
│   ├── 5abbc90e272fd34216e9189d3dc13fa62738b1f0.nq.gz
│   ├── 5e75b09167650f76759d4033bf7eb2e84fbd53bf.nq.gz
│   ├── 769224db63e14a19fb87c02434ba36aaf3db5522.nq.gz
│   ├── 77973dd9ff9648541ba9872375bba8ed6e340038.nq.gz
│   ├── 7c52ab83adbe6ac620345bae8297948bf8a8ff40.nq.gz
│   ├── 80980829f1c5bc7b51670dcd4deca83e5f2b4e61.nq.gz
│   ├── 81ea5cd70fa4ed931e74a3ef04d591aca505ab20.nq.gz
│   ├── 8c60a55274b761d38ec125d56265a60393aed9e6.nq.gz
│   ├── 9cb053de0a96a9781f80dc93923ec19d7e8de6a5.nq.gz
│   ├── a1708f401aa3b38d34cfb9a7b6d084fce2014e32.nq.gz
│   ├── ba514b7cfa48a79e2800ae9ed085ce4020115aaa.nq.gz
│   ├── c6dc633eac209ac281d1c6496135b6f7c6f6d9c2.nq.gz
│   ├── d01607af0a29bbccb70ed3e82bdfdce51fd6e02e.nq.gz
│   ├── d2969892762c2c007bfc7c9f9171faebca3a0c42.nq.gz
│   ├── df155f9290d8afd3822e10899aeeb7f073aafcac.nq.gz
│   ├── e6ea3bb1fd282e122b0eb9229d760d5fc8a0efd9.nq.gz
│   └── f3c9a7ea683e2a0b79a04e03b91fa117b49a08b0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f92208195f08a9b934a7eec0c369b062df9d8ee4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[ionelmc/python-process-tests](https://github.com/ionelmc/python-process-tests)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
