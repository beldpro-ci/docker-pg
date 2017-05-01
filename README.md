<h1 align="center"> docker-pgdb 📑  </h1>

<h5 align="center">Docker image with easy postgre database initialization</h5>

<br/>

### Overview

```yml
version: '3.2'
services:
  postgres:
    restart: 'always'
    ports:
      - '5432:5432'
    environment:
      - "PG_DB_USER=authd"
      - "PG_DB_PASSWORD=authd"
      - "PG_DB_DATABASE=authddb1"
      - "POSTGRES_PASSWORD=password"
    build: './db'
    networks:
      infranet:
        aliases:
          - 'postgres'

networks:
  infranet:
``` 

<br/>

### LICENSE

MIT
