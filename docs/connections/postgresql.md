# Postgresql


## Installation

### Docker CLI

The following command line is used to run it
``` bash
docker run -d --name postgres -p 5432:5432 postgres:latest
```

Or you can change with a more specific version such as `postgres:alpine3.20` or other version tags at [docker hub](https://hub.docker.com/_/postgres/tags)

``` bash
docker run -d --name postgres-alpine -p 5432:5432 postgres:alpine3.20
```

### Docker Compose

Before using the configuration below, make sure you have installed docker compose first.

To run it you can copy the script below
``` yaml hl_lines="3" title="docker-compose.yaml"
services:
  postgres:
    image: postgres:latest
    container_name: postgres-latest
    ports:
      - 5432:5432
    network_mode: bridge
```

You can change the version of the database highlighted in the script above, with a more specific version such as `postgres:alpine3.20` or other version tags at [docker hub](https://hub.docker.com/_/postgres/tags)


#### Download the script

Can also download the docker compose that I have provided, just download with the command line below

``` bash
wget -L https://raw.githubusercontent.com/oktapiancaw/dockerize-apps/refs/heads/master/compose/postgresql.yaml -O docker-compose.yaml
```

Then run this command line to run the latest version 

``` bash
docker compose up -d local-latest
```

## Properties

**Comming soon, hehe**