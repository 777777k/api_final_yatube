#  «API для Yatube»
API и документация для приложения Yatube

## Стек технологий:
- Python
- Djando
- DRF
***
### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/xyz.git
```

```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:

```
python -m venv env
```
Для Unix и MacOS:
```
source env/bin/activate
```
Для Windows:
```
source env/Scripts/activate
```
Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
Выполнить миграции:

```
python manage.py migrate
```
Запустить проект:

```
python manage.py runserver
```
***
### Примеры
Для доступа к API необходимо получить токен:

Нужно выполнить POST-запрос localhost:8000/api/v1/token/ передав поля username и password. API вернет JWT-токен

Далее, передав токен можно будет обращаться к методам, например:

/api/v1/posts/ (GET, POST, PUT, PATCH, DELETE)

При отправке запроса передавайте токен в заголовке Authorization: Bearer <токен>
***
#### Более подробное описание API можно получить по адресу:
http://localhost:8000/redoc/
***