# sql

## rollback_monitor.sql
This evaluates used_ublk, that is number of undo blocks it needs to roll back. So if rolling back, it would be decreasing towards 0. For other transactions that aren't rolling back, they will be increasing, as they generate rollback. Run in 1 min intervals, to estimate rollback time e.g. previous USED_UBLK - current USED_UBLK -> roll back rate per minute then divide roll back rate per minute / total USED_UBLK.
