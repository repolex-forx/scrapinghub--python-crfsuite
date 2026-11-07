# Repolex Knowledge Graph of scrapinghub/python-crfsuite

RDF knowledge graph data for [scrapinghub/python-crfsuite](https://github.com/scrapinghub/python-crfsuite), parsed by [repolex](https://repolex.ai).

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
rlex download scrapinghub/python-crfsuite
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d3ee2eba443d5d3b313741bed5076b5a36a840d1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d3ee2eba443d5d3b313741bed5076b5a36a840d1
│           └── chunk-001.nq.gz
├── blob
│   ├── 045691e3a5415e0035cec48825e507ce061c8701.nq.gz
│   ├── 079256fe4c436869e60a7a6867d304b5ce3db724.nq.gz
│   ├── 3dd927c3afdf3b4ce9aa66ffb1417c2eb16f614e.nq.gz
│   ├── 3ebb021f7cb0d9ae8c91ca854c1576e051d863d7.nq.gz
│   ├── 42df75f6b7c60751833a42c1ed4c47f48f45634b.nq.gz
│   ├── 43aed55e4988535d99cf84b7391b89b086ff4c3a.nq.gz
│   ├── 45d52b7d633d400f8f6b32c25062be6158f34786.nq.gz
│   ├── 4a81c07bc939d4feee2548bd43921f0c1224e040.nq.gz
│   ├── 4eafc5d9d2b27766c7ef863fe02e1d6f84f7a04b.nq.gz
│   ├── 4eda608aa52d7adbfb52f38fdc05ab47d9425768.nq.gz
│   ├── 5bd941037725eb57a253a377510c4e1f82cc8903.nq.gz
│   ├── 5c3320174e647abc45938f9ce33d1e8fbc4fe88e.nq.gz
│   ├── 60a19d773f71b4c098009d86bb498e0a6c7545ba.nq.gz
│   ├── 647f2038f05f5c550494fb0c6116f5f29acbee8d.nq.gz
│   ├── 6932fdd6ef21bfea3998ee22c838ee0b78462ee1.nq.gz
│   ├── 7350ce3013ea1d45b6533a98052e587b814ac5f2.nq.gz
│   ├── 7543cc11f0378b443ea5bd3896f311345a74d542.nq.gz
│   ├── 7a41475d82f7def9d8c94e6adf5f2d044d9b4aaa.nq.gz
│   ├── 8fe66d1d556362c82a5078e12fba895a49be5bad.nq.gz
│   ├── 95c240c92e3fcbf0be487a87f9df12b71c4c23fc.nq.gz
│   ├── 97da796cc354e31df198b174e82f1bcedfa64c0d.nq.gz
│   ├── a2954e3184d712187766018da8c9007e86d424a7.nq.gz
│   ├── a3304d0e13119f57d47e281f91d556209a386ec6.nq.gz
│   ├── a5698488634c1d00ebf6fa1382fe58c5da370def.nq.gz
│   ├── a799388c8fe1962879a0e50a28a950cf7b34ced0.nq.gz
│   ├── b3064241f426f454adf431ecaed84d73a705d86f.nq.gz
│   ├── be04e224714fa413d63392b2318c520a6d0cc81f.nq.gz
│   ├── ca958c48844d7f32efadddf26d05d8feb4574c5e.nq.gz
│   ├── cae0d6ba0bfc3a8cfd9cbdf65846c0df701a35cc.nq.gz
│   ├── db9713e8ffd1f6b7e6edc0edfc4b3a7f462eb020.nq.gz
│   ├── e6c3c2a446198f8f1ec5209634e332c17686832d.nq.gz
│   ├── ebeb002f9ac1ed40511f62fee10bf6d3bc9e1330.nq.gz
│   └── fcaea0a6349148e870b3d2ddbc909be334434742.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d3ee2eba443d5d3b313741bed5076b5a36a840d1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[scrapinghub/python-crfsuite](https://github.com/scrapinghub/python-crfsuite)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
