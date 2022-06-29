<div align="center">
  <h1>Scraper Backend</h1>
  <strong>Fetches information about every webpage 🤖</strong>
</div>
<br>
<p align="center">
  <a href="https://circleci.com/gh/dailydotdev/daily-scraper">
    <img src="https://img.shields.io/circleci/build/github/dailydotdev/daily-scraper/master.svg" alt="Build Status">
  </a>
  <a href="https://github.com/dailydotdev/daily-scraper/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/dailydotdev/daily-scraper.svg" alt="License">
  </a>
  <a href="https://stackshare.io/daily/daily">
    <img src="http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat" alt="StackShare">
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

## System configuration

Install Node.js - Standard

Install Visual Studio Code
-> Extension Typescript

Install Yarn: (https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable)
npm install --global yarn

Config Nodemon: (https://blog.logrocket.com/configuring-nodemon-with-typescript/)
yarn add --dev nodemon ts-node

Install pino-pretty: (https://npm.io/package/pino-pretty)
npm install -g pino-pretty


Unit testing with Jest: (https://jestjs.io/docs/getting-started)
yarn add --dev jest
oder
npm install --save-dev jest

See: [Testing TypeScript apps using Jest](https://blog.logrocket.com/testing-typescript-apps-using-jest/)
[ts-jest](https://www.npmjs.com/package/ts-jest)
[Fix Problems](https://medium.com/@joenjenga/its-jest-common-problem-faced-using-jest-9905e96db8a)

