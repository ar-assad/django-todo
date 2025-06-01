# 📝 Django Todo App

A simple Django-based Todo application.

---

## ⚙️ Requirements (for local setup)

* Python 3.8+
* pip
* virtualenv (recommended)

---

## 🚀 Running the App Locally (Without Docker)

### 1. Clone the Repository

```bash
git clone https://github.com/ar-assad/django-todo.git 
cd django-todo
```

### 2. Create and Activate a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install django
```

### 4. Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Run the Server

```bash
python manage.py runserver
```

Open your browser and go to:
[http://127.0.0.1:8000](http://127.0.0.1:8000)

---

## 🐳 Running with Docker

### 1. Make Sure Docker is Installed

[Install Docker](https://docs.docker.com/get-docker/) if you haven't already.

### 2. Build the Docker Image

From the root of the project (where the Dockerfile is):

```bash
docker build -t django-todo .
```

### 3. Run the Docker Container

```bash
docker run -p 8000:8000 django-todo
```

Access the app at:
[http://localhost:8000](http://localhost:8000)

---

## ⚠️ Common Issues

### “DisallowedHost” Error

If you're running the app on a server (e.g. EC2), make sure to add the host/IP to `ALLOWED_HOSTS` in `settings.py`:

```python
ALLOWED_HOSTS = ['<your-ip-address>']  # or ['*'] for development only
```

---

## ✅ Tips for Development

* To make changes reflect inside the Docker container, consider using Docker volumes or rebuild the image.
* Use `.env` files for managing secret keys or settings in production.
