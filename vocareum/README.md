# Vocareum Lab Setup

Vocareum integration for the Neo4j + Databricks workshop. Handles automated workspace provisioning, per-student cluster/notebook setup, and teardown.

Lab notebooks live in the repo root (`Lab_2_Databricks_ETL_Neo4j/`, `Lab_3_Semantic_Search/`) -- they are not duplicated here. The `upload.sh` script packages them into a zip at deploy time.

## Quick Start

```bash
export VOC_TOKEN="your-pat"
export VOC_COURSE_ID="206455"
export VOC_ASSIGNMENT_ID="..."
export VOC_PART_ID="..."

./upload.sh
```

## What's Here

| Path | Purpose |
|------|---------|
| `scripts/` | Lifecycle hooks (workspace_init, user_setup, lab_setup, lab_end) |
| `courseware/dlt_fleet_etl.py` | DLT pipeline (bronze/silver/gold) for fleet telemetry data |
| `courseware/aircraft_digital_twin_data.zip` | 22 CSV source files for the pipeline |
| `courseware/neo4j-databricks-workshop.cfg` | Vocareum course config (cluster, catalog, entry notebook) |
| `docs/README.md` | Student-facing instructions shown in Vocareum iframe |
| `upload.sh` | Builds notebook archive from repo root and uploads everything |

See [SETUP_GUIDE.md](SETUP_GUIDE.md) for full instructions.
