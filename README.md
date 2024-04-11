# End-to-End-Kidney-Tumor-Classification-using-Mlflow-and-DVC

### This project employs deep learning techniques to classify kidney tumors using MRI scans. Utilizing TensorFlow with a VGG16 model and Softmax activation, it achieves accurate tumor identification. Integrated with MLflow and DVC for experiment tracking and data versioning, the project also features a Flask web application hosted on AWS EC2. The CI/CD pipeline ensures seamless deployment and updates, making it a comprehensive solution for medical image classification.


## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml
10. app.py

# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/Shashankb1910/End-to-End-Kidney-Disease-Classification-Deep-Learning.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n cnncls python=3.8 -y
```

```bash
conda activate cnncls
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```




### dagshub

MLFLOW_TRACKING_URI=https://dagshub.com/sbadgujar1019/End-to-End-Kidney-Disease-Classification-Deep-Learning.mlflow 
MLFLOW_TRACKING_USERNAME=sbadgujar1019 
MLFLOW_TRACKING_PASSWORD=" "
python app.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/sbadgujar1019/End-to-End-Kidney-Disease-Classification-Deep-Learning.mlflow 

export MLFLOW_TRACKING_USERNAME=sbadgujar1019 

export MLFLOW_TRACKING_PASSWORD=

```


### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


<<<<<<< HEAD
## About MLflow & DVC

MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & taging your model


DVC 

 - Its very lite weight for POC only
 - lite weight expriements tracker
 - It can perform Orchestration (Creating Pipelines)



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 848477405825.dkr.ecr.eu-north-1.amazonaws.com/kidney

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = eu-north-1

    AWS_ECR_LOGIN_URI = demo>>  848477405825.dkr.ecr.eu-north-1.amazonaws.com/kidney

    ECR_REPOSITORY_NAME = kidney

=======
AWS - 848477405825.dkr.ecr.eu-north-1.amazonaws.com/kidney

![Normal](https://private-user-images.githubusercontent.com/129300507/321535479-03f6376b-279a-4b90-89b3-c7f103a6bef0.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTI4MjAwOTUsIm5iZiI6MTcxMjgxOTc5NSwicGF0aCI6Ii8xMjkzMDA1MDcvMzIxNTM1NDc5LTAzZjYzNzZiLTI3OWEtNGI5MC04OWIzLWM3ZjEwM2E2YmVmMC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDExJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQxMVQwNzE2MzVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01MWQ4MDkwYmU3MzU0ZTczZjhkYTRhZWMyZDA2ZjliYjk1MmQyMDNiMDA5YjliMzFkODRiZDI5MTBjMDAwNmNmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.l5IfC4E63K-ekpqSkMV4HW0PxSeNRYcs2n4sfllZhqI)


![Tumor](https://private-user-images.githubusercontent.com/129300507/321535648-a3027dd7-9c22-4abc-8ff3-a0e7ec544ff0.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTI4MjAwOTUsIm5iZiI6MTcxMjgxOTc5NSwicGF0aCI6Ii8xMjkzMDA1MDcvMzIxNTM1NjQ4LWEzMDI3ZGQ3LTljMjItNGFiYy04ZmYzLWEwZTdlYzU0NGZmMC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNDExJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDQxMVQwNzE2MzVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04YWQ4YmM2ZjdiMTI0MTIzODk4YWM0NGFiZmIzOThmZjRjOTJjYmI3ZmE3ZDU4YWZjNzY5ZDgyYmM1ZDgwNzljJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.P-PZgQVJDMdler_YhHVae8Jlmh6KiKnqiIc1wouBnOE)


>>>>>>> cbd9efe99bec3e2c29b48046d4dfef6a5b6dd6b1
