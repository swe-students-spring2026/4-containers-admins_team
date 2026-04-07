Date: April 7, 2026 (Tuesday)

Machine Learning Client - Repository Notes

This folder is part of the "Containerized App Exercise" repository.
The full repository includes:
- machine-learning-client/  -> Python machine learning subsystem
- web-app/                  -> Python Flask web app subsystem
- .github/workflows/        -> CI automation and workflows
- instructions.md           -> assignment requirements and rubric

Current status:
- Repository scaffold and CI workflows are set up.
- Application feature code is expected to be added in subsystem folders.

Development prerequisites:
- Python 3.10
- Pipenv
- Docker (for MongoDB and containerized runs)

Typical setup from repository root:
1) cd machine-learning-client
2) pipenv sync --dev

Quality checks for this subsystem:
- pipenv run pylint **/*.py
- pipenv run black --diff --check .

Notes:
- Keep implementation for ML-related logic in this folder.
- Refer to root README.md and instructions.md for full project context.