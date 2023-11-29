# 2semDockerSetupLocal
Local setup with Postgres and PgAdmin for 2nd semester

# Setup Localhost

## Requirements

- [Docker](https://docs.docker.com/get-docker/) Docker installed (Docker Desktop on Windows and Mac)

## Documentation

- [PostgreSQL](https://www.postgresql.org/) for database
- [pgAdmin](https://www.pgadmin.org/) for database management
- [Docker](https://www.docker.com/) for containerization
- [Docker Compose](https://docs.docker.com/compose/) for container orchestratio

## Setup

### 1. Install Docker Desktop

[Docker Desktop](https://docs.docker.com/get-docker/). If you are installing on Windows, you might need to update WSL. A message with instructions will show if necessary during installation.

### 2. Clone this repo

Clone this repo and open the folder with docker-compose.yml in `Git Bash` on Windows or `Terminal` on Mac.

### 2. Run Docker

```bash
  docker-compose up -d
```

### 3. Access Postgres pgadmin dashboard through browser

```bash
  localhost://5050
```
#### 3.1. Login
- login: **admin@cphbusiness.dk** (see docker-compose.yml)
- password: **1234** (see docker-compose.yml)

#### 3.2. Add new server
- Host name/address: **db**
- Port: **5432**
- username: postgres
- password: postgres

*** 

###  Stop Docker

```bash
  docker-compose down
```

### Reset DB data installation

(-v) // remove volumes
```bash
 docker-compose down -v 
```

```bash
 sudo  rm -rf ./data
```

***

## Debugging

- Check if all containers are running with `docker ps -a`
- Check if all env variables are set in .env file and are correct
- Check if docker compose has read all environment variables with `docker-compose config`
- Check the logs of the individual container with `docker logs <container_name>` or `docker logs --follow <container_name>`

