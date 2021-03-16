# Django set up project with Visual Studio Code & Docker
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This repo is an example how to set up Django project with Docker in Visual Studio Code.

The tutorial for this project is on [post](https://www.samirhinojosa.com/django-docker-visual-studio-code/) in [samirhinojosa.com/blog](https://www.samirhinojosa.com/blog/).

## Files to consider
- `.devcontainer/devcontainer.json`
- `.devcontainer/docker-compose.yml`
- `.devcontainer/Dockerfile`
- `.vscode/launch.json`
- `.vscode/settings.json`

## To run the development server with Docker / Visual Studio Code

1.  Install Docker and Docker Compose
2.  With **Visual Studio Code**
    - Install Visual Studio Code
    - Install the following extensions
        - Docker
        - Remote – Containers
        - Python
    - Open the project in Visual Studio Code
3.  Create the database and database user based on `settings.py`.\
The Postgres password is `postgres` you can see it in the `docker-compose-yml`. 
    ```python
    'NAME': 'myproject_db',
    'USER': 'my_user_db',
    'PASSWORD': 'user_pwd_db',
    ```
5.  To execute the development server then run the following command
    ```python
    python manage.py runserver 
    ```
6.  Prepare the migrations based on the apps
    ```python
    python manage.py makemigrations 
    ```
7.  Make the migrations
    ```python
    python manage.py migrate 
    ```
8.  Create an admin user
    ```python
    python manage.py createsuperuser
    ```