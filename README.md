# Рецепты

## Задание

Написан простой сервис-помощник для приготовления блюд.

Сервис знает некоторое количество рецептов:

На запрос вида `/omlet/` должен отобразиться список ингредиентов и их количество для приготовления омлета. Аналогично для запроса вида `/pasta/` - список ингредиентов и их количество для приготовления макарон с сыром. Так же есть `/buter/` для рецепта вксного бутера)).

Например:

```
http://127.0.0.1:8000/omlet/

# Ответ
яйца, шт: 2
молоко, л: 0.1
соль, ч.л.: 0.5
```

По умолчанию сервис сообщает количество ингредиентов на 1 порцию. Но если передать опциональный параметр `servings` (целое положительное число), то сервис выдает количество ингрелиентов на указанное число порций.

Например:

```
http://127.0.0.1:8000/omlet/?servings=4

# Ответ
яйца, шт: 8
молоко, л: 0.4
соль, ч.л.: 2.0
```

## Документация по проекту

Для запуска проекта необходимо:

- Установить зависимости:

```bash
pip install -r requirements.txt
```

- Выполнить команду:

```bash
python manage.py runserver
```
