# alx_travel_app — Local dev quickstart

This repository is a small Django project scaffolded for an API (Django 5.2, DRF).

Quick setup (Windows PowerShell)

1. Create and activate a venv:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install Python dependencies:

```powershell
python -m pip install --upgrade pip setuptools wheel
python -m pip install -r requirement.txt
```

3. Start RabbitMQ (Docker):

```powershell
# start RabbitMQ (management UI at http://localhost:15672)
docker compose up -d
```

4. Run migrations and start Django dev server:

```powershell
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

5. Start a Celery worker (from project root, with venv active):

```powershell
# run a Celery worker using the Django app configuration
celery -A alx_travel_app worker --loglevel=info
```

Notes
- `requirement.txt` contains project Python dependencies. RabbitMQ is a separate service (not a pip package).
- `alx_travel_app/celery.py` provides a minimal Celery app. Configure `CELERY_BROKER_URL`/`CELERY_RESULT_BACKEND` via `.env` if needed.
