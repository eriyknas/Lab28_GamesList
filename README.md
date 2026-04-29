# Лабораторная работа №28. Веб-сервер на C#: список любимых игр с полным управлением
Веб-API на ASP.NET Core для управления списком любимых игр. 
## Инструкция по запуску
`dotnet run`
## Таблица всех маршрутов
Метод|Маршрут|Описание|Статус
----|----|----|----
GET| /api/games |Получить все игры |200
GET| /api/games/{id} |Получить игру по id |200/404
POST |/api/games| Добавить игру |201
DELETE |/api/games/{id}| Удалить игру |204/404
## Примеры curl-команд для каждого маршрута
GET - Получить все игры
```bash
curl http://localhost:5000/api/games
```
GET - Получить игру по id
```bash
curl http://localhost:5000/api/games/1
```
POST - Добавить игру
```bash
curl -X POST http://localhost:5000/api/games \
  -H "Content-Type: application/json" \
  -d "{\"title\": \"Minecraft\", \"genre\": \"Adventure\", \"releaseYear\": 2017, \"isFavourite\": true}"
```
DELETE - Удалить игру
```bash
curl -X DELETE http://localhost:5000/api/games/1
```