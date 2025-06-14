## Add ollama in the container

`docker compose up -d`

## Access ollama commands from the container

`docker compose exec ollama bash`

## Install LLM using ollama

`ollama run llama3.2:latest`

## To exit from the CLI LLM

`/bye`

## Visit this to access Librechat with ollama running

`http://localhost:3080/`

## Visit this to access mongo-express (not supported yet, maybe will add later)

`http://localhost:8081/`

username: admin

password: password

## To stop librechat, in the docker bash:

`exit`

`docker compose down`

---

# DEVELOPMENT
```
npm i -g typescript
npm ci
npm run build:data-provider
npm run build:data-schemas
npm run build:api
```

from original contributions doc:

## 1. Development Setup

1. Use Node.JS 20.x.
2. Install typescript globally: `npm i -g typescript`.
3. Run `npm ci` to install dependencies.
4. Build the data provider: `npm run build:data-provider`.
5. Build data schemas: `npm run build:data-schemas`.
6. Build API methods: `npm run build:api`.
7. Setup and run unit tests:
    - Copy `.env.test`: `cp api/test/.env.test.example api/test/.env.test`.
    - Run backend unit tests: `npm run test:api`.
    - Run frontend unit tests: `npm run test:client`.
8. Setup and run integration tests:
    - Build client: `cd client && npm run build`.
    - Create `.env`: `cp .env.example .env`.
    - Install [MongoDB Community Edition](https://www.mongodb.com/docs/manual/administration/install-community/), ensure that `mongosh` connects to your local instance.
    - Run: `npx install playwright`, then `npx playwright install`.
    - Copy `config.local`: `cp e2e/config.local.example.ts e2e/config.local.ts`.
    - Copy `librechat.yaml`: `cp librechat.example.yaml librechat.yaml`.
    - Run: `npm run e2e`.
