
# Full Stack FastAPI, Vue 2 and PostgreSQL 

Official git repository : https://github.com/tiangolo/full-stack-fastapi-postgresql

## Requirements
- [Git](https://cli.github.com/)
- [Docker](https://www.docker.com/)
- [Docker-compose](https://docs.docker.com/compose/gettingstarted/)

## Installation
**Optional** :

Replace "myexample" and "myexample.com" by your project name in :
- .env
- .gitlab-ci.yml
- frontend/.env
---
**Clone the project** : \
``git clone https://github.com/frederic-spielmann/full-stack-fastapi-vue2-postgresql.git``

``cd full-stack-fastapi-vue2-postgresql``

**Start the stack** : \
``docker-compose up -d --build``

**Make sure the containers are running** : \
``docker container ls --all``

Open http://localhost/ in your web browser (port 80)  :
- Login: ``admin@myexample.com``
- Password: ``password``

## Stack:
This stack is mainly for testing purpose.
- Backend: [fastapi](https://fastapi.tiangolo.com/) (Python)
- Frontend: [VueJS 2](https://vuejs.org/) (deprecated, End-of-life: 31/12/2023 )
- Database: [postgresql v12](https://www.postgresql.org/)
- DB GUI: [pgadmin 4](https://www.pgadmin.org/)
- Proxy: [traefik](https://traefik.io/)
- Message-Broker: [rabbitmq](https://www.rabbitmq.com/)
- Monitoring and Admin Celery clusters: [mher/flower](https://github.com/mher/flower)
- Task Worker: [celeryworker](https://docs.celeryq.dev/en/stable/index.html)

## Frontend:
Packages.json

    "axios": "0.27.2",
    "core-js": "3.25.0",
    "register-service-worker": "1.7.2",
    "typesafe-vuex": "3.2.2",
    "vee-validate": "3.4.14",
    "vue": "2.7.10", (deprecated -> Vue 3)
    "vue-class-component": "7.2.6",
    "vue-property-decorator": "9.1.2",
    "vue-router": "3.6.5",
    "vuetify": "2.6.9", (deprecated -> Vuetify 3)
    "vuex": "3.6.2" (deprecated -> Pinia)

## Backend:
pyproject.toml

    python = "^3.10"
    uvicorn = "^0.18.3"
    fastapi = "^0.82.0"
    python-multipart = "^0.0.5"
    email-validator = "^1.2.1"
    requests = "^2.28.1"
    celery = "^5.2.7"
    passlib = {extras = ["bcrypt"], version = "^1.7.4"}
    tenacity = "^8.0.1"
    pydantic = "^1.10.2"
    emails = "^0.6"
    raven = "^6.10.0"
    gunicorn = "^20.1.0"
    jinja2 = "^3.1.2"
    psycopg2-binary = "^2.9.3"
    alembic = "^1.8.1"
    sqlalchemy = "^1.4.40"
    pytest = "^7.1.3"
    python-jose = {extras = ["cryptography"], version = "^3.3.0"}