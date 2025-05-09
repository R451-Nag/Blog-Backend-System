![image alt](https://github.com/R451-Nag/Blog-Backend-System/blob/ad2e1a9c56a3ad6824f78b07ceea786b7597aebe/Screenshot%202025-05-09%20194745.png)

# Blog-Backend-System
This is a blog backend system built using **Django** and **MySQL**. It allows users to authenticate, create blog posts, and comment on them via a fully functional RESTful API using the Django REST Framework.

---

## 🔧 Tech Stack

- 🐍 Python 3.x
- 🌐 Django
- 🔐 Django REST Framework
- 🗄️ MySQL (External Database)
- ⚙️ VS Code (Development)
- 🧪 Django Admin Panel + REST API Interface

---

## ⚙️ Features

- ✅ User authentication (login, superuser creation)
- ✅ Create, read, update, and delete blog posts (CRUD)
- ✅ Comment system on blog posts
- ✅ Browsable API using Django REST Framework
- ✅ Connected to external MySQL database

---

## Create Virtual environment
-python -m venv env
-env\Scripts\activate        # On Windows
# OR
-source env/bin/activate     # On Mac/Linux

## Install Dependencies
-pip install -r requirements.txt 

## 💾 MySQL Database Setup

I used **MySQL** as the database instead of the default SQLite.  
Although MySQL is external to VS Code, it's fully integrated with Django through the `settings.py`.

### 🛠️ MySQL Database Details:

- Database name: `blog_db`
- Tables include:
  - `blog_blogpost` — stores blog posts
  - `blog_comment` — stores comments
  - `auth_user` — stores user information
- The tables were created via Django models and migrations.
- Connect MySQL in settings.py
- DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'blog_db',
        'USER': 'your_mysql_username',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}

## Apply Migrations and create superuser
-python manage.py makemigrations
-python manage.py migrate
-python manage.py createsuperuser

---

## 🚀 How to Run the Project
-python manage.py runserver
-Visit: http://127.0.0.1:8000/api/blogs/
-Admin Panel: http://127.0.0.1:8000/admin/

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/blog-backend.git
cd blog-backend

