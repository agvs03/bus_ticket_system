# Bus Ticket Reservation System

A Django web application for booking bus tickets. Passengers can search for trips and book seats; admins manage buses, routes, locations, schedules and bookings.

## Features
- Find scheduled trips by origin, destination and date
- Seat booking with booking history and invoices
- Admin management of buses, categories, locations and schedules
- User registration, login and profile management

## Tech stack
Python · Django 5.2 LTS · SQLite (default) or MySQL · Bootstrap templates

## Getting started
```bash
git clone git@github.com:agvs03/bus_ticket_system.git
cd bus_ticket_system/bus_ticket_system
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
DJANGO_DEBUG=True python manage.py runserver        # Windows: set DJANGO_DEBUG=True && python manage.py runserver
```
Open http://127.0.0.1:8000.

## Configuration
All secrets come from environment variables — see [`.env.example`](bus_ticket_system/.env.example).

| Variable | Default | Purpose |
|---|---|---|
| `DJANGO_SECRET_KEY` | insecure dev key | Set a strong value in production |
| `DJANGO_DEBUG` | `False` | Enable debug mode locally |
| `DJANGO_ALLOWED_HOSTS` | `localhost,127.0.0.1` | Comma-separated host list |
| `DB_ENGINE` | `sqlite` | Set to `mysql` to use the `DB_*` variables |

## Project structure
```
bus_ticket_system/
  btrs_django/        # Project settings & URLs
  reservationApp/     # Models, views, forms, templates
  manage.py
```
