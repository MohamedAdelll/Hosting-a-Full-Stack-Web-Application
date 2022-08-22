# Hosting a Full-Stack Application

---
#test
In this project it's required to take a newly developed Full-Stack application built for a retailer and deploy it to a cloud service provider so that it is available to customers.

By Taking a developed full stack application and deploying it to a cloud service provider so that it is available to customers. This application contains the main components of a 3-tier full stack application (UI, API, and Database).

![Architecture Diagram](Documentation/Architecture_Diagram.png)

## Built With

- TypeScript
- Node.js
- Epress framework
- Angular
- postgreSQL
- AWS
- Circle-CI

### Dependencies

```
- Node v14.15.1 (LTS) or more recent. While older versions can work it is advisable to keep node to latest LTS version

- npm 6.14.8 (LTS) or more recent, Yarn can work but was not tested for this project

- AWS CLI v2, v1 can work but was not tested for this project

- A RDS database running Postgres.

- A S3 bucket for hosting uploaded pictures.

```

### Installation

Provision the necessary AWS services needed for running the application:

1. In AWS, provision a publicly available RDS database running Postgres.

> database-1.cudxhqbqgcj1.us-east-1.rds.amazonaws.com

1. In AWS, provision a s3 bucket for hosting the uploaded files. http://my-first-postgres-bucket.s3-website.us-east-2.amazonaws.com/
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

## CI / CD

> Passed
> ![Pipeline Architecture](screenshots/CircleCi_Success.png)

> Pipeline
> ![Pipeline Architecture](Documentation/Pipeline_Architecture.jpg)

## Testing

This project contains two different test suite: unit tests and End-To-End tests(e2e). Follow these steps to run the tests.

1. `cd starter/udagram-frontend`
1. `npm run test`
1. `npm run e2e`

There are no Unit test on the back-end

### Unit Tests:

Unit tests are using the Jasmine Framework.

### End to End Tests:

The e2e tests are using Protractor and Jasmine.
