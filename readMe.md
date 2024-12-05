# Django To-Do List Application Documentation

## Introduction
This document provides a comprehensive guide for the Django-based To-Do List application developed as part of the coding assignment. The application allows users to create, view, update, and delete tasks in a simple and intuitive manner.

## Features
The Django To-Do List application offers the following features:

1. **Task Management**: Users can create, read, update, and delete tasks. Each task can have a title, description, due date, tags, and a status.
2. **Task Status**: The application supports the following task statuses: OPEN, WORKING, PENDING REVIEW, COMPLETED, OVERDUE, and CANCELLED.
3. **Timestamp**: Each task is automatically assigned a creation timestamp that cannot be modified by the user.
4. **Django Admin Interface**: The application includes a Django Admin interface that allows administrators to manage all aspects of the application, including the tasks and their related data.
5. **REST API**: The application provides a set of RESTful APIs for interacting with the to-do list programmatically, including creating, reading, updating, and deleting tasks.
6. **Authentication**: The application uses basic authentication for the REST APIs.
7. **Testing**: The application includes comprehensive unit, integration, and end-to-end (E2E) tests to ensure the reliability and correctness of the codebase.
8. **Continuous Integration and Deployment**: The application uses GitHub Actions for running tests and deploying the application to the cloud.

## Installation and Setup

### Prerequisites
- Python 3.11 or higher
- Django 4.2.7 or higher
- Django REST Framework 3.14.0 or higher

### Installation Steps
1. Clone the repository containing the Django To-Do List application code.
2. Create a new Python virtual environment and activate it.
3. Install the required dependencies by running `pip install -r requirements.txt`.
4. Apply the database migrations by running `python manage.py migrate`.
5. Create a superuser account by running `python manage.py createsuperuser`.
6. Start the development server by running `python manage.py runserver`.

The application should now be accessible at `http://127.0.0.1:8000/`.

## REST API Documentation

The Django To-Do List application provides the following REST APIs:

1. **Create a Todo Item**
   - **URL**: `/api/todos/`
   - **Method**: `POST`
   - **Authentication**: Basic Authentication
   - **Request Body**:
     ```json
     {
       "title": "Buy groceries",
       "description": "Pick up milk, eggs, and bread",
       "due_date": "2023-12-31",
       "tags": ["shopping", "errands"],
       "status": "OPEN"
     }
     ```
   - **Response**: The created todo item in JSON format.

2. **Read a Todo Item**
   - **URL**: `/api/todos/{id}/`
   - **Method**: `GET`
   - **Authentication**: Basic Authentication
   - **Response**: The requested todo item in JSON format.

3. **Read All Todo Items**
   - **URL**: `/api/todos/`
   - **Method**: `GET`
   - **Authentication**: Basic Authentication
   - **Response**: A list of all todo items in JSON format.

4. **Update a Todo Item**
   - **URL**: `/api/todos/{id}/`
   - **Method**: `PUT`
   - **Authentication**: Basic Authentication
   - **Request Body**:
     ```json
     {
       "title": "Buy groceries and cleaning supplies",
       "description": "Pick up milk, eggs, bread, and cleaning products",
       "due_date": "2023-12-31",
       "tags": ["shopping", "errands", "cleaning"],
       "status": "WORKING"
     }
     ```
   - **Response**: The updated todo item in JSON format.

5. **Delete a Todo Item**
   - **URL**: `/api/todos/{id}/`
   - **Method**: `DELETE`
   - **Authentication**: Basic Authentication
   - **Response**: HTTP status code 204 (No Content).

To test the APIs, you can use the provided Postman collection, which includes examples for each of the above endpoints.

## Testing

The Django To-Do List application includes comprehensive tests to ensure the reliability and correctness of the codebase. The tests are divided into the following categories:

1. **Unit Tests**: 100% code coverage for the application's models, views, and serializers.
2. **Integration Tests**: 100% code coverage for the application's REST API endpoints.
3. **End-to-End (E2E) Tests**: Tests for the following scenarios:
   - Create a todo item
   - View all todo items
   - Update a todo item
   - Delete a todo item

Tests are automatically triggered using GitHub Action on every commit.

The test results, including the coverage reports, can be found in the project's Git repository.

## Continuous Integration and Deployment

The Django To-Do List application uses GitHub Actions for Continuous Integration (CI) and Deployment (CD) operations. The following GitHub Actions are set up for the project:

1. **Run Tests**: Automatically run the unit, integration, and E2E tests on every commit push.
2. **Run Linting Tools**: Automatically run Flake8 and Black linting tools on every commit push.

The application is deployed to Render upon successful completion of the GitHub Actions workflows.



The documentation covers the following topics:

- Application Overview
- Installation and Setup
- REST API Documentation
- Testing Procedures
- Continuous Integration and Deployment

## Django Admin Credentials

The Django admin superuser credentials for the hosted application are:

- Username: `todo`
- Password: `todo2002`



## Conclusion

The Django To-Do List application provides a simple and effective way to manage your tasks. With its comprehensive set of features, including a user-friendly Django Admin interface, RESTful APIs, and thorough testing, the application is a reliable and scalable solution for your task management needs.

If you have any questions or encounter any issues, please feel free to reach out to the development team at the email addresses provided in the coding assignment.