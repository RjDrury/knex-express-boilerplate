# express-knex-postgres-boilerplate

Boilerplate code for quick setup for CRUD applications using express/knex/postgres/jest/supertest

##Setup - Detailed Instructions Below

1. Git clone the repo ```git clone [url]``` and remove origin ```git remote remove origin```
2. npm install
3. setup postgres backend
4. Modify .env file to suit your backend and migrate/seed db
  1. migrate tables ```npx knex migrate:latest```
  2. run seeds ```npx knex seed:run```
5. npm run server
6. npm run test
7. modify code to suit your needs

## Setup PostgreSQL

### Homebrew (for macOS users)

If you dont have postgres follow this link (Follow directions until you're able to get into psql utility): https://www.codementor.io/engineerapart/getting-started-with-postgresql-on-mac-osx-are8jcopb

#### Create dev and test database (Mac)

In terminal run the following commands:

1. ```psql``` -- To get into postgreSQL utility
2. ```CREATE DATABASE db-name;``` -- Creates development server
3. ```CREATE DATABASE db-name-test;``` -- Creates testing server
4. ```\q```
5. CD into your repo


## Environmental Variables at Runtime

Create a ".env" file at the root of your project and add the following for both DEV and TEST databases

```
    POSTGRES_DEV_HOST=localhost
    POSTGRES_DEV_PORT=5432
    POSTGRES_DEV_USER=postgres
    POSTGRES_DEV_PASSWORD= \_Insert your postgres password here*
    POSTGRES_DEV_DATABASE=db-name
```

```
    POSTGRES_TEST_HOST=localhost
    POSTGRES_TEST_PORT=5432
    POSTGRES_TEST_USER=postgres
    POSTGRES_TEST_PASSWORD= \_Insert your postgres password here*
    POSTGRES_TEST_DATABASE=db-name-test
```
