[![GoDoc](https://godoc.org/github.com/go-bootstrap/go-bootstrap?status.svg)](http://godoc.org/github.com/go-bootstrap/go-bootstrap)
[![license](http://img.shields.io/badge/license-MIT-red.svg?style=flat)](https://raw.githubusercontent.com/go-bootstrap/go-bootstrap/master/LICENSE.md)

## go-bootstrap

This is not a web framework. It generates a skeleton web project for you to kick-ass.

Feel free to use or rip-out any of its parts.

**NOTE:** Due to lack of Windows machine, at the moment, PostgreSQL template is not working on Windows.


## Prerequisites

1. PostgreSQL or MySQL if you choose to use a database.

2. Go programming language, version 1.3.x or newer.

3. Ensure `$GOPATH/bin` is in your `$PATH`. Example: `PATH=$PATH:$GOPATH/bin`

## Installation

1. `go get github.com/go-bootstrap/go-bootstrap`

2. `$GOPATH/bin/go-bootstrap -dir github.com/{git-user}/{project-name}`

3. Start using it: `cd $GOPATH/src/github.com/{git-user}/{project-name} && go run main.go`


## PostgreSQL Environment Variables

If you have `PGUSER`, `PGPASSWORD`, `PGHOST`, `PGPORT`, `PGSSLMODE` environment variables set,
they will be used to generate and bootstrap the database.


## Decisions Made for You

This generator makes **A LOT** of decisions for you. Here's the list of things it uses for your project:

1. There are 3 templates to choose from:

    * Core: If you don't want a database.

    * PostgreSQL.

    * MySQL.

2. bcrypt is chosen as the password hasher.

3. Bootstrap Flatly is chosen for the UI theme.

4. Session is stored inside encrypted cookie.

5. Static directory is located under `/static`.

6. Model directory is located under `/models`.

7. It does not use a full blown ORM.

8. Test database is automatically created under `$GO_BOOTSTRAP_PROJECT_NAME-test`.

9. A minimal Dockerfile is provided.

10. A minimal Vagrantfile is provided.

11. [github.com/jmoiron/sqlx](https://github.com/jmoiron/sqlx) is chosen to connect to a database.

12. [github.com/gorilla](https://github.com/gorilla) is chosen for a lot of the HTTP plumbings.

13. [github.com/carbocation/interpose](https://github.com/carbocation/interpose) is chosen as the middleware library.

14. [github.com/tylerb/graceful](https://github.com/tylerb/graceful) is chosen to enable graceful shutdown.

15. [github.com/rnubel/pgmgr](https://github.com/rnubel/pgmgr) is chosen as the database migration and management tool for PostgreSQL.

16. [github.com/mattes/migrate](https://github.com/mattes/migrate) is chosen as the database migration and management tool for MySQL.

17. [github.com/Sirupsen/logrus](https://github.com/Sirupsen/logrus) is chosen as the logging library.

18. [github.com/spf13/viper](https://github.com/spf13/viper) is chosen to manage application config.
