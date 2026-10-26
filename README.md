# Airbyte Cookbook

<!-- ZQM-START -->
<!-- markdownlint-disable MD033 -->
<p align="center">
  <strong>ZQM Computing — Geospatial Engineering & Scientific Computing</strong><br>
  <a href="https://github.com/ZQM-Computing">ZQM Computing</a>
</p>
<!-- markdownlint-enable MD033 -->
<!-- ZQM-END -->

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A **Airbyte cookbook** — connector-based ELT into Postgres and DuckDB. Fleet Docker deployment in progress: a kind cluster is up on Node-1 and Node-3, with UI and ingress work still underway. Patterns are planned from the deployment design. It is intended for Data engineers who prefer configured connectors over hand-written pipelines. Validate each pattern against your own data, software versions, and operating environment before adopting it.

## Repository role and status

**Status:** Active, public — seeding. Pattern passes land in follow-up work from fleet-verified setups; the tables below list what is planned, not what is already written.

**What this repository is:** Airbyte patterns — see the table below.

**What it contributes:** Part of the ZQM Computing geospatial portfolio. The umbrella index for the series is [geospatial-cookbooks](https://github.com/ZQM-Computing/geospatial-cookbooks).

**Standing:** This repository is maintained independently. Automated checks cover only the paths and environments configured in its workflows; they do not establish production readiness or operational certification.

## Who this is for

Data engineers who prefer configured connectors over hand-written pipelines.

## Prerequisites

- Airbyte via kind cluster (abctl)
- Postgres or DuckDB as a destination
- Source credentials, kept out of repos

## Patterns (planned)

| # | Example | What it will demonstrate |
|---|---------|--------------------------|
| 01 | `01-first-connection` | A first connection: source, destination, and sync mode |
| 02 | `02-postgres-dest` | Syncing into Postgres tables |
| 03 | `03-schedules` | Scheduled syncs and incremental modes |
| 04 | `04-dbt-pairing` | Transforming synced tables with dbt (see dbt-cookbook) |

## Repository layout

```text
airbyte-cookbook/
├── examples/          # pattern passes, landing in follow-up work
├── README.md
└── LICENSE
```

## Roadmap

- First pattern pass: the first two table rows
- Second pass: the remaining rows, from fleet-verified setups

## Contributing

A contributing guide lands with the first pattern pass. Report security issues to <zqmcomputing@gmail.com> — please do not open a public issue for those.

## More from this series

- [dlt-cookbook](https://github.com/ZQM-Computing/dlt-cookbook) — ELT pipelines from Python into Postgres and DuckDB
- [dbt-cookbook](https://github.com/ZQM-Computing/dbt-cookbook) — SQL transformations, models, and tests on Postgres
- [airflow-cookbook](https://github.com/ZQM-Computing/airflow-cookbook) — DAGs, schedules, and geospatial pipelines
