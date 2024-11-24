# АНАЛИЗ ДАТАСЕТА С ИНФОРМАЦИЕЙ О ПОСЕТИТЕЛЯХ ВЕБ-САЙТА В Power BI
## Импорт данных
Загружаем наш датасет в Power BI:
"Home" → "Get Data" → "Text/CSV"

## Проверка и подготовка данных

Проверим, что:
* Дата в столбце Date имеет формат Date, далее отсортируем все по дате
* Столбцы правильно отображаются (нет лишних или пустых строк).
![image](https://github.com/user-attachments/assets/c8e8845f-4774-4da8-939e-696796db7b0e)

## Построение графиков и визуализаций

### График посещаемости по датам
Выбераем "Line Chart" (график линий) из панели визуализаций.
![image](https://github.com/user-attachments/assets/34e082de-b757-4563-b421-cfaddaa25dfa)

### Распределение по дням недели
![image](https://github.com/user-attachments/assets/29333b79-5cfd-42d8-b2e2-648359593c1e)

### Круговая диаграмма: доля первых и возвращающихся посещений
![image](https://github.com/user-attachments/assets/eb021762-c28b-4e38-96f2-7b68b255f012)

### Матрица с распределением посещаемости по дням и датам
![image](https://github.com/user-attachments/assets/0e960c3e-9acf-418b-93dd-d22c81b69b95)

## Добавление вычисляемых метрик с помощью DAX

### Retention Rate (Удержание пользователей):
Эта мера покажет, какой процент пользователей возвращается на сайт.
Retention Rate = DIVIDE(SUM('daily-website-visitors'[Returning.Visits]), SUM('daily-website-visitors'[Unique.Visits])) * 100
![image](https://github.com/user-attachments/assets/e1e91670-6c48-4587-a8e7-45d8faabf5f3)

## Настройка дашборда

Добавим срез по дате. Теперь мы сможем анализировать данные за определенные периоды времени
![image](https://github.com/user-attachments/assets/31bc01e2-b0d2-41cb-b5af-245f026080ef)
![image](https://github.com/user-attachments/assets/f56fdabd-840d-40fd-a0db-ab04e4e5fce7)

