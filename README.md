# Hosting a Full-Stack Application

### **You can use you own project completed in previous courses or use the provided Udagram app for completing this final project.**

---

In this project you will learn how to take a newly developed Full-Stack application built for a retailer and deploy it to a cloud service provider so that it is available to customers. You will use the aws console to start and configure the services the application needs such as a database to store product information and a web server allowing the site to be discovered by potential customers. You will modify your package.json scripts and replace hard coded secrets with environment variables in your code.

After the initial setup, you will learn to interact with the services you started on aws and will deploy manually the application a first time to it. As you get more familiar with the services and interact with them through a CLI, you will gradually understand all the moving parts.

You will then register for a free account on CircleCi and connect your Github account to it. Based on the manual steps used to deploy the app, you will write a config.yml file that will make the process reproducible in CircleCi. You will set up the process to be executed automatically based when code is pushed on the main Github branch.

The project will also include writing documentation and runbooks covering the operations of the deployment process. Those runbooks will serve as a way to communicate with future developers and anybody involved in diagnosing outages of the Full-Stack application.

# Udagram

This application is provided to you as an alternative starter project if you do not wish to host your own code done in the previous courses of this nanodegree. The udagram application is a fairly simple application that includes all the major components of a Full-Stack web application.



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

1. In AWS, provision a publicly available RDS database running Postgres. `postgres.c9yipu3gzpbi.us-east-1.rds.amazonaws.com`
1. In AWS, provision a s3 bucket for hosting the uploaded files. `http://mybucket-864662948199.s3-website-us-east-1.amazonaws.com`
1. Export the ENV variables needed or use a package like [dotnev](https://www.npmjs.com/package/dotenv)/.
* POSTGRES_USERNAME=postgres
* POSTGRES_PASSWORD=postgres
* POSTGRES_HOST=postgres.c9yipu3gzpbi.us-east-1.rds.amazonaws.com
* POSTGRES_DB=postgres
* AWS_BUCKET=arn:aws:s3:::mybucket-864662948199
* AWS_REGION=us-east-1
* AWS_PROFILE=default
* JWT_SECRET=mysecretstring
* URL=http://localhost:8100
1. From the root of the repo, navigate udagram-api folder `cd starter/udagram-api` to install the node_modules `npm install`. After installation is done start the api in dev mode with `npm run dev`.
1. Without closing the terminal in step 1, navigate to the udagram-frontend `cd starter/udagram-frontend` to intall the node_modules `npm install`. After installation is done start the api in dev mode with `npm run start`.

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

## Built With

- [Angular](https://angular.io/) - Single Page Application Framework
- [Node](https://nodejs.org) - Javascript Runtime
- [Express](https://expressjs.com/) - Javascript API Framework

## License

[License](LICENSE.txt)


## Front-End Link:

- Link to the hosted working frontend application:
  (http://mybucket-864662948199.s3-website-us-east-1.amazonaws.com)

## Screenshots:

1. AWS RDS for the database overview:
   ![RDS](/screenshots/console_RDS.png)
2. AWS ElasticBeanstalk for the (backend) API deployment:
   ![Home](/screenshots/console_elastic.png)
3. AWS S3 for (frontend) web hosting: ``
   ![Home](/screenshots/console_s3.png)
4. Home page of the application:
   ![Home](/screenshots/fe.png)
5. Udagram Project in Circle CI:
   ![Udagram](/screenshots/circle_ci_pipeline.png)
6. Environment Variables:
   ![Udagram](/screenshots/config_enviroment_variable_circle_ci.png)
7. Picture of the last successful execution of the pipeline:
   ![Last Build](/screenshots/circle_ci_workflow.png)
8. Build Phase
   ![Build](/screenshots/circle_ci_build.png)
9. Deployment Phase
   ![Deployment](/screenshots/circie_ci_deploy.png)
