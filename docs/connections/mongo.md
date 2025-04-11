# MongoDB


## Installation

### Docker CLI

The following command line is used to run it
``` bash
docker run -d --name mongo -p 27017:27017 mongo:latest
```

Or you can change with a more specific version such as `mongo:4.4` or other version tags at [docker hub](https://hub.docker.com/_/mongo/tags)

``` bash
docker run -d --name mongo-v4 -p 27017:27017 mongo:4.4
```

### Docker Compose

Before using the configuration below, make sure you have installed docker compose first.

To run it you can copy the script below
``` yaml hl_lines="3" title="docker-compose.yaml"
services:
  mongo:
    image: mongo:latest
    container_name: mongo-latest
    ports:
      - 27017:27017
    network_mode: bridge
```

You can change the version of the database highlighted in the script above, with a more specific version such as `mongo:4.4` or other version tags at [docker hub](https://hub.docker.com/_/mongo/tags)


#### Download the script

Can also download the docker compose that I have provided, just download with the command line below

``` bash
wget -L https://raw.githubusercontent.com/oktapiancaw/dockerize-apps/refs/heads/master/compose/mongo.yaml -O docker-compose.yaml
```

Then run this command line to run the latest version

``` bash
docker compose up -d local-latest
```

## Properties

**Comming soon, hehe**