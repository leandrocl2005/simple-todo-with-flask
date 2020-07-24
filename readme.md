# TODO TASK FLASK APP

Simple todo app from Fazt Code tutorial.

## Setup (Anaconda with Vs Code)

```bash
conda create --name flask37 python=3.7
conda activate flask37
conda install -c anaconda flask
conda install -c conda-forge flask-sqlalchemy
mkdir database
pip install pylint-flask
pip install pylint-flask-sqlalchemy
```

Edit in settings.json
"python.linting.pylintArgs": ["--load-plugins", "pylint-flask", "pyling-flask-sqlalchemy"]

## Sqlite3 console commands
Create task.db and access sqlite3 terminal:
> sqlite3 database/tasks.db

See database location:
> .databases

See all tables in db
> .tables

## Python console commands
Import db from app.py
> from app import db

Create table from model
> db.create_all()

Exit from python console
> exit()

## Fonte
- https://www.youtube.com/watch?v=V9VU1g4IWlg
- https://stackoverflow.com/questions/53975234/instance-of-sqlalchemy-has-no-column-member