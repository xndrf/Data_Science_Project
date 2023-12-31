# Проект 1. Анализ вакансий HeadHunter

## Оглавление
- Цель проекта
- Задачи проекта
- Проблематика проекта
- Список используемых данных
- Список используемых библиотек в проекте
- Итоги проекта
- Дополнительные сведения о проекте

## Цель проекта
Исследование базы данных HeadHunter c построением модели основных характеристик соискателей

## Задачи проекта
1. Выполнить базовый анализ структуры данных;
1. Выполнить преобразования данных;
1. Провести разведовательный анализ с исследованием основных зависимостей;
1. Выполнить очистку  данных.

## Проблематика проекта
Часть соискателей не указывает желаемую заработную плату, когда составляет резюме и в связи с этим команда HeadHunter хочет построить модель, которая бы автоматически определяла примерный уровень заработной платы, подходящей пользователю, исходя из информации, которую он указал о себе.

## Список используемых данных
1. Данные по соискателям выгруженные за период с 10.04.2018 по 15.05.2019 по городам РФ;
- [ссылка на доступ к данным HeadHunter](https://drive.google.com/file/d/1MlY1ibOSJj2YLUXrhP8Pqqz6JvBYq0sw/view)
1. Данные по кросс курсах валютам, сгенерированные на период выгрузки данных с hh
 - [ссылка на доступ к сайту по генерации кросс курсах валют](https://mfd.ru/)

## Список используемых библиотек в проекте

```python
# Библиотека для отображения графиков Plotly через nbviewer:
from plotly.offline import plot, iplot, init_notebook_mode
init_notebook_mode(connected=True)

# Библиотеки для работы с данными:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.express as px

# Библиотека для построения линии аномальных значений в задании 8, при построении графика в plotly:
import plotly.graph_objects as go

# Библиотека для возможности отображения графиков на nbviewer:
import plotly.io as pio
```

## Итоги проекта
- **Предварительно исследованы данные:**
1. Чтение DataFrame;
1. Выведена информация по строкам таблицы;
1. Выведена информация о числе непустых значений в столбцах;
1. Выведена информация по основной статистической информации.
-  **Выполнено преобразование данных:**
1. Извелечена и унифицирована информация по признакам **Образования**;
1. Извлечена и преобразована информация по **Полу** и **Возрасту** соискателей;
1. Извлечена и преобразованна информация по **Опыту работы** соискателей, и превидена в единую систему измерения *месяц*;
1. Извлечена и структурированна информация по **Городам**, преобразованна информация по Готовности соискателей к **командировкам** и **переездам**;
1. Извлечена и преобразованна информация по **Занятости** и **Графику** соискателей;
1. Извлечены и преобразованны данные по **курсам валют** к общепринятым сокращениям.
- **Исследование зависимостей в данных показало (не очищенных данных):**
1. Выявлены предварительные аномальные значения возраста, опыта работа, желаемой заработной платы, образования (люди с высшим обращованием в 14 лет).
1. Мода распределения возраста соискателей равна 30 годам; Максимальное количество соискателей приходится на возраст от 25 до 45 лет - определим это как возраст старта профессионального взросления в сфере рынка труда; 
1. Мода распределения опыта работы соискателей составляет 6 лет и 9 месяцев; Большинство соискателей имеют опыт работы от 0 месяцев до 250 месяцев;
1. Мода распределения заработной платы соискателей составляет 30 тысяч рублей; Межквартальный размах зарплаты находится в границах от 37 до 95 тысяч рублей, а желание по заработной плате доходят аж до 24 304 880 руб/месяц (Большая вероятность аномалии);
1. Больше всех хотят зарабатывать люди которые: обучались в ВУЗе, те кто готов к командировкам и переезду, и кто живёт в большом городе;
1. Выполнены дополнительные построения графиков и выявлено, что большинством соискателей на hh являются мужчины, превышают количество женщин в 5 раз; Выведен топ 5 медианных значения зарплат, и больше всего зарплату получают **Руководителеи проектов**.
- **Выполнена очистка данных:**
1. Найдены и удалены дубликаты в данных;
1. Определены пропуска, часть которых была заполненна медианными значениями, часть почищена;
1. Очищены аномальные данные, где в резюме заработная плата была выше 1 млн. рублей и ниже 1 тысячи рублей, где опыт работы равен или превышает возраст соискателя;
1. Выполнена дополнительная проработка распределения возраста в логарифмическом масштабе, и на основе метода z-отклонений, при сигме (left=3, right=4) определено 3 аномальных значения возраста, которые впоследствии очищены из DataFrame.

## Дополнительные сведения о проекте
В связи с тем, что GitHub не позволяет просматривать графики с библиотеки plotly рекомендуемы источник просмотра проектной работы сайт [nbviewer.org](https://nbviewer.org).

#### **Ссылка на данный проект на сайте nbviewer.org находится [здесь](https://nbviewer.org/github/xndrf/Data_Science_Project/blob/e9d06274774034a39d08d5ffb6cbb05c1ac2b41f/Research_hh%28Part_1%29/Project-1.%20Ноутбук-шаблон.ipynb)**