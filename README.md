# Taski

### Описание
Это инструмент для планирования задач, иначе говоря «трекер». Приложение, где вы сможете составлять список задач и отмечать выполненные.

Технологии:
- Python
- Django
- Django REST Framework
- Simple JWT
- PostgreSQL

### Запуск проекта
Клонировать репозиторий и перейти в него в командной строке:
```
git clone [https://github.com/Anastasia7Si/kittygram_final](https://github.com/Anastasia7Si/taski-docker)
cd taski-docker
```
В корне проекта создать файл .env и прописать в него свои данные.
Пример:
```
POSTGRES_DB=taski
POSTGRES_USER=taski_user
POSTGRES_PASSWORD=taski_password
```
Запустить проект через docker-compose:
```
docker compose -f docker-compose.yml up
```
Выполнить миграции:
```
docker compose -f docker-compose.yml exec backend python manage.py migrate
```
Собрать статику и скопировать ее:
```
docker compose -f docker-compose.yml exec backend python manage.py collectstatic
docker compose -f docker-compose.yml exec backend cp -r /app/static_backend/. /backend_static/static/
```
### Автор
```
- Пушкарная Анастасия
````
