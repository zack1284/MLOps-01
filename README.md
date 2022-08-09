# MLOps-01

## Introduction

## Data source

data source: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud?resource=download

## MLflow Server

You can find mlflow tracking server at `127.0.0.1:5000`

## Min IO 

Min IO is used to store files that can be used to rebuild our models. You can find Min IO service at `127.0.0.1:9000`

## Nginx

Nginx is used to perform simple authentication in this case. You can find it at `127.0.0.1`

## To start 

`docker-compose -f docker-compose.yml up -d `

## Start training models

 - In your own environment, For example: conda. Enter "mlflow file", type `python train.py`
 - Inside mlflow container, enter container through docker desktop or `docker exec -it [container ID] /bin/bash`. Enter "train" file, type `python train.py`.