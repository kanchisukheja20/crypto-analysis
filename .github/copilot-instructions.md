# Copilot / AI Agent Instructions for this Repository

This repository is a small data-analysis/report project. There is no application code or build system detected — primary contents are data and report assets. Use these instructions to get productive quickly and avoid breaking assumptions.

- **Big picture:** This repo stores raw input data under `raw_data/` and finalized report assets under `report/`.
  - `raw_data/api/` contains API link files (`api_link`, `api_link.txt`) used as data sources.
  - `report/report_images/images/` contains generated visuals used by the final report.

- **Primary workflows (discoverable):**
  - Inspect `raw_data/` for input sources before changing analyses.
  - Place any generated outputs (plots, CSVs, figures) under `report/report_images/` and reference them in `README.md` or new report docs.

- **What I (the agent) should assume:**
  - There are no Python/Node manifests (`requirements.txt`, `pyproject.toml`, `package.json`) or CI config files present. Do not run builds or tests unless the user provides scripts or environment details.
  - No tests or executables are discoverable. Before creating or executing scripts, ask the user for desired language/runtime and any credentialed API keys.

- **Code/changes guidance specific to this repo:**
  - Avoid modifying `LICENSE` and `README.md` without explicit request.
  - If adding analysis code, create a top-level `src/` or `notebooks/` folder and add a minimal `README.md` documenting how to run it and required dependencies.
  - Keep raw data immutable: never overwrite files in `raw_data/` — add derived outputs to a new folder (e.g., `derived/` or under `report/`).

- **Examples of useful actions an agent can take (ask for permission first):**
  - Add a `requirements.txt` and a small `scripts/run_analysis.py` that demonstrates how to consume `raw_data/api/api_link.txt` and produce a sample plot saved to `report/report_images/`.
  - Scaffold a short `CONTRIBUTING.md` that documents the data-first workflow and where outputs live.

- **When you need more info:**
  - Prompt the user for: runtime (Python/Node), desired data processing steps, data formats (CSV/JSON), and any external API credentials.
  - If asked to run code, request the target execution environment (local, Docker, WSL) and whether you should create reproducible env files.

- **Files to inspect when reasoning about a change:** `raw_data/`, `raw_data/api/api_link*`, `report/report_images/`, `README.md`.

If any section above is unclear or you want me to extend the instructions with runnable examples (scaffold scripts, dependency files, or CI), tell me which language/runtime to use and I will draft them.
