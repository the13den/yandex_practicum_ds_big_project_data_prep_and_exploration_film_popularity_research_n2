# О работе "Большой проект по предобработке и исследовательскому анализу данных. Выяснение того как господдержка влияет на кассовые сборы и рейтинг фильма"

Данный проект содержал меня подробное ТЗ. Я предобработал данные на Pandas. Используя графики и таблицы, корелляцию Пирсона выяснил как господдержка влияет на популярность фильма. Сложность проекта заключалась в обилии строковых столбцов, которые пришлось очищать. Большая часть визуализаций в проекте выполнена с помощью Plotly

Технологии: Python, Pandas, matplotlib, plotly

# ТЗ

Теперь самое время проверить знания и решить аналитический кейс. Выполнять работу вы будете самостоятельно.

Когда закончите, отправьте работу на проверку ревьюеру. В течение суток вы получите комментарии, которые нужно учесть: доработать проект и вернуть ревьюеру обновлённый вариант. Возможно, вы будете дорабатывать кейс по комментариям несколько раз. Не переживайте, это нормально.

**Проект завершён, когда одобрены все доработки.**

---

## Описание проекта

Заказчик исследования — **Министерство культуры Российской Федерации**.

Вам необходимо:
- Изучить рынок российского кинопроката и выявить текущие тренды.
- Уделить внимание фильмам, получившим государственную поддержку.
- Попробовать ответить на вопрос: насколько такие фильмы интересны зрителю.

Вы будете работать с данными, опубликованными на портале открытых данных Министерства культуры. Набор данных содержит информацию о:
- Прокатных удостоверениях,
- Сборах и государственной поддержке фильмов,
- Данных с сайта КиноПоиск.

---

## Инструкция по выполнению

### Шаг 1. Открытие и объединение данных

1. Откройте файлы с данными.
2. Объедините данные так, чтобы все объекты из датасета `mkrf_movies` обязательно вошли в итоговый датафрейм.

**Пути к файлам:**
- `/datasets/mkrf_movies.csv` — данные о прокатных удостоверениях.  
  [Скачать датасет]
- `/datasets/mkrf_shows.csv` — данные о прокате в российских кинотеатрах.  
  [Скачать датасет]

### Шаг 2. Предобработка данных

1. **Проверка типов данных**  
   Проверьте типы данных в датафрейме и преобразуйте их, где это необходимо.

2. **Обработка пропусков**  
   - Изучите пропуски в датафрейме.
   - Объясните, почему были заполнены пропуски определённым образом или почему вы не стали этого делать.

3. **Обработка дубликатов**  
   - Проверьте наличие дубликатов.
   - Опишите возможные причины их появления.

4. **Работа с категориальными данными**  
   - Изучите столбцы, содержащие категориальные значения.
   - Определите общую проблему, встречающуюся почти во всех категориальных столбцах.
   - Исправьте проблемные значения в поле `type`.

5. **Анализ количественных данных**  
   - Проверьте столбцы с количественными значениями на предмет подозрительных данных.
   - Опишите, как лучше поступить с такими данными.

6. **Добавление новых столбцов**  
   - **Год проката:** Создайте столбец, выделив год из даты премьеры фильма.
   - **Режиссёр и жанр:** Создайте два столбца — с именем и фамилией главного режиссёра, а также с основным жанром фильма (включите первые значения из списка режиссёров и жанров соответственно).
   - **Доля государственной поддержки:** Посчитайте, какую долю от общего бюджета фильма составляет государственная поддержка.

### Шаг 3. Исследовательский анализ данных

1. **Анализ количества фильмов по годам:**
   - Определите, сколько фильмов выходило в прокат каждый год.
   - Учтите, что данные о прокате в кинотеатрах отсутствуют для некоторых фильмов.
   - Посчитайте долю фильмов с указанной информацией о прокате и проанализируйте, как эта доля менялась по годам.
   - Сделайте вывод о том, какой период представлен полнее всего.

2. **Динамика проката:**
   - Проанализируйте, как менялась динамика проката по годам.
   - Определите год с минимальной и максимальной суммой сборов.

3. **Сводная таблица сборов:**
   - С помощью сводной таблицы посчитайте среднюю и медианную сумму сборов для каждого года.
   - Сравните значения и сделайте выводы.

4. **Влияние возрастного ограничения:**
   - Исследуйте, влияет ли возрастное ограничение аудитории (например, «6+», «12+», «16+», «18+» и т. д.) на сборы фильма в период с 2015 по 2019 год.
   - Определите, фильмы с каким возрастным ограничением собрали больше всего денег.
   - Проверьте, меняется ли картина в зависимости от года и предположите возможные причины изменений.

### Шаг 4. Исследование фильмов с государственной поддержкой

- На этом этапе конкретных инструкций нет.
- **Задачи:**
  - Изучите закономерности в данных.
  - Определите, сколько средств выделяется на поддержку кино.
  - Проверьте, насколько хорошо окупаются такие фильмы и какой у них рейтинг.

### Шаг 5. Общий вывод

- Сформулируйте общий вывод по проделанному анализу.

---

## Оформление проекта

- **Среда выполнения:** Jupyter Notebook.
- **Структура работы:**
  - Программный код — в ячейках типа `code`.
  - Текстовые пояснения — в ячейках типа `markdown`.
  - Используйте форматирование и заголовки для удобства восприятия.

---

## Описание данных

### Таблица `mkrf_movies`
Содержит информацию из реестра прокатных удостоверений. У одного фильма может быть несколько удостоверений.

**Столбцы:**
- **title** — название фильма.
- **puNumber** — номер прокатного удостоверения.
- **show_start_date** — дата премьеры фильма.
- **type** — тип фильма.
- **film_studio** — студия-производитель.
- **production_country** — страна-производитель.
- **director** — режиссёр.
- **producer** — продюсер.
- **age_restriction** — возрастная категория.
- **refundable_support** — объём возвратных средств государственной поддержки.
- **nonrefundable_support** — объём невозвратных средств государственной поддержки.
- **financing_source** — источник государственного финансирования.
- **budget** — общий бюджет фильма (включает полный объём государственной поддержки; данные указаны только для фильмов, получивших поддержку).
- **ratings** — рейтинг фильма на КиноПоиске.
- **genres** — жанр фильма.

### Таблица `mkrf_shows`
Содержит сведения о показах фильмов в российских кинотеатрах.

**Столбцы:**
- **puNumber** — номер прокатного удостоверения.
- **box_office** — сборы в рублях.

---

## Критерии оценки проекта

- **Анализ данных:** Описание найденных проблем и методов их решения (замена типов, обработка пропусков и дубликатов).
- **Автоматизация:** Использование автоматизированных подходов для однотипных действий.
- **Выводы:** Представление итоговых данных в сводных таблицах.
- **Визуализация:** Применение методов построения графиков.
- **Структура кода:** Соблюдение структуры проекта и аккуратность кода.
- **Комментарии:** Наличие пояснений к каждому шагу анализа.

---

Успехов в выполнении проекта!

# Технические комментарии
- Версия с опциональной критикой без правок. Сделал лишь так, чтобы тетрадь запускалась и удалил ненужные библиотеке
- Ruby