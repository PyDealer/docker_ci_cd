[![Main Kittygram workflow](https://github.com/PyDealer/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/PyDealer/kittygram_final/actions/workflows/main.yml)
#  Как работать с репозиторием финального задания

## Что такое kyttigram

Киттиграм - это инстаграм для ваших кошечек, и не только. Можно постить фотки, выбирать их цвет, указывать год рождения и имя любимого питомца.

## Стек:
Python, django, DRF, docker, nginx, gunicorn, js, react, html, css

## Что нужно сделать

touch .env

Переменные env:
POSTGRES_USER=<br>
POSTGRES_PASSWORD=<br>
POSTGRES_DB=<br>
DB_HOST=<br>
DB_PORT=<br>
SECRET_KEY= #django_secret_key<br>
DEV='dev'<br>
ALLOWED_HOSTS=<br>
<br>
docker-compose -f docker-compose.production.yml up --build<br>

## Автор:
PyDealer

## Как проверить работу с помощью автотестов

В корне репозитория создайте файл tests.yml со следующим содержимым:
```yaml
repo_owner: ваш_логин_на_гитхабе
kittygram_domain: полная ссылка (https://доменное_имя) на ваш проект Kittygram
taski_domain: полная ссылка (https://доменное_имя) на ваш проект Taski
dockerhub_username: ваш_логин_на_докерхабе
```

Скопируйте содержимое файла `.github/workflows/main.yml` в файл `kittygram_workflow.yml` в корневой директории проекта.

Для локального запуска тестов создайте виртуальное окружение, установите в него зависимости из backend/requirements.txt и запустите в корневой директории проекта `pytest`.

## Чек-лист для проверки перед отправкой задания

- Проект Taski доступен по доменному имени, указанному в `tests.yml`.
- Проект Kittygram доступен по доменному имени, указанному в `tests.yml`.
- Пуш в ветку main запускает тестирование и деплой Kittygram, а после успешного деплоя вам приходит сообщение в телеграм.
- В корне проекта есть файл `kittygram_workflow.yml`.
