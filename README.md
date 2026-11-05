# Newspaper App

A Django-based newspaper application where users can create accounts, publish articles, read posts, and interact through comments. The project demonstrates Django's authentication system, custom user models, class-based views, model relationships, and access control.

## Features

- **Custom User Model:** Extends Django's `AbstractUser` with an additional age field.
- **User Authentication:** User registration, login, logout, password change, and password reset using Django's built-in authentication views.
- **Article Management:** Authenticated users can create, view, update, and delete articles.
- **Author-Based Access Control:** Only the author of an article can edit or delete it.
- **Comment System:** Users can add comments to articles.
- **Django Admin Integration:** Manage users, articles, and comments through the Django administration panel.
- **Responsive UI:** Uses Bootstrap-based styling and Django Crispy Forms.
- **Automated Tests:** Includes tests for custom user creation and the signup workflow.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| Django 5.2 | Backend web framework |
| SQLite | Database |
| HTML | Template structure |
| Bootstrap | UI styling |
| Django Crispy Forms | Form rendering |
| Git & GitHub | Version control |

## Project Structure

```text
newspaper/
│
├── accounts/
│   ├── migrations/
│   ├── admin.py
│   ├── forms.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
│
├── articles/
│   ├── migrations/
│   ├── admin.py
│   ├── forms.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
│
├── pages/
│   ├── views.py
│   └── urls.py
│
├── templates/
│   ├── registration/
│   │   └── signup.html
│   ├── base.html
│   ├── home.html
│   └── article_list.html
│
├── django_project/
│   ├── settings.py
│   └── urls.py
│
├── manage.py
└── requirements.txt
```

## Getting Started

Follow these instructions to run the project locally.

### 1. Clone the repository

```bash
git clone https://github.com/Muzahidin735/news.git
cd news
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

**Windows:**
```bash
.venv\Scripts\activate
```

**Linux / macOS:**
```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply database migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create a superuser

```bash
python manage.py createsuperuser
```

### 6. Run the development server

```bash
python manage.py runserver
```

Open the application at:

```text
http://127.0.0.1:8000/
```

Access the Django administration panel at:

```text
http://127.0.0.1:8000/admin/
```

## Application URLs

| URL | Description |
|---|---|
| `/` | Homepage |
| `/accounts/signup/` | User registration |
| `/accounts/login/` | User login |
| `/accounts/logout/` | User logout |
| `/accounts/password_change/` | Change password |
| `/articles/` | View articles |
| `/articles/new/` | Create an article |
| `/admin/` | Django administration |

*The password-related URLs use Django's built-in authentication routes. Article detail, edit, and delete URLs are generated using their respective named URL patterns.*

## Testing

Run the project's automated tests using:

```bash
python manage.py test
```

The accounts application includes tests covering:

- Custom user creation.
- Superuser creation.
- Signup page accessibility.
- Successful user registration.

## Key Django Concepts Practiced

Through this project, I explored and implemented:

- Custom user models using `AbstractUser`.
- Custom user creation and change forms.
- Django authentication and authorization.
- Class-based views and generic views.
- Model relationships using `ForeignKey`.
- Django ModelForms.
- `LoginRequiredMixin` and `UserPassesTestMixin`.
- Django URL routing and template inheritance.
- Django admin customization.
- Automated testing.

## Future Improvements

- Implement email verification during registration.
- Add article search and filtering.
- Add pagination for article listings.
- Improve the commenting experience.
- Add user profile management.
- Introduce a production-ready deployment configuration.
