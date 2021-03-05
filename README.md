# sql

## rollback_monitor.sql
This evaluates used_ublk, that is number of undo blocks it needs to roll back. So if rolling back, it would be decreasing towards 0. For other transactions that aren't rolling back, they will be increasing, as they generate rollback.
