# LLM-HypatiaX-REPRO-Improvements

A separate workspace for research, prototypes, analysis, documentation, and substantial improvements that are not part of the reproducible experiment pipeline.

The canonical reproducibility code, experiment definitions, workers, benchmark entry points, and CI workflows remain in [LLM-HypatiaX-REPRO](https://github.com/sednabcn/LLM-HypatiaX-REPRO).

## What belongs here

- Exploratory research and technical investigations.
- Standalone prototypes and alternative implementations.
- Analysis, historical run outputs, and visualizations that do not define canonical pipeline results.
- Design proposals, post-run investigations, and documentation for substantial future changes.
- Superseded one-off repair scripts, patches, and recovery inventories retained for provenance.
- Improvements being evaluated before deliberate promotion into REPRO.

## What does not belong here

- Copies of the active REPRO pipeline that could become ambiguous sources of truth.
- Experiment workers, benchmark execution paths, or CI workflows intended to run canonical experiments.
- Results presented as reproducible pipeline outputs unless produced and validated in REPRO.

## Repository layout

The repository preserves original REPRO-relative paths for migrated material. For example, historical files formerly under `archive/`, `scripts/archive/`, `docs/`, and `recovery-inventory-*/` remain under those same paths here. This makes provenance and cross-reference straightforward while keeping them out of the active pipeline checkout.

| Path | Purpose |
| --- | --- |
| `research/` | Literature notes, technical investigations, and analysis |
| `prototypes/` | Isolated proof-of-concept implementations |
| `design/` | Architecture proposals and promotion plans |
| `docs/` | Cross-cutting documentation and decision records; mirrored historical docs retain their original paths |
| `archive/` | Superseded explorations, historical run data, audits, and patches retained for context |
| `scripts/archive/` | Superseded one-off scripts retained for provenance |
| `recovery-inventory-*/` | Historical branch and commit recovery inventories |
| `hypatiax/experiments/benchmarks/core295_*`, `scripts/core295_*`, `config/core295_catalogue.json` | Core-295 research tooling (catalogue discovery/review, planning, and fail-closed shard tooling); not part of the canonical experiment launcher. Runtime dependencies remain in canonical REPRO; this workspace is not a self-contained execution environment. |

`REPRO_TRANSFER_MANIFEST.tsv` records every migrated path, its source Git blob SHA, and the reason for separation.

Each new project should document its purpose, status, assumptions, dependencies, inspection or execution steps, limitations, and promotion intent.

## Promotion into REPRO

Promote changes to the canonical repository only through a reviewed PR to [LLM-HypatiaX-REPRO](https://github.com/sednabcn/LLM-HypatiaX-REPRO), including:

1. The problem and motivation.
2. Exact files and behavior affected.
3. Reproducibility, compatibility, and dependency implications.
4. Regression coverage and CI evidence where appropriate.
5. Migration or rollback notes.

Do not present exploratory results as validated pipeline outputs. Keep provenance and promotion history explicit.

## Status convention

Use one of: **exploratory**, **prototype**, **under review**, **promotion candidate**, **promoted**, or **archived**.

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution conventions.
