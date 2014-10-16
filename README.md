# Backup Scripts

Collection of backup scripts (sometimes just wrapers) for MySQL.
Tools to enhance the MySQL Backup experience and make it easier (almost plug and play...almost!)

All the scripts take care of the retention policy (defined by the user), as followed:

- For MyDumper: User will define weekly and daily retention times.
- For Mysqldump: User will define weekly and daily retention times.
- For Mysqlbinlog: User will define number of days that the binlog files will be keep it
- For XtraBackup: User will define weekly and daily retention times.

## Binlog backup
pull-binlogs.sh
Bash script for backup binlogs using the mysqlbinlog utility that comes with MySQL 5.6.
To launch this script, run:

```
  nohup ./pull_binlog.sh > /var/log/mysql/pull_binlog.log 2>&1 /dev/null
```

## MyDumper backup
mydumper.sh
Bash script used as a wraper of the [MyDumper](https://launchpad.net/mydumper "MyDumper") backup tool. Run this script as a daily cronjob

## Mysqldump backup
mysqldump.sh
Bash script used as a wraper of the classic mysqldump backup tool. Run this script as a daily cronjob

## XtraBackup script.
xtrabackup.sh
Bash script used as a wrapper of the Percona XtraBackup tool. Run this script as a daily cronjob. 
It only takes care of full backups. Coming soon: Incremental backups
