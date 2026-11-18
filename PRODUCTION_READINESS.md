# Production-readiness checklist: Server logs ELT / dbt Cloud

**Provenance:** README attributes the project to Data Engineering Zoomcamp and references `kkumyk/log_files_analysis_pipeline`. Verify which implementation changes are yours before presenting as original work.

## Controls to implement
- Mask/hash request IP addresses and other identifiers; specify retention and access boundaries.
- Require schema contracts and dead-letter/quarantine paths for malformed server-log records.
- Make daily ingestion idempotent and backfillable; partition data by event date and track late-arriving events.
- Configure dbt Cloud jobs and environments via least-privilege service credentials.
- Enforce dbt generic tests, freshness checks, referential integrity and documentation.
- Add orchestration retry policies, task timeouts and reconciliation counts from GCS through BigQuery.
- Add CI gates, observability, alerting, cost budgets and rollback procedures.

## Status
The README references dbt Cloud and Kestra, but repository text alone does not prove deployed jobs, business SLAs or production users. Verify with run logs and CI results before using those claims in a CV.
