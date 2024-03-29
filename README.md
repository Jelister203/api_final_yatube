# Yatube API

### Introduction

This project represents the API for very popular website Yatube. It let's you
browse some recent posts, make some new one, delete your own posts and much-much more!

### End-points

 Получить список всех публикаций. При указании параметров limit и offset выдача должна работать с пагинацией.

* GET /api/v1/posts/

Добавление новой публикации в коллекцию публикаций. Анонимные запросы запрещены.

- POST /api/v1/posts/

Получение публикации по id.

- GET /api/v1/posts/{id}/

Обновление публикации по id. Обновить публикацию может только автор публикации. Анонимные запросы запрещены.

- PUT /api/v1/posts/{id}/

Частичное обновление публикации по id. Обновить публикацию может только автор публикации. Анонимные запросы запрещены.

- PATCH /api/v1/posts/{id}/

Удаление публикации по id. Удалить публикацию может только автор публикации. Анонимные запросы запрещены.

- DELETE /api/v1/posts/{id}/

Получение всех комментариев к публикации.

- GET /api/v1/posts/{post_id}/comments/

Добавление нового комментария к публикации. Анонимные запросы запрещены.

- POST /api/v1/posts/{post_id}/comments/

Получение комментария к публикации по id.

- GET /api/v1/posts/{post_id}/comments/{id}/

Обновление комментария к публикации по id. Обновить комментарий может только автор комментария. Анонимные запросы запрещены.

- PUT /api/v1/posts/{post_id}/comments/{id}/

Частичное обновление комментария к публикации по id. Обновить комментарий может только автор комментария. Анонимные запросы запрещены.

- PATCH /api/v1/posts/{post_id}/comments/{id}/

Удаление комментария к публикации по id. Обновить комментарий может только автор комментария. Анонимные запросы запрещены.

- DELETE /api/v1/posts/{post_id}/comments/{id}/

Получение списка доступных сообществ.

- GET /api/v1/groups/

Получение информации о сообществе по id.

- GET /api/v1/groups/{id}/

Возвращает все подписки пользователя, сделавшего запрос. Анонимные запросы запрещены. Возможен поиск по подпискам по параметру search.

- GET /api/v1/follow/

Подписка пользователя от имени которого сделан запрос на пользователя переданного в теле запроса. Анонимные запросы запрещены.

- POST /api/v1/follow/

Получить JWT-токен.

- POST /api/v1/jwt/create/

Обновить JWT-токен.

- POST /api/v1/jwt/refresh/

Проверить JWT-токен.

- POST /api/v1/jwt/verify/

### Installation

- Копировать репозиторий на локальную машину;
- Выполнить миграции;
- В директории файла manage.py выполнить команду:

```
py manage.py runserver
```