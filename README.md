# Repolex Knowledge Graph of zopefoundation/Persistence

RDF knowledge graph data for [zopefoundation/Persistence](https://github.com/zopefoundation/Persistence), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/Persistence
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dd314e753b91ce2024540d86aa834bde3cb6dc96
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dd314e753b91ce2024540d86aa834bde3cb6dc96
│           └── chunk-001.nq.gz
├── blob
│   ├── 01d7fbc00a56fa443ee7a3f2e4504f1493492e2f.nq.gz
│   ├── 1b0cf63a480ae1ec129729977c44694b161bb646.nq.gz
│   ├── 2d9b6f6073982fc3bdf9cc5f61372fffefd57133.nq.gz
│   ├── 32e6e7343d36b0167d83d3fdf4b636a1f6211000.nq.gz
│   ├── 33f5dc9f46b31cd827fed2aeba3f35ef5a46f1ce.nq.gz
│   ├── 4b7e84d4189385d5b6e4f9f483836836c7d6b1e7.nq.gz
│   ├── 4dd049d21cad44d727dd5e7e9334f71eb1807ac4.nq.gz
│   ├── 545e9aa91dca056445ca20e2e08f2cc992a63fab.nq.gz
│   ├── 60ee4f42fcdd8e424eee8ebb051bda21c3737204.nq.gz
│   ├── 63813b91d7d84d2b30e855c86f3652502882a319.nq.gz
│   ├── 6dc3470c88f84bf1f94ac68d41ebc06b816d106d.nq.gz
│   ├── 77f3c744e601e8cdd746df3914bf9c9c8ea5365f.nq.gz
│   ├── 78609a5f5a06dd7d09bef2926810c672a193b0a1.nq.gz
│   ├── 861b4334a4115fc010ec6ddbb4ded613f2ff991e.nq.gz
│   ├── 8c562a0d2bb5fc1039d9d9b8124c0d517fbf20b7.nq.gz
│   ├── 99978ee25a0b84ee2694a5d19a18d9e486614c8a.nq.gz
│   ├── 9b559f6a6a754e8dc5bfc3f7597f4f0c66ee11d0.nq.gz
│   ├── 9b9fef92a4274c450f57d8a5a4087f93761cde80.nq.gz
│   ├── a4a38a1803b01f191c832128836e48861d4a3612.nq.gz
│   ├── b8581dd898cbb33e63961b4d181ff0ffbe5d03ee.nq.gz
│   ├── bab7f94be5ef86cce49612e6cdab326a57143d7d.nq.gz
│   ├── da2968d9fe1a56fd32e9e8ee2c51510d98f274a1.nq.gz
│   ├── df8e822df2f323a8abd36a0d0550f4afbb78753a.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e62eec2685820226d926dae3ba92518b526a522e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8c61c67dafe6162e848dc16dc75e0474c572063.nq.gz
│   ├── ebe6d07a3ac429b206bffaec433f1107a4d14885.nq.gz
│   ├── fdafa384691cf7210c388eca5b4069293bc7e205.nq.gz
│   ├── fdd77cece6a12f3ea3d46669b698dcdd8e48d235.nq.gz
│   └── ffee6a163301e8ce55668b2a9bbe412f51a594fd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dd314e753b91ce2024540d86aa834bde3cb6dc96.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[zopefoundation/Persistence](https://github.com/zopefoundation/Persistence)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
