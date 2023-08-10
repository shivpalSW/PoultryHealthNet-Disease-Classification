# MLflow-DVC-PoultryHealthNet-Avian-Disease-Classification
PoultryHealthNet-Avian-Disease-Classification using MLOPS (MLFLOW,DVC and Github actions & AWS cloud )


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

## 3. Created AWS ECR repo to store/ save Docker image
Saved the URI : 815723463103.dkr.ecr.us-east-1.amazonaws.com/poultryhealthnet