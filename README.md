# Assignment 3 : MGMT 590, Production Scale Data Products, Summer 2021

## Creating Web Application - Question Answering

Purpose of the this hands-on project was to create a Web Application using Stream Lit API
The app is deployed at: https://mgmt590-webapp-ykof2ki2ga-uc.a.run.app

## Learning Outcomes

At the end of the this hands-on training, students will be able to;

- Understood the achitechture of the Webapp

- Get fimiliar with the Streamlit content

- Automated deploy using a GitHub Action that executes the following on merges into the
master branch of your GitHub repository

- Build an accessible webapplication

- Use git repo to manage the application versioning.

- Using cloud SQL database to run the application.

## User Guide

### Below is the preview to all the functionalities of the web application.

- Get List of Models : Used to get list of models in the DB 
![Get](./one.PNG)

- Insert a model : Used to insert a model with the model name, model type, tokenizer of the model. ()
![Insert](./two.png)

- Delete a model
- ![Delete](./three.png)

- Get Answers
- ![Get](./three.png)

- Recently Answered Questions
- ![Recent](./four.png)

- Upload a file with questions to get the answers
- ![Upload](./five.PNG)

## Dependencies

The Dependencies are in the `requirements.txt` namely:

Flask==1.1.2

transformers[torch]==4.2.2

requests==2.25.1

streamlit==0.82.0

pandas==1.1.5

pytest==6.2.4

freezegun==1.1.0

mock==4.0.3

if you want to exactly rebuild the development environment
run the following command:

    (venv) $ pip install -r requirements.txt
    
The required packages are outdated very quickly and you can try to use newer versions.
If you experience problems you can always go back and use the version specified here.

To generate your own requirements file use

    (venv) $ pip freeze >requirements.txt
## ## Usage
### Without Docker
To run the dashboard, please execute the following from the root directory:
```bash
pip3 install -r requirements.txt
streamlit run dashboard.py
```
When run locally, the dashboard is accessible here:
```
http://localhost:8501
```

### With Docker
To run the web app using Docker containers, please execute the following from the root directory:
```bash
docker build -t dashboard .
docker run -d --name dashboard -p 8501:8501 dashboard
```
 
 
 
