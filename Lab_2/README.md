# Lab 2

## Хід роботи
1. За допомогою пакетного менеджера *PIP* встановив *pipenv* та створив ізольоване середовище для Python:
```
pip install pipenv
pipenv --python 3.6
pipenv shell
```
2. Встановив бібліотеки (*requests, ntplib*):
```
pipenv install requests
pipenv install ntplib
```
3. Створив файл *app.py*, протестував та запустив, програма працює правильно.

+ Перевірка на коректне виконання скрипта `app.py`.
Вивід:
```
========================================
Результат без параметрів: 
No URL passed to function
========================================
Результат з правильною URL: 
Time is:  10:06:58 PM
Date is:  11-10-2020

```

4. Для тестування встановив бібліотеку *pytest*, запустив тести, всі тести виконались успішно:
```
pipenv install pytest
pytest tests/tests.py
```
+ Результати виконання тестів `tests.py`. Вивід: 
```
============================= test session starts ==============================
platform linux -- Python 3.6.9, pytest-6.1.2, py-1.9.0, pluggy-0.13.1
rootdir: /home/andrii/labs/Lab_2
collected 4 items

tests/tests.py ....                                                      [100%]

============================== 4 passed in 2.70s ===============================
```
5. Дописав у програмі (*app.py*) функцію, яка буде перевіряти час доби AM/PM та виводити "Доброго дня/ночі". Також у файлі (*tests.py*) написав тест який перевіряє правильність роботи функції.

+ Результати виконання модифікованого `app.py`:
```
========================================
Результат без параметрів: 
No URL passed to function
========================================
Результат з правильною URL: 
Time is:  10:19:10 PM
Date is:  11-10-2020
Доброго дня

```
6. Виконання функції та тестів перенаправив у файл *results.txt*:
```
pipenv run python3 app.py append >> results.txt
pipenv run pytest tests/tests.py >> results.txt
```

