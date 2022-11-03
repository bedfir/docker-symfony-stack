# Docker Symfony Stack,  PHP-fpm 8.1 / Nginx / Postgres

Create multiple symfony project with docker.
## Requirements
Docker (v18.06+)
Docker Compose (v1.22+)

## Getting Started

### installation

1. Clone this directory

`git clone git@github.com:bedfir/docker-symfony-stack.git`

Get the pgadmin for all the bdd servers


2. Complete the .env file

> Change these examples: 

APP_NAME=`myProject`

FOLDER_WWW=`myProject` 

DOMAIN=`myProject`

POSTGRES_PASSWORD=`Yello123`

POSTGRES_USER=`myProject-user`

POSTGRES_DB=`myProject-bdd`

PORT_SERVER=`80`

PORT_BDD=`5432`

### Build and run

From this directory, start up services by running `docker-compose up -d`

### Install your symfony project

Follow instructions from the symfony project, taking into account :

* `docker compose exec <APP_NAME>-php <command>`
> **example** `docker compose exec myProject-php composer create-project symfony/skeleton:"6.1.*" .`
