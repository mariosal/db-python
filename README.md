# Design and Applications of Databases - [Python assignment](docs/Assignment.pdf)

## Requirements

- [MariaDB](https://mariadb.org/) >= 5.1
- [Node Foreman](https://strongloop.github.io/node-foreman/)
- [Python](https://www.python.org/) >= 3.4

## Installation

```sh
pyvenv venv
. venv/bin/activate
pip install -r requirements.txt

mysql -u user -p -h host -P port
```

```sql
CREATE DATABASE database;
USE database;
source etc/dump.sql;
```

## Configuration

```sh
echo "DATABASE_URL='mysql://user:password@host:port/database'" >> .env
```

## Execution

```sh
nf start
```

### Development

Change `Procfile` to:

```sh
web: python -m bottle --debug --reload app
```

## Authors

- Alexandros Kalimeris <kalimerisalx@gmail.com> <sdi1400056@di.uoa.gr>
- Mario Saldinger <mariosaldinger@gmail.com> <sdi1400177@di.uoa.gr>
