# My Django Project

This is a Django project for managing reservations. This project includes a simple web application that allows users to create, view, update, and delete reservations.

## Features

- User authentication (login, logout, register)
- Create, read, update, delete (CRUD) operations for reservations
- Admin interface for managing users and reservations
- Responsive design

## Requirements

- Python 3.x
- Django 3.x
- MySQL
- Virtual environment (optional but recommended)

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/my-django-project.git
    cd my-django-project
    ```

2. Create and activate a virtual environment:

    ```bash
    python -m venv env
    source env/bin/activate   # On Windows use `env\Scripts\activate`
    ```

3. Install the dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up the database:

    - Make sure MySQL is installed and running.
    - Create a MySQL database:

    ```sql
    CREATE DATABASE reservation;
    ```

    - Create a MySQL user and grant privileges:

    ```sql
    CREATE USER 'admindjango'@'localhost' IDENTIFIED BY 'employe@123!';
    GRANT ALL PRIVILEGES ON reservation.* TO 'admindjango'@'localhost';
    FLUSH PRIVILEGES;
    ```

5. Update the `settings.py` file with your database configuration:

    ```python
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.mysql',
            'NAME': 'reservation',
            'USER': 'admindjango',
            'PASSWORD': 'employe@123!',
            'HOST': 'localhost',
            'PORT': '3306',
        }
    }
    ```

6. Apply the migrations:

    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

7. Create a superuser:

    ```bash
    python manage.py createsuperuser
    ```

8. Run the development server:

    ```bash
    python manage.py runserver
    ```

9. Open your web browser and go to `http://127.0.0.1:8000` to see the application.

## Usage

- Navigate to the homepage to view the available reservations.
- Use the admin interface at `http://127.0.0.1:8000/admin` to manage users and reservations.

## Contributing

1. Fork the repository.
2. Create a new branch:

    ```bash
    git checkout -b feature-branch
    ```

3. Make your changes and commit them:

    ```bash
    git commit -m 'Add some feature'
    ```

4. Push to the branch:

    ```bash
    git push origin feature-branch
    ```

5. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Contact

If you have any questions or suggestions, please feel free to contact me at [your-email@example.com].
