# Проект золотообрабатывающей компании

## Содержание

* [Основная информация](#основная-информация)
* [Описание датасета](#описание-датасета)
* [Дополнительные условия](#дополнительные-условия)
* [Используемые библиотеки python](#используемые-библиотеки-python)


## Основная информация

В рамках проекта строится модель машинного обучения для промышленной компании, разрабатывающая решения для эффективной работы промышленных предприятий. 
**Задача**: С помощью машинного обучения предсказать коэффициент восстановления золота из золотосодержащей руды на основе данных с параметрами добычи и очистки. 
**Цель**: оптимизация производства.

## Описание датасета

Данные по добыче и очистке находятся представлены в трех датасетах:
- gold_recovery_train_new.csv — обучающая выборка, данные по каждому этапу флотации, содержит данные по добавляемых веществам и концентрации веществ на выходе;
- gold_recovery_test_new.csv — тестовая выборка, по сравнению с обучающей выборкой не содержит целевых признаков а также ряд данных по другим веществам, получаемых на выходе из флотации;
- gold_recovery_full_new.csv — исходные данные, содержит полную информацию из обучающей и тестовой выборки.

Данные индексируются датой и временем получения информации (признак date). 
Наименование признаков в датасетах происходит по следующему принципу: [этап].[тип_параметра].[название_параметра]
Пример: rougher.input.feed_ag

Возможные значения для блока [этап]:
- rougher — флотация
- primary_cleaner — первичная очистка
- secondary_cleaner — вторичная очистка
- final — финальные характеристики

Возможные значения для блока [тип_параметра]:
- input — параметры сырья
- output — параметры продукта
- state — параметры, характеризующие текущее состояние этапа
- calculation — расчётные характеристики


## Используемые библиотеки python
- Matplotlib
- NumPy
- Pandas
- Scikit-learn


## Дополнительная информация

Обязательная метрика оценки модели - sMAPE. Формула представлена в коде работы.
