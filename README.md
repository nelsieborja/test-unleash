# Running the [Unleash](https://www.getunleash.io) service

Run following commands in a terminal/bash shell:

### Prerequisites
Install the dependencies

```shell
npm init
npm install unleash-server --save
```

Create a local `unleash` database in PostgreSQL
```shell
$ psql postgres <<SQL
CREATE USER unleash_user WITH PASSWORD 'password';
CREATE DATABASE unleash;
GRANT ALL PRIVILEGES ON DATABASE unleash to unleash_user;
SQL
```

### Start PostgreSQL service
```shell
brew services restart postgresql@15
```

### Start the Unleash server
```shell
node server.js
```

### Login with the default credentials

username: admin
password: unleash4all

---
## References

* [Unleash server setup](https://docs.getunleash.io/using-unleash/deploy/getting-started)
* [Postgres15 permission denied for schema public](https://stackoverflow.com/questions/74110708/postgres-15-permission-denied-for-schema-public)