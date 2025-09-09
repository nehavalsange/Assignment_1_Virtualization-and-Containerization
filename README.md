# Assignment_1_Virtualization-and-Containerization
# Docker Containers

## What it does
Builds a two-container stack: a Postgres DB seeded with sample `trips` rows and a Python app that queries the DB, computes statistics, prints JSON to stdout, and writes `/out/summary.json`.

## Commands
Build & run:
- `docker compose up --build`
or
- `make up` (if you created the Makefile)

Stop & cleanup:
- `docker compose down -v`
or
- `make down`

## Example output (printed to terminal)
(See the file out/summary.json after run)

## Where outputs are written
- `./out/summary.json`

## Troubleshooting
- If the app fails to connect: ensure Docker Desktop is running and port 5432 is free, or remove the `ports` mapping in compose.yml.
- If `/out` is not writable: ensure `out/` exists and has proper permissions: `mkdir -p out && chmod 755 out`
