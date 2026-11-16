# Автоматизация тестирования REST API (Pytest + Requests)

Проект демонстрирует навыки автоматизации тестирования бэкенда и REST API на примере открытого тестового стенда [JSONPlaceholder](https://typicode.com).

## 🛠 Технологический стек
* **Язык:** Python 3.9+
* **Фреймворк тестирования:** PyTest (фикстуры, параметризация `@pytest.mark.parametrize`)
* **HTTP-клиент:** Requests (`requests.Session`)

## 🧪 Покрытые сценарии
* `GET /posts/{id}` — получение ресурса по ID, валидация статус-кода `200 OK` и типов данных в JSON-ответе (параметризованный тест).
* `POST /posts` — создание нового ресурса, проверка статус-кода `201 Created` и корректности сохраненных полей.
* `PUT /posts/{id}` — полное обновление данных ресурса (`200 OK`).
* `DELETE /posts/{id}` — удаление ресурса (`200 OK`).
* `GET /posts/999999` — негативный сценарий: проверка корректной обработки несуществующего ресурса (`404 Not Found`).

## 🚀 Установка и запуск

```bash
git clone https://github.com
cd REST_API_tests_pytest
pip install -r requirements.txt
pytest -v
```
