help:
	@echo make '[ setup | run | install | run ]'

setup:
	sudo apt update
	sudo apt install gcc libssl-dev mysql-server libmysqlclient-dev python virtualenv python-dev

install:
	virtualenv venv
	venv/bin/pip install -r requirements.txt

run:
	venv/bin/gunicorn -c gunicorn_config.py -w 10 app:app --access-logfile -

