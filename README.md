### Описание проекта:
Yatube -приложение блог с возможностью регистрации пользователей, создания групп, постов и подписок
Проект api_final_yatube представляет собой набор эндпоинтов приложения yatube для связи с фронтендом. 

### Как пользоваться проектом:

Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:Vlaldis95/api_final_yatube.git
```
перейти в директорию проекта на вашем компьютере: 
```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение (команды для OS Windows):

```
python3 -m venv venv
```
```
source venv/Scripts/activate
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

### Примеры эндпоинтов:

Общий локальный хост: http://127.0.0.1:8000/

эндпоинты для аунтентификации: /auth/users/ 
POST-запрос с введенными username и password зарегистрирует пользователя

api/v1/jwt/create/ 
POST-запрос с введенными username и password даст токен, который нужен для авторизации 

http://127.0.0.1:8000/api/v1/posts/

GET-запрос: 
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}

http://127.0.0.1:8000/api/v1/posts/
POST-запрос 
{
  "text": "string",
  "image": "string",
  "group": 0
}