# Stable Diffusion Image generating API

Stable Diffusion Image generating API is a project that enables users to generate images from an input prompt through a
simple HTTP API. It uses Stable Diffusion, a high-quality image synthesis method, to produce JPEG encoded images that
are instantly available for use or download.

A user sends an HTTP request with the image prompt as a parameter and in return receives a JPEG encoded image over the
HTTP connection. This API is currently accessible without any form of authorization or encryption, allowing trouble-free
access and usage by anyone who needs to convert text prompts into graphical representations. However, users must bear in
mind that the lack of authorization and encryption means the data sent over the API is not secure and could potentially
be intercepted.

To get started with using this project, there are a set of instructions and prerequisites for setting up your local
environment for development and testing purposes. Automated tests help ensure the robustness of the application.


## Getting Started
In order to set up the project on your system, you will need to follow these instructions.
### Step 1: Install Python 3.11
You must first ensure that you have Python 3.11 installed on your system. You can download it from the official Python website.
```shell
https://www.python.org/downloads/release/python-3110/
```
### Step 2: Create Python Virtual Environment
Next, navigate to the project root directory and create a new Python virtual environment.
```shell
cd /path/to/project/directory
python3.11 -m venv venv
```
### Step 3: Activate Python Virtual Environment
Now you should activate the Python virtual environment.
```shell
source venv/bin/activate
```
### Step 4: Install Required Packages
Then install the required packages for the project using pip.
```shell
pip install -r requirements.txt
```
Now, your development environment setup for this project is complete.

## Prerequisites
Python 3.11 or later installed on the system

## Running the tests
There are tests in the `test_main.http` file for testing the API.

### 1. Run `uvicorn`
Make sure `uvicorn` is up and running, and take note of which port it uses

### 2. Curl
use `curl` or similar tool to curl the endpoint as specified in the `test_main.http` file. The JSON at the bottom is
the body of the POST call sent to the API.