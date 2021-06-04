

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
### MongoDB Connection String for MongoDB exporter
```
mongo_exporter_mongo_addr: "mongodb://MONITORING-USER:###############@{{ ansible_ssh_host }}:27017/admin"
```
