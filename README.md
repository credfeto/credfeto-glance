# credfeto-glance

## Watchtower update schedule

Watchtower removes superseded images after updating (`WATCHTOWER_CLEANUP=true`) and checks for updates on a cron schedule.

- Default `WATCHTOWER_SCHEDULE`: `0 30 * * * *` (every hour, 30 minutes past).
- The format has 6 fields, seconds first: `second minute hour day month weekday`.
- To override it, set `WATCHTOWER_SCHEDULE` in the `.env` file next to `docker-compose.yml`, for example `WATCHTOWER_SCHEDULE="0 0 7 * * *"` for 07:00 daily. This lets hosts running several stacks update at different times.
