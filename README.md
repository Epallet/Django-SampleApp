## Epallet Sample Project
This README outlines the details on building and running the Epallet Sample Django application using Docker.

## Prerequisites
Before proceeding, ensure you have the following installed on your system:

Docker
Git (for cloning the repository, if necessary)

## Getting Started
These instructions will get your copy of the Epallet Sample Project up and running on your local machine for development and testing purposes.

## Cloning the Repository
If you haven't already, clone the project repository to your local machine:


Copy code
git clone [URL to Repository]
cd epallet_sample_project


## Building the Docker Image
Navigate to the root directory of the project (where the Dockerfile is located) and run:


docker build -t epallet-sample-app .
This command builds the Docker image of the application, tagging it as epallet-sample-app.

## Running the Application
To start the application, run:


docker run -p 8000:8000 epallet-sample-app
This command runs the Docker container, mapping port 8000 of the container to port 8000 on the host machine.

# Accessing the Application
Once the server is running, you can access the application by visiting http://127.0.0.1:8000/sample/ in your web browser.

## Additional Commands
Django Admin Access
To access Django's admin panel:

Ensure the Docker container is running.

Create a superuser (if not already created):


docker exec -it [CONTAINER_ID] python epallet_sample_project/manage.py createsuperuser
Follow the prompts to create a superuser. You can find the [CONTAINER_ID] by running docker ps.

Visit http://127.0.0.1:8000/admin/ and log in with the superuser credentials.

## Notes
The provided Dockerfile and commands are intended for development and testing purposes. For a production environment, additional configurations may be necessary.
Modify the requirements.txt file as needed to include any new dependencies.
Customization:





