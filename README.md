# Overview

The purpose of this project is to create a Continuous Integration/Continuous Delivery (CI/CD) pipeline for a Python Machine Learning Flask application.  The application returns a prediction of a median housing price of a house in the Boston area given a set of input variables.

## Project Plan
The project plan for the pipeline is described in a Trello board and spreadsheet:

Trello Board: https://urldefense.com/v3/__https://trello.com/b/fPufDYN5/azure-pipeline__;!!BhdT!1tKzq60elvX4JeWiTR_IXuGxxPS_GZg2Vrom05KtOiEh6-HJkbvgRfM7$
Spreadsheet: * A link to a spreadsheet that includes the original and final project plan>

## Instructions

The CI/CD pipeline consists of two separate pieces: (1) A CI pipeline implemented using Github as a repository, Azure Cloud Shell as a workspace or jump server, and Github Actions Container as a SaaS build server; and (2) A CD pipeline that uses Github as a repository and Azure Pipelines as a deployment server, deploying the application as an Azure Web App.

![CI/CD Pipeline Architecture](/images/arch.jpg)

The steps for running the CI/CD pipeline to build and deploy the application are:

(1) Create (or log into your Azure account).

(2) Clone the project from Github

Execute the command:

git clone https://github.com/sgriesmer/azure-pipeline.git

(3) Create Python Virtual Enviroment

python3 -m env ~/.myrepo
source ~/.myrepo/bin/activate

(4) Install, lint, and test the application locally

Execute the command:

make all

to install, lint, and test the application into the Github repository.

Any code changes should pass tests.  The output of a successful test run should look like:

![Test results after make all](/images/"screen slot of passed tests after make all".png)

(5) Push code to Github and verify that lint and test pass remotely

Execute the commmands:



(6) 


<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


