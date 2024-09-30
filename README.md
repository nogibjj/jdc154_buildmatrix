# Matrix Build

Brief overview of template for development environment containing Dockerfile, Makefile, Requirements, and CI/CD (github actions)

[![cicd](https://github.com/nogibjj/jdc154_buildmatrix/actions/workflows/cicd.yml/badge.svg)](https://github.com/nogibjj/jdc154_buildmatrix/actions/workflows/cicd.yml)

## Project Overview
The purpose of this project is to set up a Github actions workflow which will test multiple python versions and environments. To do this, I updated my yaml file to include a matrix build of Python versions which will run when I do my github actions.

## requirements.txt
A textfile containing essential packages and versions for your project. Currently with fillers but can be edited and updated depending on your project needs. Make sure to include versions. 

## MAKEFILE
Defines a set of tasks to be executed. Contains commands for installing your requirements (from requirements.txt), linting, formatting, and testing which can be called with 'make command_name' to check your code and run/compile your files more efficiently in an automated manner.

## github actions
cicd.yml file which can be edited based on needs. For CI/CD to automate the DevOps process. Works for multiple Python versions. Maps similar to key value pairs and indentation matters for Github/Gitlab to recognize what pipelines / jobs to run when you push code. 

If the matrix build was correctly configured, we should see: 
![alt text](image.png)

And can see each Python version was successfully run and tested on: 

![alt text](image-4.png)
![alt text](image-3.png)
![alt text](image-2.png)
![alt text](image-1.png)

## devcontainer
Dockerfile and devcontainer to detail virtual machine / environment for project. Update and edit based on project needs.

## Preparation
1. Open codespaces 
2. Load repo to code spaces
2. Wait for installation of all requirements in requirements.txt

## Check format and test errors
1. Format code `make format`
2. Lint code `make lint`
3. Test code `make test`
(alternatively, do all with `make all`) 

