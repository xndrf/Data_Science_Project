# 🚢 Titanic: Machine Learning from Disaster

<div align="center">

![Titanic](https://storage.googleapis.com/kaggle-competitions/kaggle/3136/logos/header.png)

[![Kaggle](https://img.shields.io/badge/Kaggle-Competition-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/competitions/titanic)
[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

*Прогнозирование выживаемости пассажиров Титаника - классическая задача машинного обучения для начинающих*

</div>


## Описание задачи

**Задача:** Построить модель машинного обучения, которая предсказывает, какие пассажиры выжили после крушения Титаника.

**Цель:** Достичь максимальной точности предсказания на тестовой выборке.

**Метрика:** Accuracy (доля правильных ответов)

## Данные

Набор данных содержит информацию о 891 пассажире для обучения и 418 для тестирования.

### Структура данных:

| Поле | Описание | Тип |
|------|-----------|------|
| **PassengerId** | Уникальный идентификатор пассажира | Числовой |
| **Survived** | Целевая переменная: 0 = Погиб, 1 = Выжил | Бинарный |
| **Pclass** | Класс билета (1, 2, 3) | Категориальный |
| **Name** | Имя пассажира | Текстовый |
| **Sex** | Пол | Категориальный |
| **Age** | Возраст | Числовой |
| **SibSp** | Количество братьев/сестер/супругов на борту | Числовой |
| **Parch** | Количество родителей/детей на борту | Числовой |
| **Ticket** | Номер билета | Текстовый |
| **Fare** | Стоимость билета | Числовой |
| **Cabin** | Номер каюты | Текстовый |
| **Embarked** | Порт посадки (C = Cherbourg, Q = Queenstown, S = Southampton) | Категориальный |

### Основные результаты:

RandomForest  Accuracy 0.8406
