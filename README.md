# aws SAM app with Lambda
In this project initialize and deploy a simple API using aws SAM. 

## Technologies Used
* aws SAM
* aws CLI
* Python 3.8
* REST API
* Docker


## Dependencies
* Install aws SAM - https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html
* Install aws CLI – https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
* Install Python3.8 - https://www.python.org/downloads/release/python-380/
* Install Docker - https://docs.docker.com/desktop/windows/install/


## Executing program
* Download the repository to your computer and go to project file
```
git clone https://github.com/sayedh/awsSAM-Lambda-app
cd awsSAM-Lambda-app
```
* Configure the aws CLI
```
aws configure
```
![image](https://user-images.githubusercontent.com/30685241/176317869-1c21f2a8-0b12-412e-85fc-ddffc15d462e.png)


* Build and deploy the app
```
sam build
sam deploy --guided
```
* Get the API Endpoint from the Lambda > Functions page in the AWS management console

![image](https://user-images.githubusercontent.com/30685241/176315943-bd056654-dafb-4e77-afb7-dc21baa21f8e.png)

* Finally test the API - https://3hvs85ic4m.execute-api.us-west-1.amazonaws.com/Prod/helloWorld?personId=5

![image](https://user-images.githubusercontent.com/30685241/176316025-ad34f4a8-5c74-42e4-a177-62ad0192d6d2.png)

## Run the API locally
* Ensure Docker is up and running 
* Start the local host with following command 
```
sam local start-api
```

![image](https://user-images.githubusercontent.com/30685241/176317829-64738774-3873-4209-b1a7-b8615eebb17f.png)

* Now test it - http://127.0.0.1:3000/helloWorld?personId=6

![image](https://user-images.githubusercontent.com/30685241/176317725-abf42802-30e9-4afc-a966-8341a2a234b9.png)
