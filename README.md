# Repolex Knowledge Graph of aio-libs-abandoned/async-timeout

RDF knowledge graph data for [aio-libs-abandoned/async-timeout](https://github.com/aio-libs-abandoned/async-timeout), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs-abandoned/async-timeout
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7dc0022fb8160e3d7905cefa279e034e37063814
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7dc0022fb8160e3d7905cefa279e034e37063814
│           └── chunk-001.nq.gz
├── blob
│   ├── 033c86b7a40a331f281bd406e991ef1db597c208.nq.gz
│   ├── 146b8e807c52dd950bc4459b4d792e17b9fe0de0.nq.gz
│   ├── 178917043ecde38894106ab489349dd6158a7556.nq.gz
│   ├── 394c2c5ff15afff1ca13f4ef8b871d4d7094bcd9.nq.gz
│   ├── 3b94f915737aba1f12a0f067fdba3726bfe02df5.nq.gz
│   ├── 43acf59e2f809bda8b70c7046b606ff983370478.nq.gz
│   ├── 491deae0af2cae800a8fd1bc1ffb5ecd09221266.nq.gz
│   ├── 8b436cfa41a77f99b11c2fda58fcd8a0b01b7b7a.nq.gz
│   ├── 9741a010eb2919b612ae7aea6c02362dbc016553.nq.gz
│   ├── ac6c0b6f00d90133b91ea4b16484262903e1a9e6.nq.gz
│   ├── b024da80e9c1c8c800cc1b46e90c1e783cb446cc.nq.gz
│   ├── b1db8f211418c9d59d74bc1b567e52cfa5d80f21.nq.gz
│   ├── b4a8eb135055e956b606e9ab4d6ff4f74dc4f53d.nq.gz
│   ├── c3937a4020650b156f2c5684e27b713ea9cd976e.nq.gz
│   ├── d1671e950f58438c8398310068f593a8cfc03065.nq.gz
│   ├── dc34412d828c2ceb156a5989dc0c6003bd22ddba.nq.gz
│   ├── df1adfa0fc29492bbc6d3ad99e6247f53a51a867.nq.gz
│   ├── e9371928d2f131b14b76adfafaf8d8903b113202.nq.gz
│   ├── eace0faf706b1568ce603e6e7f4b986275250692.nq.gz
│   ├── fcc90db272fdbbb1d2c657c307c4d3aeec49f402.nq.gz
│   └── fe4aa581635bb30ee4e880366b1bbab6227fb148.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7dc0022fb8160e3d7905cefa279e034e37063814.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[aio-libs-abandoned/async-timeout](https://github.com/aio-libs-abandoned/async-timeout)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
