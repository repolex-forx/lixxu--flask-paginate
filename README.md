# Repolex Knowledge Graph of lixxu/flask-paginate

RDF knowledge graph data for [lixxu/flask-paginate](https://github.com/lixxu/flask-paginate), parsed by [repolex](https://repolex.ai).

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
rlex download lixxu/flask-paginate
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f51a23a625757d964c0208e75ccee4c833c05977
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f51a23a625757d964c0208e75ccee4c833c05977
│           └── chunk-001.nq.gz
├── blob
│   ├── 003bd40426588075c6e1fe3e0c29048859c16adb.nq.gz
│   ├── 18c720f804c6f034cdb1ee02a616cc1e271a4007.nq.gz
│   ├── 1c6df309edc8fd9c5aaa21d4a7fb867dd73ba8ec.nq.gz
│   ├── 1f48051d856428c32071e591d6f167ae7980ed05.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 33014f9da00da57a83452673c9acda932b7a958d.nq.gz
│   ├── 33f47449c11d241e36c83d7f95d819bbe56e2c8f.nq.gz
│   ├── 385dba21458a321b4a763c94bcde50c6399e8d65.nq.gz
│   ├── 39a98662fe3b44b4644943d8be045a8a8992c51f.nq.gz
│   ├── 3eb33cf38480f43a7eed3da3a6f826611dfedb8c.nq.gz
│   ├── 43bfc4e2c095d1107e6399c070860ad1e4b7ae25.nq.gz
│   ├── 4627f211c4b32bd49c38938d3edff5db2b30e903.nq.gz
│   ├── 4f748190593a963a0d31d96414c2e57bb82e8c07.nq.gz
│   ├── 4f989352c70bd6898af8984b238121d3242fb313.nq.gz
│   ├── 532f605784224e1b41a48749b242e76429e1e96c.nq.gz
│   ├── 542b462515db7875ea5813c33181870ae06edff7.nq.gz
│   ├── 548fd1f16a5d226409202ccb644f05a91236b3e6.nq.gz
│   ├── 5a378da8cb92b35b2a1f41975a82aa0e14f8fa2e.nq.gz
│   ├── 66b6e4c2f3b55b25afd9716f9d3c5afb47b15d4e.nq.gz
│   ├── 6852609ade2b08bce5dfb42465de4459b8f53cbb.nq.gz
│   ├── 7a3dad12fb7adb117a705691cd227e5431d2e28e.nq.gz
│   ├── 8beb8a83245dac13d886f0698e92c6362b853f41.nq.gz
│   ├── 8daab7ee6efe3b6f3c2a2594b711e7a9026eb5e2.nq.gz
│   ├── 91b97c662a95d38d3416e4e8cd71e0e327e693b4.nq.gz
│   ├── 9a4faea1f89cd9eb632640413dfc56d7fc8b2c44.nq.gz
│   ├── b3292bdff8ed5429eedd7f409839979d408beb6a.nq.gz
│   ├── b5ca39bc1ea7d9c27dfb80b986a59acb14594468.nq.gz
│   ├── b6b07ee072a0325763a2ef0ec9dd372d58474539.nq.gz
│   ├── c3c3d6301dc99ee5339c1a9aaf81a2d347ab4683.nq.gz
│   ├── c8e5fa5000c9b49eb0efef06e28a51dd84e05e7a.nq.gz
│   ├── caa3b5a53135482da4ee4ce4ff1e729acdba5137.nq.gz
│   ├── f95898685ca59610cf36d6efb9b07ced2641f532.nq.gz
│   ├── fba2ba29a47079c26e4f6e002caadbe2ae44bb5b.nq.gz
│   └── fe2141c565e6976b6a2a5b73f318ad7c6dc3d58b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f51a23a625757d964c0208e75ccee4c833c05977.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[lixxu/flask-paginate](https://github.com/lixxu/flask-paginate)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
