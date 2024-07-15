# Fyle Backend Challenge

# Completed Tasks

- [x] [PRINCIPAL]List submitted and graded assignments API
- [x] [PRINCIPAL]List all teachers API
- [x] [PRINCIPAL]Grade an assignment/Re-grade an assignment API
- [x] [TEACHER]Wrote tests for Grading API
- [x] Fixed all bugs in the code and made sure all tests pass
- [x] Test Coverage is at 94%(covering all important parts of the code)
- [x] Wrote SQL queries for the test cases provided
- [x] Dockerized the application(Docker + Docker Compose)
- [x] Added documentation for building and running the application with Docker

## Installation

1. Fork this repository to your github account
2. Clone the forked repository and proceed with steps mentioned below

### Install requirements

```
virtualenv env --python=python3.8
source env/bin/activate
pip install -r requirements.txt
```
### Reset DB

```
export FLASK_APP=core/server.py
rm core/store.sqlite3
flask db upgrade -d core/migrations/
```
### Start Server

```
bash run.sh
```

This will start app on localhost:7755

### Start Server using Docker

```
# Build the docker image
docker build -t flask-gunicorn-app .

# Run the docker container
docker run -d -p 7755:7755 flask-gunicorn-app

# Optionally, you can use docker compose
docker compose up
```

This will start app on localhost:7755

### Run Tests

```
pytest -vvv -s tests/

# for test coverage report
# pytest --cov
# open htmlcov/index.html
```
