# Zabbix Template Abills

This template only checked on 3.0.x and 3.2.x versions.

## Install

```
apt install unixodbc libodbc1 libmyodbc odbcinst
```

Add to `/etc/odbcinst.ini`

```
[MySQL]
Description = ODBC for MySQL
Driver      = /usr/lib/x86_64-linux-gnu/odbc/libmyodbc.so
Setup       = /usr/lib/x86_64-linux-gnu/odbc/libmyodbcS.so
FileUsage   = 1
```

Add to `/etc/odbc.ini`

```
[abills]
ReadOnly = yes
Driver   = MySQL
Server   = <IP>
Port     = 3306
USER     = <LOGIN>
PASSWORD = <PASSWORD>
Database = abills
```
