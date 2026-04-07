**Last updated:** 2026-04-07 07:38:24 PM EDT

[![Lint-free](https://github.com/swe-students-spring2026/4-containers-admins_team/actions/workflows/lint.yml/badge.svg)](https://github.com/swe-students-spring2026/4-containers-admins_team/actions/workflows/lint.yml)
[![GitHub events logger](https://github.com/swe-students-spring2026/4-containers-admins_team/actions/workflows/event-logger.yml/badge.svg)](https://github.com/swe-students-spring2026/4-containers-admins_team/actions/workflows/event-logger.yml)

# Containerized App Exercise

This repository contains a multi-container project scaffold with a machine learning client, a web app, and a MongoDB database.

The repository currently includes project structure, CI workflows, and Python lint/format tooling. Application feature code can be added in the subsystem folders below.

## Repository Layout

- `machine-learning-client/` - Python machine learning subsystem
- `web-app/` - Python Flask web app subsystem
- `.github/workflows/` - CI automation and repository workflows
- `instructions.md` - full assignment requirements and rubric

## Team

- [bloombar](https://github.com/bloombar)

> Add all teammate names here as GitHub profile links.

## Prerequisites

- Python 3.10
- [Pipenv](https://pipenv.pypa.io/en/latest/)
- [Docker](https://www.docker.com/) (for MongoDB and containerized runs)

## Setup

Install dependencies for each subsystem:

```bash
cd machine-learning-client
pipenv sync --dev

cd ../web-app
pipenv sync --dev
```

## Run Quality Checks

Run linting and formatting checks in each subsystem:

```bash
cd machine-learning-client
pipenv run pylint **/*.py
pipenv run black --diff --check .

cd ../web-app
pipenv run pylint **/*.py
pipenv run black --diff --check .
```

## Database (MongoDB) for local development

Start MongoDB in Docker:

```bash
docker run --name mongodb -d -p 27017:27017 mongo
```

Stop and restart as needed:

```bash
docker stop mongodb
docker start mongodb
```

## Environment Variables

No required `.env` variables are currently defined in this repository.

If you introduce environment variables later:

1. Create example files (for example, `web-app/.env.example` and `machine-learning-client/.env.example`) with dummy values.
2. Keep real `.env` files out of version control.
3. Document each variable and expected value format in this README.

## Notes

- Follow the full project requirements in `instructions.md`.
- Add Dockerfiles and a `docker-compose.yml` once subsystem runtime code is in place.
