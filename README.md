# Итоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy
API: flask
Данные: с kaggle - https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset 

Задача: предсказать по описанию новости является ли она фейком или нет (поле target). Бинарная классификация

Используемые признаки:

- title(text)
- text (text)
- subject (text)

Преобразования признаков: tfidf

Модель: RandomForestClassifier

### Клонируем репозиторий и создаем образ
```
$ git clone https://github.com/Ksenia-90/news_project.git
$ cd news_project
$ docker build -t ksenia-90/news_project .
```

### Запускаем контейнер

Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)
```
$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models ksenia-90/news_project

```

### Переходим на localhost:8181



