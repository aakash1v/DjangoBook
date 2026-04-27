# Project variables
PROJECT_NAME = myproject
PYTHON = python3
MANAGE = $(PYTHON) manage.py

# Default target
.DEFAULT_GOAL := help

# ----------------------
# 📌 Help
# ----------------------
help:
	@echo "Available commands:"
	@echo " make run          - Run development server"
	@echo " make migrate      - Apply migrations"
	@echo " make makemigrations - Create migrations"
	@echo " make superuser    - Create superuser"
	@echo " make shell        - Open Django shell"
	@echo " make test         - Run tests"
	@echo " make collectstatic - Collect static files"
	@echo " make lint         - Run linting (flake8)"
	@echo " make format       - Format code (black)"
	@echo " make clean        - Remove cache files"

# ----------------------
# 🚀 Core Commands
# ----------------------
run:
	$(MANAGE) runserver

migrate:
	$(MANAGE) migrate

makemigrations:
	$(MANAGE) makemigrations

superuser:
	$(MANAGE) createsuperuser

shell:
	$(MANAGE) shell

test:
	$(MANAGE) test

collectstatic:
	$(MANAGE) collectstatic --noinput

# ----------------------
# 🧹 Code Quality
# ----------------------
lint:
	flake8 .

format:
	black .

# ----------------------
# 🧼 Cleanup
# ----------------------
clean:
	find . -name "*.pyc" -delete
	find . -name "__pycache__" -delete
