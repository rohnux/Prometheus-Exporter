

### Create user in MongoDB for authentication for the MongoDB exporter:

```
db.createUser(
  {
    user: "MONITORING-USER",
    pwd: "###############",
    roles: [
        { role: "clusterMonitor", db: "admin" },
        { role: "read", db: "local" }
    ]
  }
)
```
