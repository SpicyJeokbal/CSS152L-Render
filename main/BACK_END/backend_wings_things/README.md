# Wings N' Things Backend

---

# Database Backup

# this is the backup for database
To back up your local PostgreSQL database, run the following command in your terminal:

```
pg_dump -U postgres -h localhost -F c -b -v -f backup_wingsnthings.backup postgres
```
- `-U postgres` : database username (see db.js)
- `-h localhost` : host (see db.js)
- `-F c` : custom format (recommended for restore)
- `-b` : include blobs
- `-v` : verbose
- `-f backup_wingsnthings.backup` : output file name
- `postgres` : database name (see db.js)

To restore:
```
pg_restore -U postgres -h localhost -d postgres -v backup_wingsnthings.backup
```

---

