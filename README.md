# Repolex Knowledge Graph of jupyter-server/jupyter_server_fileid

RDF knowledge graph data for [jupyter-server/jupyter_server_fileid](https://github.com/jupyter-server/jupyter_server_fileid), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter-server/jupyter_server_fileid
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c2902acd44b63a421e7226c3bc8b6856943d4c0d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c2902acd44b63a421e7226c3bc8b6856943d4c0d
│           └── chunk-001.nq.gz
├── blob
│   ├── 1cea1a855624c14898e94ea69831bbf463f2fa36.nq.gz
│   ├── 21a03d939f6fee669a88be554a017796c90bbad3.nq.gz
│   ├── 31dbf0d704ae126a6a14f5c1fb63ce6142bc100a.nq.gz
│   ├── 3227141da31cf59ea5e69b115911c0e7547a88db.nq.gz
│   ├── 329e1bdc85a685cf622c643ae2988be82fb329c8.nq.gz
│   ├── 32bb24529f92346af26219baed295b7488b77534.nq.gz
│   ├── 375c10e05d6948547fec5fcdc48127efef8d6156.nq.gz
│   ├── 396330bb9729d2ec595617aef79fb28600d86bd7.nq.gz
│   ├── 52377c30172a73551e1c5c21795ebc1eaca2c085.nq.gz
│   ├── 5295e776b63d7adfab3ddad99962cc6f81968909.nq.gz
│   ├── 58d9b1acd44a8fdfafea574252b56b9cc5f2132f.nq.gz
│   ├── 60af4c5f16741c7c2fe17cdd9718ae5f6d56d8a4.nq.gz
│   ├── 65168da9507c2b98454cc7b1753144526dcc3ef8.nq.gz
│   ├── 8240395fdb86df904c39ed62a97a628205087c00.nq.gz
│   ├── 9357e25478336b26065173364cec705e1bd7364c.nq.gz
│   ├── 9ee0b6707d65878ca1669e7f542e21f1ef69686d.nq.gz
│   ├── a26d368d4a4841e4248ac89fe50a76db8b161a6d.nq.gz
│   ├── a6f280c579281046f73289e3a46e61596fffa54b.nq.gz
│   ├── ab4cbfe22a059ecc8e6558a76cdf51444e35b31c.nq.gz
│   ├── b295197df82aa93ebc1314240de2580d2d1678c9.nq.gz
│   ├── b8c0628517ed222ab418b6b3754abd4428254b3d.nq.gz
│   ├── b9c17d5a99c115efc8b66f522c19d0d994d26710.nq.gz
│   ├── bb9c7662c9d7b7b8979edabb868b698cf8625a5a.nq.gz
│   ├── bdb64f71d876ce3282c75e45f2286d7fa760393e.nq.gz
│   ├── be929968070305af0d610e603c57a0b615995c55.nq.gz
│   ├── beebcaff1a58f74982013ab8eeaee4d526b800d1.nq.gz
│   ├── c8148b5e3f7487bc50a4486776c23146b0788579.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d9057ce009cb179af733da2a0c5d068aec8a45b3.nq.gz
│   ├── e03d5680ef5df058030be63d3b392a0ecb859f7c.nq.gz
│   ├── e42512d547ebeef40994e6adbb6bdc43396a9f86.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f21fa6374270d59bb20f47ad60afcb35f2052954.nq.gz
│   ├── f93d6cca1e225160e8b908df6f1e79f718fc9c1d.nq.gz
│   └── f9b02f7b3014297f99425819831669295dcae9d0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c2902acd44b63a421e7226c3bc8b6856943d4c0d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 43 files
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

[jupyter-server/jupyter_server_fileid](https://github.com/jupyter-server/jupyter_server_fileid)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
