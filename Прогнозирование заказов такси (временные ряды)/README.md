# Прогнозирование заказов такси

## Описание проекта

У меня был датасет с историческими данными о заказах такси в аэропортах. Чтобы привлекать больше водителей в период пиковой нагрузки, нужно спрогнозировать количество заказов такси на следующий час.

## Навыки и инструменты

* временные ряды
* matplotlib
* seaborn
* seasonal_decompose
* pipeline
* phik
* DecisionTreeRegressor
* LinearRegression
* LGBMRegressor
* KNeighborsRegressor
* adfuller
* plot_ac


## Общий вывод

Я изучила исторические данные компании "Четенькое такси" о заказах такси в аэропортах. Данные в датасете были представлены с начала марта по конец августа.

Проведя анализ данных, я выяснила, что с наступлением лета количество заказов в такси стабильно растет, скорее всего это связано с сезоном отпусков. Закономерности по количеству заказов в течение дня я не обнаружила. Думаю это связано с тем, что самолеты прилетают в любое время дня.

Для обучения модели я добавила в датасет новые признаки: календарные признаки (час, день недели и месяц), отстающие значения, скользящее среднее. После выбора, обучения и тестирования модели выянилось, что модель недообучилась, поэтому я решила добавить еще один признак - разность временного ряда.

Для выполнения задачи я обучила 5 разных моделей: LinearRegression, SVC, DecisionTreeRegressor, KNeighborsRegressor и LGBMRegressor и подобрала для них гиперпараметры. Лучшей оказалась модель LGBMRegressor c гиперпараметрами max_depth=2, num_leaves=13. RMSE на тренировочной выборка равна 27,7.

Проведя тестирование модели на тестовых данных я получила RMSE = 45,1.

