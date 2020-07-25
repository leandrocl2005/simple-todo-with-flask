# TODO TASK FLASK APP

Simple todo app do tutorial do Fazt Code.

## Setup (Anaconda with Vs Code)

```bash
conda create --name flask37 python=3.6
conda activate flask37
conda install -c anaconda flask
conda install -c conda-forge flask-sqlalchemy
mkdir database
pip install pylint-flask
pip install pylint-flask-sqlalchemy
```

Editar settings.json
"python.linting.pylintArgs": ["--load-plugins", "pylint-flask", "pyling-flask-sqlalchemy"]

## Sqlite3 console commands
Cria task.db e acessa terminal sqlite3:
> sqlite3 database/tasks.db

Ver endereço do database:
> .databases

Ver todas tabelas do db
> .tables

## Python console commands
Importa *db* do *app.py*
> from app import db

Criar tabela do *model*
> db.create_all()

Sair do *python console*
> exit()

## Deploy (pythonanywhere)
- No console *bash* do pythonanywhere digite:
```bash
git clone https://github.com/leandrocl2005/simple-todo-with-flask.git
cd simple-todo-with-flask
virtualenv --python=python3.6 myvenv
source myvenv/bin/activate
pip install flask
pip install Flask-SQLAlchemy
```
- Na aba *web* escolha *add a new app*
- Escolha *Next*, *Manual configuration*, *Python 3.6*, *Next* nessa ordem
- Configure o *path* para o *Source code* como segue: /home/SEU_NICK/simple-todo-with-flask
- Configure o path para a virtualenv como segue: /home/SEU_NICK/simple-todo-with-flask/myvenv
- Configure os estáticos colocando URL /static/ e Directory /home/SEU_NICK/simple-todo-with-flask/static
- Substitua o conte ́udo do arquivo wsgi por:
```code
import sys
path = 'home/SEU_NICK/SEU_PROJETO_GIT'
if path not in sys.path:
  sys.path.append(path)
from app import app as application
```
- Salve as alterações
- Volte para aba *web*
- Clique em *reload*
- Seu website estará no ar em SEUNICK.pythonanywhere.com

## Fonte
- https://www.youtube.com/watch?v=V9VU1g4IWlg
- https://stackoverflow.com/questions/53975234/instance-of-sqlalchemy-has-no-column-member