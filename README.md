# postgres-pg-cron

Docker image Postgres:17 with PG_Cron installed

## Overview

This project provides a Docker image based on Postgres 17 with the `pg_cron` extension pre-installed and configured. The `pg_cron` extension allows you to run scheduled jobs directly inside the PostgreSQL database.

## Features

- **Postgres 17**: The latest version of PostgreSQL.
- **pg_cron**: Schedule jobs using cron syntax directly in PostgreSQL.
- **Custom Entrypoint**: A custom entrypoint script to configure `pg_cron` with the specified database.
- **Initialization Scripts**: Support for running initialization SQL scripts on container startup.

## Usage

### Docker Compose

To run this image using Docker Compose, use the following configuration:

```yaml
services:
  postgres:
    image: nikelborm/postgres-pg-cron:latest
    restart: always
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: postgres
      POSTGRES_DB: postgres
    volumes:
      - pgdata:/var/lib/postgresql/data
    ports:
      - "5432:5432"

volumes:
  pgdata:
```

Feel free to adjust any sections as needed.
