# crypto_analysis

## Short description
A compact data-analysis project and Power BI dashboard that summarizes cryptocurrency market metrics (price changes, market capitalization, momentum scoring) to provide visual insights about market movement and asset performance.

## Table of contents
- [Introduction](#introduction)
- [Dataset / Inputs](#dataset--inputs)
- [Tech stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis & Features](#analysis--features)
- [Results / Insights](#results--insights)
- [Project structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Introduction
This repository holds the raw data, processed data and report assets used to build a Power BI dashboard for cryptocurrency analysis. It is intended to make it easier to explore price movements, market cap trends, and momentum-based scoring of crypto assets.

## Dataset / Inputs
- Raw API endpoints and link files are stored under `raw_data/api/` (e.g., `api_link`, `api_link.txt`).
- Derived/cleaned datasets (if present) live in `clean_data/` or `report/` depending on project conventions.

Note: Do not modify raw files in `raw_data/`; create derived outputs in `report/` or `derived/` instead.

## Tech stack
- Power BI Desktop (primary reporting tool)
- Optional: Python (pandas, matplotlib) or other scripting languages for ETL and generating figures (use only if added by contributors)

## Installation
1. Clone the repository:

```bash
git clone <repo-url>
cd crypto-analysis
```

2. Open the Power BI report files with Power BI Desktop (if available) or inspect the `report/` directory for exported assets.

3. If you add analysis scripts using Python, create a virtual environment and install dependencies (example placeholder):

```bash
python -m venv .venv
.venv\Scripts\activate    # Windows
pip install -r requirements.txt
```

## Usage
- Open the Power BI report files (if included) to interact with dashboards and visuals.
- If you add scripts (e.g., `scripts/run_analysis.py`), run them to produce derived CSVs or plot images that should be saved to `report/report_images/`.

## Analysis & Features
- Momentum calculation based on historical growth metrics
- Price change percentage analysis (24h, 7d)
- Market capitalization ranking and trend analysis
- Comparative performance insights for selected cryptocurrencies

(Implementation details live in any scripts or notebooks contributors add to `src/` or `notebooks/`.)

## Results / Insights
The project aims to produce visual dashboards and analytical summaries that help answer questions like:
- Which cryptocurrencies show consistent momentum over the selected period?
- How do short-term (24h) and mid-term (7d) price changes compare?
- Which assets rank highest by market cap growth or momentum score?

Include any exported figures or CSVs under `report/report_images/` and reference them in documentation.

## Project structure
- `raw_data/` — raw API data and endpoint links (do not modify in-place)
- `report/` — report files, exported figures, and final outputs
  - `report/report_images/` — generated visuals used by reports
- `clean_data/` (optional) — cleaned datasets ready for analysis
- `scripts/` or `src/` (optional) — place analysis scripts or notebooks here
- `LICENSE` — project license

## Contributing
- Open an issue or PR before making large changes.
- Keep raw data immutable; add derived outputs to `report/` or `derived/`.
- If adding runnable analysis, include a `requirements.txt` and a short `README` in the new folder describing how to run it.

## License
See the `LICENSE` file for details.

## Contact
For questions or collaboration, open an issue in this repository or contact the project owner at `kanchisukheja20@gmail.com`.

---

