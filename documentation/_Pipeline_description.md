# Pipeline Process

## CircleCI is used to build this pipeline

<br>

### The configuration of the pipeline contains:

<br>

#### 1- First, CircleCI install node and aws cli and eb cli

#### 2- Then circleCI checks if there are any changes made to the repo uisng the checkout process

#### 3- Then CircleCI installs the frontend and the backend dependencies

#### 4- After that, CircleCI builds the frontend and the backend to make the app ready for production

#### 6- After that, CircleCI deploys the frontend to S3 bucket and the backend to EB

<br>

### Pipeline illustration

![pipeline-diagram](./pipeline.png)
