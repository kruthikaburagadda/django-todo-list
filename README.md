# To-Do List Application

A simple web-based task management application built with **Python** and the **Django** web framework.

## Features

- Add new tasks with a title and description
- View all tasks
- Mark tasks as completed
- Delete tasks
- Persistent storage using SQLite

## Tech Stack

| Layer     | Technology |
|-----------|------------|
| Language  | Python 3.x |
| Framework | Django     |
| Database  | SQLite     |
| Frontend  | HTML, CSS  |

## Project Structure

```
django-todo-list/
├── requirements.txt
└── backend/
    ├── manage.py
    ├── db.sqlite3
    ├── backend/
    │   ├── __init__.py
    │   ├── settings.py
    │   ├── urls.py
    │   ├── asgi.py
    │   └── wsgi.py
    └── ToDo/
        ├── migrations/
        ├── templates/
        │   └── todo_list.html
        ├── __init__.py
        ├── admin.py
        ├── apps.py
        ├── models.py
        ├── urls.py
        └── views.py
```

## Setup & Run

```bash
# 1. Clone the repository
git clone git@github.com:kruthikaburagadda/django-todo-list.git
cd django-todo-list

# 2. Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run migrations
cd backend
python manage.py migrate

# 5. Start the development server
python manage.py runserver
```

Open your browser and go to: **http://localhost:8000**

## Architecture

The application follows Django's **MVT (Model-View-Template)** architecture:

- **Model** — defines the `Todo` table (title, description, completed)
- **View** — handles add, list, complete, and delete operations
- **Template** — renders the UI using HTML, CSS, and Django template tags
