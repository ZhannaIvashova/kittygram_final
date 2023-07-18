#  Проект Kittygram
**Kittygram — социальная сеть для обмена фотографиями любимых питомцев.**
## Описание
*Этот проект даст пользователям возможность создать учетную запись, публиковать личные посты, подписываться на любимых авторов и оставлять комментарии.*
## Технологии
Python 3.9
Django 3.2.3
DjangoRestFramework 3.12.4
PostgreSQL
Nginx
Node.js
Docker
CI/CD
## Ссылки на развернутые приложения
- https://kittygramproj.hopto.org/
- https://taskiiii.hopto.org/
### Запуск проекта через docker-compose
- Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:ZhannaIvashova/kittygram_final.git
cd kittygram_final
```
- В корне проекта создать файл .env
```
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
```
- Запустить проект
```
docker compose up
``` 
- Выполнить миграции и собрать статику:
```
docker compose exec backend python manage.py migrate
docker compose exec backend python manage.py collectstatic
docker compose exec backend cp -r /app/collected_static/. /backend_static/static/
```
### Обратная связь
IvashovaHome@yandex.ru
