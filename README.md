# Финальный проект спринта: CRUD для Yatube  
api_yatube  
_Спринт 13_
## Стек:
Python, Django  

## Запуск отладочного сервера:
- Склонировать репозиторий:
```commandline
git clone git@github.com:Oryshich/api-yatube.git
```
В директории с проектом
- Создание виртуального окружения:
```commandline
python -m venv venv
```
- Активация виртуального окружения:
```commandline
source venv\Scripts\activate  
```
- Обновить pip:
```commandline
python3 -m pip install --upgrade pip
```
- Установка зависимостей:
```commandline
pip install -r requirements.txt
```
- Выполнить миграции:
```
python3 yatube_api/manage.py migrate
```
- Запуск отладочного сервера:
```commandline
cd yatube_api
python manage.py runserver
```

## Задача  
В проекте api_yatube есть приложение posts с описанием моделей Yatube.
Реализовано API для всех моделей приложения (в приложении **api**).

API доступен только аутентифицированным пользователям. В проекте 
использована аутентификация по токену TokenAuthentication.

Аутентифицированный пользователь авторизован на изменение и удаление своего контента; 
в остальных случаях доступ предоставляется только для чтения. 

## Реализованы следующие эндпоинты:


```api/v1/api-token-auth/``` (POST): передаём логин и пароль, получаем токен.  
```api/v1/posts/``` (GET, POST): получаем список всех постов или создаём новый пост.  
```api/v1/posts/{post_id}/``` (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем пост с идентификатором ```{post_id}```.  
```api/v1/groups/``` (GET): получаем список всех групп.  
```api/v1/groups/{group_id}/``` (GET): получаем информацию о группе с идентификатором ```{group_id}```.  
```api/v1/posts/{post_id}/comments/```  
>(GET): получаем список всех комментариев поста с идентификатором ```{post_id}```   
>(POST): создаём новый комментарий для поста с идентификатором ```{post_id}```.   

```api/v1/posts/{post_id}/comments/{comment_id}/``` (GET, PUT, PATCH, DELETE): получаем, редактируем или удаляем комментарий с идентификатором ```{comment_id}``` в посте с id=post_id.

## 
__109__ когорта yandex-practicum [Oryshich](https://github.com/Oryshich).  
2025