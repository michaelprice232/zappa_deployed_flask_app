# Basic Flask App Deployed via Zappa

Simple Flask application, automatically deployed to AWS Lambda/Gateway via Zappa. Based on tutorial [here](https://www.gun.io/blog/serverless-microservices-with-zappa-and-flask).

Pre-requisite:
1) Update the BUCKET_NAME variable to use in `my_app.py` file
2) Have a valid AWS CLI credentials file configuration with IAM permissions to create all the required Lambda/API Gateway/IAM/S3/Cloudwatch resources

## To set up the environment:
* python3 -m venv venv
* source venv/bin/activate
* pip install -r requirements.txt
* zappa init (for the first time config setup. Your AWS CLI credentials file needs to be configured)
* zappa deploy *environment* (the environment name is defined in the previous step)

## To update the stack once code changes have been made:
* zappa update *environment*

## To clean up the resources:
* zappa undeploy *environment*