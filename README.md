<img width="1273" height="310" alt="image" src="https://github.com/user-attachments/assets/68658e34-ebfb-41d7-a65d-9017fa4ca0dc" /><img width="1273" height="310" alt="image" src="https://github.com/user-attachments/assets/68658e34-ebfb-41d7-a65d-9017fa4ca0dc" /># Trading journal

A simple trade journal app built with Python Flask.

![home](https://github.com/mransbro/tradingjournal/blob/main/img/homepage.png)

## Installation

Make sure you have the following prereqs:

1. Python >= 3.11
2. Pip
3. Git

Installing the app is easy:

1. Clone the repository in the directory you wish: `git clone` https://github.com/mransbro/tradingjournal.git
2. Enter the tradingjournal directory. (cd tradingjournal)
3. Install requirements: `pip install -r requirements.txt`
4. Run the app: `python3 run.py`.
5. For production use gunicron `gunicorn -w 4 "app:init_app()"`

## Want to try it out

Demo running on [Render](https://tradingjounral.onrender.com)

## Roadmap

- Error handling
- Tests
- Reduce number of packages

# Built with

- [Python 3](https://python.org): programming language
- [Flask](https://flask.palletsprojects.com): web framework
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com): database
- [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/): python WSGI server
- [Bootstrap](https://getbootstrap.com/): CSS and JS framework
- [Black](https://black.readthedocs.io/en/stable/): Python linting

=============================================== Assignment Task ======================================

## CI/CD Pipeline Implementation using GitHub Actions for Flask Application

Overview

This project demonstrates the implementation of a Continuous Integration and Continuous Deployment (CI/CD) pipeline using GitHub Actions for a Flask-based Python application. The pipeline automates the process of building, testing, and deploying the application based on branch activity and release events.

The objective is to ensure that code changes are validated through automated testing and deployed in a structured and controlled manner.

<img width="1273" height="310" alt="image" src="https://github.com/user-attachments/assets/de8f179d-9617-4a32-a473-5535105127e4" />
<img width="1273" height="310" alt="image" src="https://github.com/user-attachments/assets/de8f179d-9617-4a32-a473-5535105127e4" />



## Project Structure

The repository is organized as follows:

app/ – Contains the main Flask application code
tests/ – Includes test cases for validating application functionality
run.py – Entry point to run the Flask application
requirements.txt – Lists all required Python dependencies
.github/workflows/ci-cd.yml – Defines the CI/CD pipeline

## CI/CD Workflow

The pipeline is configured using GitHub Actions and is triggered by specific repository events.

## Continuous Integration

When code is pushed to the main or staging branch, the following steps are executed:

Checkout of the repository code
Setup of Python environment
Installation of dependencies using pip
Execution of test cases using pytest

This ensures that all changes are tested before being considered for deployment.

## Deployment to Staging

When changes are pushed to the staging branch:

<img width="854" height="239" alt="image" src="https://github.com/user-attachments/assets/93aa81bd-500b-4d69-b523-b615619f75bb" />


The CI process is executed
If all tests pass, the application proceeds to the staging deployment step

This stage is used for validating features in a pre-production environment.

<img width="1584" height="274" alt="image" src="https://github.com/user-attachments/assets/759d3cf0-18a9-472b-a352-8c036de372eb" />

<img width="1201" height="794" alt="image" src="https://github.com/user-attachments/assets/90c25847-8195-4e99-8ee2-453387f6e4cd" />



##Deployment to Production

When a release is created:

The workflow is triggered automatically
After successful test execution, the application is deployed to production

This approach ensures controlled and version-based deployments.

<img width="1584" height="274" alt="image" src="https://github.com/user-attachments/assets/7bf34b7b-c086-4fe1-9c51-31d2fcea5938" />


## Workflow Configuration

The CI/CD pipeline is defined in the following file:

.github/workflows/ci-cd.yml

The workflow includes:

A build and test job
A staging deployment job triggered on the staging branch
A production deployment job triggered on release creation


## How to Trigger the Pipeline
Push code to main branch to run CI
Push code to staging branch to trigger staging deployment
Create a release to trigger production deployment

<img width="1313" height="447" alt="image" src="https://github.com/user-attachments/assets/2b1e8f64-e65d-4053-a74f-b98966419402" />


## Key Features
Automated dependency installation
Test execution using pytest
Branch-based deployment strategy
Release-based production deployment
Secure handling of sensitive information

