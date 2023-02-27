# Udacity_ML-API_Project
[![CircleCI](https://circleci.com/gh/DudeGFA/Udacity_ML-API_Project.svg?style=svg)](https://circleci.com/gh/DudeGFA/Udacity_ML-API_Project)

### Project Overview
In this project, I applied the skills I have acquired in this course to operationalize a Machine Learning Microservice API.

I was given a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on the [data source site](https://www.kaggle.com/c/boston-housing). This project tests my ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks
The project goal is to operationalize this working, machine learning microservice using kubernetes, which is an open-source system for automating the management of containerized applications. In this project I:

- Tested my project code using linting      
- Completed a Dockerfile to containerize this application       
- Deployed my containerized application using Docker and made a prediction            
- Improves the log statements in the source code for this application           
- Configured Kubernetes and created a Kubernetes cluster        
- Deployed a container using Kubernetes and made a prediction           
- Uploade a complete Github repo with CircleCI to indicate that my code has been tested

### Environment setup, code test and lint
- Run `make all`

### Running `app.py`            
1. Standalone - `python app.py`                         
2. On a docker container - `./run_docker.sh`                    
3. In a Kubernetes cluster - `./run_kubernetes.sh`              
**To run using option 3, a kubernetes cluster must be provided and setup**            

### Brief description of files          
- model_data: Contains data used in training the sk_learn model             
- output_txt_files: contains logging output of `./run_docker.sh` and `./run_kubernetes.sh` commands         
- app.py: Machine learning flask app            
- Dockerfile: Contains instructions for building the docker container           
- make_predictions.sh: Bash script that send sample request to the running app              
- Makefile: includes instructions on environment setup and lint tests               
- requirements.txt: app environmental dependemcies          
- run_docker.sh: Bash script to run the application on a docker container           
- run_kubernetes.sh: Bash script to run the application in a kubernetes cluster                 
- upload_docker.sh: Bash script to upload the built docker container to docker hub              
