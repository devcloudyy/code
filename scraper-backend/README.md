<div align="center">
  <h1>Scraper Backend</h1>
  <strong>Fetches information about every webpage 🤖</strong>
</div>
<br>
<p align="center">
  <a href="">

  </a>
</p>

The service uses [Puppeteer](https://github.com/puppeteer/puppeteer), a headless Chrome, to scrape webpages.
Currently it's only purpose is to provide information when a user suggests a new source.
The scraper can find the icon, rss feed, name, and other relevant information for every page.

## Stack

* Node v12.19.0 (a `.nvmrc` is presented for [nvm](https://github.com/nvm-sh/nvm) users).
* NPM for managing dependencies.
* Fastify as the web framework

## Project structure

* `__tests__` - There you can find all the tests and fixtures. Tests are written using `jest`.
* `helm` - The home of the service helm chart for easily deploying it to kubernetes.
* `src` - This is obviously the place where you can find the source files.
  * `scrape` - Stores many utility functions to scrape information from a webpage.

## Local environment

Daily Scraper requires nothing to run. It doesn't need any database or a service.

[.env](.env) is used to set the required environment variables. It is loaded automatically by the project.

Finally run `npm run dev` to run the service and listen to port `5001`.

--


## System configuration - Installation

### `Visual Studio Code` 
* [Extension Typescript](https://marketplace.visualstudio.com/items?itemName=TypeScriptTeam.typescript-474)

### `NodeJS` ([Link](https://nodejs.org/)) 
* [Package HTTP Server](https://www.npmjs.com/package/http-server)
```bash
# Check installation
node --version

# Add HTTP Server package
npm install --global http-server
```

### `Yarn` ([Link](https://classic.yarnpkg.com/lang/en/docs/install/))
```bash
# Global installation
npm install --global yarn

# Check installation
yarn --version
```

### `Nodemon and ts-node` ([Link](https://blog.logrocket.com/configuring-nodemon-with-typescript/))
```bash
# Global installation
yarn global add nodemon ts-node
# yarn global add nodemon --prefix /usr/local

# Local installation
yarn add --dev nodemon ts-node

# Check installation
which nodemon

# Add to PATH
export PATH="$(yarn global bin):$PATH"
```

### `pino-pretty` ([Link](https://npm.io/package/pino-pretty))
```bash
# Global installation
npm install -g pino-pretty

# Local installation
yarn add --dev pino-pretty

```

### `Jest` ([Link](https://jestjs.io/docs/getting-started))
* and Package [ts-jest](https://www.npmjs.com/package/ts-jest)

```bash
# Global installation
npm install -g jest

# Local installation
npm install --save-dev jest
# yarn add --dev jest


## for TypeScript see also:
npm i ts-jest
```

<br />

<br />

# Run Tests

## Unit testing with Jest ([Link](https://jestjs.io/docs/getting-started))
1. Testing - [Testing TypeScript apps using Jest](https://blog.logrocket.com/testing-typescript-apps-using-jest/)
2. Hotfixes - [Common Issues](https://medium.com/@joenjenga/its-jest-common-problem-faced-using-jest-9905e96db8a)

## Create Test Units
```bash
# Locate Directory of scraper-backend\test-units
cd %PROJECTPATH%\scraper-backend\__tests__

# Run Test Units
jest --testEnvironment=node --runInBand
```

<br />

## Start NodeJS http server
```bash
# Locate Directory of Web Application
cd %PROJECTPATH%\scraper-backend\__tests__\fixture

# Run http server
http-server .
```
> Now, you can visit http://127.0.0.1:8080 or http://localhost:8080

## Start scraper-backend Service
```bash
# Locate Directory of scraper-backend Service
cd %PROJECTPATH%\scraper-backend

# Run Service/Project
npm run dev
```
> Now, you can visit http://127.0.0.1:5001 or http://localhost:5001

