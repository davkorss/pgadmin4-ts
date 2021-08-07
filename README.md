# pgadmin4-ts
pgAdmin 4 Tiny Service

## Usage

- Remember to add the ``postgres-local`` docker network to your PostgreSQL services
```
version: "3.9"
services:
  postgres:
    image: "postgres"
    networks:
      - postgres-local
networks:
  postgres-local:
    name: postgres-local
```
- Let's clone and run the tiny service
```bash
#!/bin/bash
git clone https://github.com/davkorss/pgadmin4-ts.git
cd pgadmin4-ts
docker-compose up -d --build
```
- Open http://localhost:5050 in your browser
- **username:** ``guest@guest.com`` **password:** ``guest``
