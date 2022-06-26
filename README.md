
# Проект **YaMDb** 

## Описание

Проект **YaMDb** собирает любые заметки и истории пользователей по различным категориям.


## Технологии в проекте
- **Python 3.7.9**
- **Django 2.2.28**
- **Django Framework**
- **Django Rest Framework**

---

## Процедура запуска проекта (Данный проект не подойдет для запуска в dev-режиме)

1. Клонировать репозиторий и перейти в него в командной строке
``` 
git clone git@github.com:Alex1995markson/infra_sp2.git
cd infra_sp2
```

2. Если не установлен Docker, то обязательно скачать и установить. (Подробную информацию по установке можно найти на сайте [Docker] (https://www.docker.com/)). Для создания образа и контейнеров выполните следующую команду из директории где находится файл ```docker-compose.yaml```.
```
cd infra/
docker-compose up -d --build
``` 

3. Следующие команды для выполнения миграций, и добавление статики
```
docker-compose exec web python manage.py makemigrations
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py collectstatic
```
