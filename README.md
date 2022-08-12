# MLOps-01

## Introduction

## Data source

data source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download

## To start 

`docker-compose -f docker-compose.yml up -d `

## Start training models

Assuming there are 2 types of scenario:
 - In your own environment, For example: conda. Enter "mlflow file", type `python train.py`
 - Inside mlflow container, enter container through docker desktop or `docker exec -it [container ID] /bin/bash`. Enter "train" file, type `python train.py`.

## MLflow Server

You can access mlflow tracking server at `127.0.0.1:5000`

## Min IO 

Min IO is used to store files that can be used to rebuild our models. 

You can access Min IO service at `127.0.0.1:9000`

## Nginx

Nginx is used to perform simple authentication in this case. 

You can access it at `127.0.0.1`
 
## Notes
 - If you run into error "import boto 3 ". Run the following command in your enviroment `pip install boto3`
 - mlflow's function : `mlflow run [URI or Git repo] --no-conda` did not work well with docker. If conda.yml file is in the same directory with docker-compose.yml, it would report error. 
- Run this if using IOS to allow wait-for-it.sh running, if not, can't creat a bucket at the start. `sudo chmod -R 777 wait-for-it.sh` 
- visual studio code install "docker extension" and "remote containers". The docker extension is important. 
- change IP address in dockerfile or change it inside container's train.py.
- Remote containers might return NewConnectionError 113 on Mac when first time connecting. Close the remote connection and restart.
