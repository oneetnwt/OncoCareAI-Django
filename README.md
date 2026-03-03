# OncoCare

A web-based oncology care management system built with Django, designed to support healthcare professionals in managing cancer patient data, treatment workflows, and clinical records.

---

## Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Development Server](#running-the-development-server)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

OncoCare is a Django-based healthcare information system focused on oncology. It aims to streamline the management of patient records, treatment plans, appointments, and clinical data for oncology departments and cancer care facilities.

---

## Tech Stack

| Layer       | Technology         |
|-------------|--------------------|
| Backend     | Python / Django 5.2 |
| Database    | SQLite (development) |
| Frontend    | Django Templates   |
| Server      | WSGI (Django dev server) |

---

## Getting Started

### Prerequisites

- Python 3.10+
- pip
- (Optional) virtualenv or venv

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/OncoCareDj.git
   cd OncoCareDj
   ```

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply migrations:**

   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (admin account):**

   ```bash
   python manage.py createsuperuser
   ```

### Running the Development Server

```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`.  
The admin panel is accessible at `http://127.0.0.1:8000/admin/`.

---

## Project Structure

```
OncoCareDj/
├── config/               # Project configuration
│   ├── settings.py       # Django settings
│   ├── urls.py           # Root URL configuration
│   ├── asgi.py           # ASGI entry point
│   └── wsgi.py           # WSGI entry point
├── manage.py             # Django management CLI
└── db.sqlite3            # SQLite database (auto-generated)
```

---

## Configuration

Key settings are managed in [config/settings.py](config/settings.py).

| Setting        | Default              | Description                          |
|----------------|----------------------|--------------------------------------|
| `DEBUG`        | `True`               | Enable/disable debug mode            |
| `DATABASES`    | SQLite               | Database backend configuration       |
| `ALLOWED_HOSTS`| `[]`                 | Allowed hostnames for production     |
| `TIME_ZONE`    | `UTC`                | Server timezone                      |

> **Note:** Before deploying to production, set `DEBUG = False`, configure `ALLOWED_HOSTS`, replace the `SECRET_KEY`, and switch to a production-grade database (e.g., PostgreSQL).

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
