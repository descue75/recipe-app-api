# recipe-app-api

Create Django Project

```
docker-compose run --rm app sh -c "django-admin startproject app ."
```

Create Django App

```
docker-compose run -rm app sh -c "python manage.py startapp core"
```

Run

```
docker-compose up
```

Lint

```
docker-compose run --rm app sh -c "flake8"
```

Run Tests

```
docker-compose run --rm app sh -c "python manage.py test"
```

Make Migrations

```
docker-compose run --rm app sh -c "python manage.py makemigrations
```

Clear Migrations

```
docker volume ls
docker-compose down
docker volume rm recipe-app-api_dev-db-data
```

Run Migrations

```
docker-compose run --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"
```

Create Superuser
```
docker-compose run --rm app sh -c "python manage.py createsuperuser"
```
