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
