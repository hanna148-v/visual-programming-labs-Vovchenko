# Документация REST API (Лабораторная работа №2)

## 1. GET /api/text
Возвращает простой текстовый ответ.

* **Запрос:** `GET http://localhost:1880/api/text`
* **Успешный ответ (200 OK):**
  ```text
  кошки

## 2. GET /api/info
Возвращает данные о студенте в формате JSON.

* **Запрос:** `GET http://localhost:1880/api/info`
* **Успешный ответ (200 OK):**
  ```text
 msg.payload = {
    student: "hanna vovchenko",
    course: "visual programming"
}

## 3. GET /api/items
Возвращает информацию о сущности по её ID с поддержкой параметров запроса[cite: 1].

* **Query параметры:** id (string) — идентификатор сущности.

* **Запрос успешный:** `GET http://localhost:1880/api/items?id=10`
* **Успешный ответ (200 OK):**
  ```text
  {
  "id": "10",
  "title": "Товар #10",
  "status": "Available"
}

* **Запрос без параметров:** `GET http://localhost:1880/api/items`
* **Успешный ответ (200 OK):**
  ```text
  {
  "error": "Bad Request: параметр 'id' обязателен"
}