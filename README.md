# Repolex Knowledge Graph of coleifer/ukt

RDF knowledge graph data for [coleifer/ukt](https://github.com/coleifer/ukt), parsed by [repolex](https://repolex.ai).

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
rlex download coleifer/ukt
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d31d5a4586479567398a7896c709cb702e318cdf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d31d5a4586479567398a7896c709cb702e318cdf
│           └── chunk-001.nq.gz
├── blob
│   ├── 04d259222b5f5ef7d1ad4fce07f2b101161fe8b9.nq.gz
│   ├── 1156dae80463fd710d80ea8604d1ba3887d4d7d6.nq.gz
│   ├── 3138240f959eafa0ae3641ec1b00b8b7dcba513e.nq.gz
│   ├── 3e6825d4bfac5a4e31a01c8816e97476a50b916f.nq.gz
│   ├── 3f37f29070fab06d98238be94fded8551c3d5c45.nq.gz
│   ├── 41c7da4150b740dff03ed4dd0b9d011036b8c00f.nq.gz
│   ├── 4c3dcad6e3f69bb38d0fe7ad1a4410e5d9d4ac80.nq.gz
│   ├── 4cdbd3059bb144f2d8885da76c57b91f3d3281da.nq.gz
│   ├── 4d8f4d8cf8551f9e3c64c9c6c896b45101f542f4.nq.gz
│   ├── 5635ad9e644bc273d30383bd763ce90127ae6936.nq.gz
│   ├── 57cf0026e0267dca377d75719db241beafb88f18.nq.gz
│   ├── 60403229475afb84db7a77d99d46fe047bc9608b.nq.gz
│   ├── 61e0ed7435f50143669aebe910cd24d8876c05af.nq.gz
│   ├── 7afcd11c0a524dbef1ecb1029aeabfa0243e2af9.nq.gz
│   ├── 902f159a03c3075bad6587de89d85e9e23602cb3.nq.gz
│   ├── 928acad0d0ac84c62c00088e7e2217297bf0c1e2.nq.gz
│   ├── 9517e4e364c9288963b16b14b63c839fa22d1ec5.nq.gz
│   ├── 97448100f469080f06bf63916bc863c8c73b74cb.nq.gz
│   ├── 9d81d562bbc20d755840d19bcd2f47ef35709053.nq.gz
│   ├── b3260fb7152646b49ae0f66b0420940475e9e0d5.nq.gz
│   ├── c752ab3ead2e7be324e5cafb5e1d53135c16af13.nq.gz
│   ├── d21528e96c071d3cae70021c3cecc0098260bfb0.nq.gz
│   ├── d2834cd2c90c2c74554f94804924f1d34f105eab.nq.gz
│   ├── db66ed0a51b95feb95ebd234e826b94d662b3ed1.nq.gz
│   ├── dc24cfadf91fbcf74406f96e8ea77ecb23d678bb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9bc7f9c48e71c460ae576a62675a062ae45b8a8.nq.gz
│   ├── e9c66c3f2145a61b90d9493622aafc7bd8c0dc8d.nq.gz
│   ├── edbd97b7d29539da828401740b76fe6a29a35e83.nq.gz
│   ├── f443fe66d47b28aade70a2e06feeec83e47009e7.nq.gz
│   └── ffa6b0cdf65cec680bd13cec0da509b47cc968af.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d31d5a4586479567398a7896c709cb702e318cdf.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 37 files
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

[coleifer/ukt](https://github.com/coleifer/ukt)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
