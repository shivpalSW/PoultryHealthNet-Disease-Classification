# PoultryHealthNet-Avian-Disease-Classification
PoultryHealthNet-Avian-Disease-Classification using MLOPS 

### Tool stack used:
1. Python
2. DVC 
3. Github actions 
4. Docker
5. AWS cloud (I AM,ECR,EC2)

### WOrkflow steps I have followed in this project
1. created config.yaml
2. created secrets.yaml [Optional] (for if we are using databse and in case we need to keep credentials secreat )
3. created params.yaml
4. created the entity
5. created the configuration manager in src config
6. created the components
7. created the pipeline file
8. created the main.py file
9. created the dvc.yaml file (MLOPS tool)

# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/shivpalSW/PoultryHealthNet-Disease-Classification
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


### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


# AWS-CICD-Deployment-with-Github-Actions

## 1. Logged in to AWS console.

## 2. Created IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Add Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Created ECR repo to store/save docker image
    - Save the URI: 815723463103.dkr.ecr.ap-south-1.amazonaws.com/poultryhealthnet

	
## 4. Created EC2 machine (Ubuntu) 

## 5. Opened EC2 and Installed docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configured EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app


# 8. Push your CICD.yaml file and moniter Github-->Actions window for CICD Process.