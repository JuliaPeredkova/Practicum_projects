# Модель для поиска негативных комментариев

## Описание проекта

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.

Необходимо обучить модель классифицировать комментарии на позитивные и негативные.

Значение метрики качества F1 должно быть не меньше 0.75.

## Навыки и инструменты

* работа с текстом
* pandas
* pymystem3
* nltk
* TfidfVectorizer
* LogisticRegression
* DecisionTreeClassifier
* tqdm

## Общий вывод

В проекте я классифицировала комментарии на положительные и отрицательные. В начале я подготовила данные: лемматизировала столбец, очистила данные от лишних символов и слов, провела оценку важности слов.

Передо мной стояла задача бинарной классификации. Я построила две модели LogisticRegression и DecisionTreeClassifier и обучила их на тренировочный данных. У модели LogisticRegression получилась более высокая метрика качетсва 0,76. Я провела тестирование этой модели на тестовых данных и получила метрику 0,78, что соответствует заявленной в задании метрике качества.
