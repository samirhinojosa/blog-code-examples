# Django hiding sensitive data with Decouple
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

How to **hide sensitive data** in **Django** with Python **Decouple** Library

For more details, you can see the original [post](https://www.samirhinojosa.com/hide-sensitive-data-in-django-with-decouple/) in [samirhinojosa.com/blog](https://www.samirhinojosa.com/blog/).

## Files to consider
- `requirements.txt`
- `.env`
- `djangohidingsensitivedata/settings.py`

## To run the development server with Docker / Visual Studio Code

1.  Install Docker and Docker Compose
2. With a **Terminal** 
    - In the project directory root, run the following command in shell
        ```docker
        docker-compose up
        ```
    - In another shell run the command below
        ```docker
        docker-compose exec web bash 
        ```
3. With **Visual Studio Code**
    - Install Visual Studio Code
    - Install the following extensions
        - Docker
        - Remote – Containers
        - Python
    - Open the project in Visual Studio Code
4.  Create the database and database user based on `settings.py`.\
In this case, consider the file `.env` as well.\
The Postgres password is `postgres` you can see it in the `docker-compose-yml`. 
    ```python
    'NAME': 'test_db',
    'USER': 'test',
    'PASSWORD': 'test',
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