# Contributing

## Scope

This repository is separate from the canonical reproducibility pipeline. Keep exploratory work isolated and label its maturity clearly.

## Before adding a project

Include a short README in the project directory recording:

- **Purpose:** the question or problem being explored.
- **Status:** exploratory, prototype, under review, promotion candidate, promoted, or archived.
- **Scope:** what is and is not covered.
- **Method:** key assumptions, data sources, and dependencies.
- **Reproduction:** exact inspection or execution steps, if applicable.
- **Limitations:** known gaps and risks.
- **Promotion:** whether the work is intended for REPRO, and what evidence is required.

## Reproducibility and safety

- Never describe an experiment as run or validated without recorded evidence.
- Do not commit credentials, tokens, private datasets, or other secrets.
- Avoid hidden network calls and implicit provider/API usage in prototypes.
- Keep generated data and large artifacts out of Git unless there is a clear, reviewed reason.
- Do not add workflows that launch expensive experiments or call external model providers without explicit review and authorization.

## Promoting work to the canonical repository

Changes to the experiment pipeline must be proposed separately in [LLM-HypatiaX-REPRO](https://github.com/sednabcn/LLM-HypatiaX-REPRO). The PR should identify the originating project/commit and explain impact on experiment definitions, workers, dependencies, artifacts, and reproducibility.

A prototype is not canonical merely because it performs well in an isolated demonstration.
