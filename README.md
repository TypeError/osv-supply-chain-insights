# osv-supply-chain-insights

**Data-driven analysis of open-source supply-chain vulnerability trends using OSV.**

This repository explores vulnerability volume, severity, and remediation trends
across major open-source ecosystems using the Open Source Vulnerabilities (OSV)
dataset. It is intended to power both **monthly trend updates** and **annual
year-in-review analyses**, with a focus on supply-chain risk rather than
individual CVE deep dives.

---

## Scope

Initial ecosystem coverage includes:

- npm (JavaScript)
- PyPI (Python)
- Maven (Java)
- Go
- Cargo (Rust)

The emphasis is on **ecosystem-level signals**, such as:
- severity distribution shifts
- remediation speed
- data quality and churn
- year-over-year and month-over-month trends

---

## Data Approach

The project follows a simple, reproducible data flow:

```
raw OSV data → curated datasets → analysis & reporting
```

- **Raw data** is stored verbatim for traceability
- **Curated datasets** are flattened and normalized for analysis
- **Reports** consume curated data only and do not mutate inputs

Parquet is used as the primary analysis format.

---

## Repository Layout (high level)

```text
scripts/    # data fetching and curation
src/        # reusable pipeline logic
data/       # raw and curated datasets (gitignored)
reports/    # Quarto-based analysis and writeups
```

Details may evolve as the project matures.

---

## Analysis & Reporting

Analysis is performed using **Python, Polars, and Quarto**.
Reports are designed to support:

* monthly ecosystem trend summaries
* annual supply-chain retrospectives
* charts suitable for public sharing (e.g. LinkedIn)

---

## Design Principles

* Prefer reproducibility over convenience
* Keep raw data immutable
* Use flat, explainable schemas
* Optimize for insight, not dashboards

---

## License

MIT
