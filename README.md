# Harborline Analytics

Data platform and department dashboards for Harborline Logistics, a fictional third-party logistics company. Practice
program; all data is simulated.

The simulator that produces the source data lives in its own folder (`harborline-lab`) and is not part of this repository.

## What's here

| Folder | What goes in it |
|---|---|
| `docs/adr/` | Architecture decision records, starting with `0001-platform.md` |
| `docs/metrics/` | Every metric definition agreed, with its owner |

Add `ingestion/`, `transform/`, `orchestration/`, `infra/`, `dashboards/` and `tests/` as the work needs them.

## How work happens

One branch per ticket (`feat/DATA-<n>-short-slug`), Conventional Commits carrying the ticket key, a pull request with
self-review, and `main` protected. Secrets never go in this repository: pre-commit scans every commit.
## Repository Structure

| Directory | Purpose |
|---|---|
| `ingestion/` | Source data extraction and Bronze ingestion |
| `transform/` | Silver and Gold data transformations |
| `orchestration/` | Pipeline scheduling and dependencies |
| `infra/databricks/` | Databricks infrastructure and deployment configuration |
| `dashboards/` | Dashboard definitions and related assets |
| `tests/` | Data quality checks and automated tests |
| `docs/adr/` | Architecture Decision Records |
| `docs/metrics/` | Approved business metric definitions |

The Harborline Lab simulator is maintained separately and is not included in this repository.
## Local Development

### Prerequisites

- Git and GitHub CLI
- Docker Desktop
- Python (version to be confirmed)
- VS Code
- Access to Databricks for cloud data processing

### Getting Started

1. Clone the repository:

   `gh repo clone KarimAbdelaziz2503/harborline-analytics`

2. Open the project:

   `cd harborline-analytics`

3. Start the Harborline Lab simulator using its separate setup instructions.

4. Verify the simulator is available at `http://localhost:8081` for the current local environment.

5. Review `docs/setup.md` for environment verification and configuration notes.

### Running and Testing

This repository currently contains the project skeleton. Executable ingestion pipelines, automated tests, and deployment commands will be added in subsequent tickets.

Do not use production credentials or commit local environment files.

## Project Tracking

- **Epic:** [DATA-1 — Data Platform Foundation](http://localhost:8081/tracker/issue/DATA-1)
- **Current ticket:** DATA-5 — Finish your data repository and project skeleton

The tracking links above require the Harborline Lab simulator to be running locally.