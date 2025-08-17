# Site Control
This is a basic script to handle the development work of a few small logger webapps with React/TS frontends and Go backends that handle thin SQLite database requests.

It's also been a `bash` learning journey for me, and I am adding complexity for complexity's sake to get my feet wet with a comprehensive utility script.

## Milestone Goals:

- [ ] Can start and stop a development version of the webapp (Vite + Go in a tmux session) via the script
- [ ] Can sync changes to a user systemd service repo 
- [ ] Can deploy the tunneled website and test in production
- [ ] Can retrieve site statistics like resource usage, uptime, versioning, etc.

## Idea Dump

My desired stat blocks would look something like:
```
pay.example-domain.com
 ├─ Production: UP
 |  ├─ Version: 0.9.8 (27JUL2025)
 |  ├─ Uptime: 17d 5h 30m
 |  ├─ Last deploy: 14AUG2025
 |  ├─ CPU: 2.9% | RAM: 55.3MB
 |  └─ Port 5001
 └─ Development: UP
    ├─ v0.9.9 (15AUG2025) - feat/analysis-view
    ├─ Last commit: 1d 14h ago
    ├─ CPU: 3.3% | Memory: 58.9MB
    └─ Port 5051

fuel.example-domain.com
 ├─ Production: UP
 |  ├─ Version: 0.5.1 (07AUG2025)
 |  ├─ Uptime: 18h 45m
 |  ├─ Last deploy: 09AUG2025
 |  ├─ CPU: 2.0% | RAM: 45.2MB
 |  └─ Port 5002
 └─ Development: UP
    ├─ v0.5.4 (15AUG2025) - feat/live-stats
    ├─ CPU: 2.2% | Memory: 41.8MB
    ├─ Port 5052
    └─ Last commit: 7h ago
```