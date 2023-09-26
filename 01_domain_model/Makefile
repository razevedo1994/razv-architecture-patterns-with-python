.PHONY: install virtualenv lint fmt test clean

install:
	@echo "Installing for dev environment"
	@.venv/bin/python -m pip install -r requirements.txt

virtualenv:
	@echo "Creating virtual environment"
	@python3 -m venv .venv

lint:
	@.venv/bin/pflake8 test_model.py model.py

fmt:
	@.venv/bin/isort test_model.py model.py
	@.venv/bin/black --line-length 79 test_* model.py

test:
	@.venv/bin/pytest -v