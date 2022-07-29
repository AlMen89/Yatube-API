### Описание

В проекте продемонстрирован функционал API для социальной сети блогеров YaTube


### Установка

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/AlMen89/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

### Примеры

Получение JWT-токена:

```
POST http://127.0.0.1:8000/api/v1/jwt/create/

JSON:
{

    "username": "string",
    "password": "string"

}
```

Получение публикаций:

```
GET http://127.0.0.1:8000/api/v1/posts/
```

Создание публикации:

```
POST http://127.0.0.1:8000/api/v1/posts/

JSON:
{
  "text": "string",
  "image": "string",
  "group": 0
}

Использовать полученный ранее JWT-токен
```

### Использованные технологии
Django
REST Framework
Djoser
GIT