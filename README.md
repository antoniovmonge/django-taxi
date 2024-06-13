# Django REST (Caching, Logging, and Throttling)

This is a Django REST project used to apply caching, logging, and throttling aiming to follow best practices for production-ready applications.

[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)

License: MIT

## Estructure

The project follows the Django-Cookiecutter structure, with some modifications and additions to bring a better developer experience.

## Stack

- Django
- Django REST Framework
- Celery
- Redis
- PostgreSQL
- Docker
- Docker Compose

## Env Files

Environment variables for local development are included to enable easy setup for local development.

For production environments, a secret `.env` file must be created and keep it safe.

## Basic Commands

A Makefile is provided with the most common commands to run the project. This Makefile also serve as a kind of documentation for the project.

### Setup

To build the image and start the containers, run:

```bash
make up-build
```

### Create Superuser and Test User in Development Environment

```bash
make users
```

### Test  tests with pytest and coverage

To run the tests, check your test coverage, and generate an HTML coverage report:

```bash
make test
```

```bash
make coverage
```

### Email Server in DEVELOPMENT

Mailpit allow us to test the email sending in development environment without sending real emails.

Container mailpit will start automatically when you will run all docker containers in development.

With Mailpit running, to view messages that are sent by your application, open your browser and go to `http://127.0.0.1:8025`
