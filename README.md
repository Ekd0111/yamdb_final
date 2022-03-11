<<<<<<< HEAD
=======
Status of workflow

![yamdb_workflow](https://github.com/Ekd0111/yamdb_final/yamdb_workflow.yml/badge.svg)

>>>>>>> b3bb3710b3b47a0e26ac666bebef85d1424cc725
# Учебный проект YAMDB_FINAL
## Описание
Этот проект может многое. Главная цель которого - закрепление практических навыков DevOps: CI и CD.
## Технологии
Python 3.7
Django 2.2.19
Docker 20.10.12

## Как запустить проект:

### Клонировать репозиторий и перейти в папку infra проекта в командной строке:

```git clone https://github.com/Ekd0111/infra_sp2.git```

```cd infra_sp2/infra/```

### Заполните файл .env по шаблону:

                                                                                                         ```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=
POSTGRES_USER=
POSTGRES_PASSWORD=
DB_HOST=db
DB_PORT=5432
```

### Запустите контейнеры в фоновом режиме:

```docker-compose up -d```

### Выполните миграции в контейнере, создайте суперпользователя, соберите статику:

```docker-compose exec web python manage.py migrate```
```docker-compose exec web python manage.py createsuperuser```
```docker-compose exec web python manage.py collectstatic --no-input```

### Заполните базу данными:

```python manage.py loaddata fixtures.json```

### Проверьте работоспособность приложения:

- зайдите на http://localhost/admin/ и убедитесь, что страница отображается полностью: статика подгрузилась;
- авторизуйтесь под аккаунтом суперпользователя и убедитесь, что миграции прошли успешно;
- протестируйте приложение, например, через Postman.
### Авторы:
ЯП и Кольцова Екатерина
