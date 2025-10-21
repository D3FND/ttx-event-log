# TTX Event Log

A community-driven repository for sharing and analyzing event logs from tabletop exercises (TTX), cyber ranges, and real-world incidents.

## About
Each event submission captures who did what, when, and why — standardized into a simple CSV schema for easy filtering and reuse.

## Schema
Timestamp,Speaker/Role,Decision/Observation,Evidence Reference,Action Item,Owner,Tags

## Labels (metadata)
Use labels to enrich events without changing the schema:
- `source:cloudtrail`, `source:windows`, `source:sentinel`
- `cell:blue`, `cell:red`, `cell:white`, `cell:green`
- `phase:detect`, `phase:analyze`, `phase:contain`, `phase:eradicate`, `phase:recover`, `phase:lessons`
- `sev:low|medium|high|critical`
- `cve:CVE-YYYY-NNNN`, `ttp:T####`, `actor:NAME`
- `service:aws-ec2|okta|gmail|…`
- `sensitivity:public|cui|pii`
- `ttx:scenario-name`, `round:phase1|phase2`

## Contribute
1. Go to **Issues → New Event**.
2. Fill out the form (no sensitive data or live tenant identifiers).
3. Submit — automation validates and opens a PR that appends to the CSV.

## Data
- Canonical CSV: `data/event_log_template.csv`
- Optional monthly files: `data/YYYY-MM.csv` (enable the monthly workflow if desired).

## Privacy & Safety
Do not include secrets, PII, live tenant details, or proprietary indicators. Use synthetic/sanitized examples where needed.
