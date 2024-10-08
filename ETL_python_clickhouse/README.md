# Анализ данных из ClickHouse с использованием Pandahouse

## Описание проекта

В этом проекте используется библиотека `pandahouse` для выгрузки данных из базы данных ClickHouse и анализа полученных данных в Python. Датасет `ldn_listings` содержит информацию об объявлениях на Airbnb в Лондоне 🇬🇧: включает в себя полные описания жилья, характеристики и средние оценки в отзывах. 

## Используемые Инструменты и Библиотеки

<p>
  <kbd>Python</kbd>
  <kbd>Pandas</kbd>
  <kbd>Pandahouse</kbd>
  <kbd>ClickHouse</kbd>
  <kbd>Matplotlib</kbd>
  <kbd>NumPy</kbd>
  <kbd>Seaborn</kbd>
</p>

## Задачи

1. Проверка корректности подключения к базе данных ClickHouse.
2. Определение 75-го перцентиля цены для типа жилья `Private room`.
3. Расчет средней цены и рейтинга по типам жилья, визуализация зависимости между ценой и рейтингом.
4. Подсчет способов верификации аккаунтов для пользователей, предлагающих впечатления.
5. Анализ распределения объявлений с впечатлениями по районам, визуализация в виде тепловой карты.
6. Анализ распределения цен по типам жилья с предложенными впечатлениями, построение графиков распределений.
7. Извлечение данных о ценах и датах первого отзыва начиная с 2 января 2010 года.
8. Построение графика динамики средних цен по типу комнаты по годам.

## Датасет

Датасет `ldn_listings` содержит информацию о жилье на Airbnb в Лондоне. **Основные** столбцы включают:
- `price` – цена за ночь
- `room_type` – тип сдаваемого жилья
- `host_id` – идентификатор хозяина
- `host_verifications` – способы верификации хозяина
- `experiences_offered` – тип предлагаемых впечатлений
- `neighborhood` – район
- `review_scores_rating` – рейтинг
- `date_of_first_review` – дата первого отзыва

## Подключение к ClickHouse

```python
import pandahouse as ph

connection = {
    'host': 'http://your-clickhouse-server',
    'database': 'default',
    'user': 'default',
    'password': ''
}
```

## Основные выводы

- Наибольшие колебания в цене наблюдаются у целых домов/квартир, особенно в последние годы.
- Гостиничные номера показывают устойчивый рост цен, что может свидетельствовать о повышении качества услуг или увеличении спроса.
- Частные комнаты остаются наиболее стабильным вариантом по цене.
- Общие комнаты либо не были популярны, либо данные по ним неполные.
