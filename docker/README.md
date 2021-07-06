# Cloud Agnostic Open Source NiFi Data Pipeline

This project contains Docker Image of a NiFi pipeline that is built to extract data from a variety of sources and bring it all into a centralised data lake.

**Website** :

The working project URL can be accessed at [https://sampathcodes.com:8080/nifi](https://sampathcodes.com:8080/nifi) which is subject to the request to bring the pipeline up.

**Architecture Diagram** :

<img width="492" alt="architecture_diagram" src="https://user-images.githubusercontent.com/55593893/124603972-0cbee180-de9d-11eb-8b1a-169b4f8d6de8.png">

**Directory Structure** :

Code Files | Content Info
------------ | -------------
flow.xml.gz | contains the NiFi pipeline flow logic built to extract data from different sources.
Dockerfile | Contains the definition of NiFi Dockerfile to be built deploy the  changes made to made to the repository

**Execution Steps** :

1. The Latest Docker NiFi image is pulled from docker repository : [https://hub.docker.com/r/sampathdocks/aaqua_nifi](https://hub.docker.com/r/sampathdocks/aaqua_nifi)
2. The Image runs in AWS Fargate using ECS container deployment mode. 
3. The Pipeline collects data from a variety of data sources like Kafka, MongoDB, PostgreSQL and puts the data into S3.
4. The solution is cloud-agnostic because the NiFi container Image can be deployed to any Cloud services provider or can be run on an on-premise server with docker.



