# alx_travel_app_0x00 — duplicated project for exercises

This folder is a duplicate of the original project, adapted to be runnable locally with minimal configuration.

Quick start (PowerShell)

1. Create and activate a virtual env:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies (from the root repo `requirement.txt` or create one):

```powershell
python -m pip install --upgrade pip
python -m pip install -r ..\requirement.txt
```

3. Run migrations and seed the DB:

```powershell
python manage.py migrate
python manage.py seed
```

This will create two users (`host1`, `guest1`) and a few sample listings.
