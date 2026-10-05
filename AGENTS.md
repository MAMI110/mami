# Notes
- Single Python service (`python main.py`): console + embedded worker + core, SQLite by default. No credentials needed.
- Run: `docker compose -f docker-compose.base44.yml up -d`; served on port 3000 (PORT=3000). Health: `/health`.
- Default login: admin / admin. GitHub OAuth (`LUNEL_GITHUB_CLIENT_ID/SECRET`) is optional.
- No hot reload (main.py spawns a worker); restart the `app` service after backend edits.
