# Анализ Данных Клиентов

Проект анализирует данные клиентов и их операций, выявляя тенденции и предпочтения. Используются данные о пользователях и их транзакциях для определения успешных операций, предпочитаемых платформ и визуализации возрастных распределений.

## Используемые Инструменты и Библиотеки

<p>
  <kbd>Python</kbd>
  <kbd>Pandas</kbd>
  <kbd>Jupyter</kbd>
  <kbd>Matplotlib</kbd>
  <kbd>matplotlib</kbd>
  <kbd>requests</kbd>
</p>

## Описание проекта

Решены следующие задачи:
1. Импортированы библиотека `pandas` и загружены датасеты `user_data` и `logs`.
2. Проверены размер таблиц, типы переменных, наличие пропущенных значений и описательная статистика.
3. Определен клиент с наибольшим числом успешных операций (`success == True`).
4. Определена платформа с наибольшим количеством успешных операций.
5. Определена платформа, предпочитаемая премиум-клиентами.
6. Визуализировано распределение возраста клиентов в зависимости от их премиум-статуса.
7. Построен график распределения числа успешных операций.
8. Визуализировано число успешных операций на платформе `computer` в зависимости от возраста клиентов и определена возрастная группа с наибольшим числом успешных операций.


## Датасет

 `user_data`

- **client**: идентификатор пользователя
- **premium**: является ли клиент премиум
- **age**: возраст

 `logs`

- **client**: идентификатор пользователя
- **success**: результат (успех - 1, нет - 0)
- **platform**: платформа
- **time**: время в формате Unix

