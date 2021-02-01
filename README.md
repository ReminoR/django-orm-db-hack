# db-hack
Представляем вашему скрипты "удачливых" учеников.  
Данный модуль содержит 3 функции:
 - fix_marks - исправление плохих оценок на хорошие
 - remove_chastisements - удаление замечаний
 - create_commendation - похвала


## Начало использования
Чтобы начать использовать скрипты положите файл *scripts.py* в корневую папку электронного журнала (вашего сайта). Запустите shell импортируйте скрипты с помощью команды
```python
from scripts import fix_marks, remove_chastisements, create_commendation
```
Следуйте дальнейшим указаниям.

>Обратите внимание. Если вы копируете функцию из файла в shell и запускаете ее там, не забудьте импортировать необходимые модели и библиотеки
```python
from datacenter.models import Mark, Schoolkid, Chastisement, Lesson, Commendation
from django.core.exceptions import ObjectDoesNotExist, MultipleObjectsReturned
import random
```

## Функция fix_marks
Принимает в качестве аргументов учетную запись ученика и желаемую оценку. Исправляет все оценки (2 или 3) на заданную вами оценку (4 или 5)

**Пример использования**
```python
fix_marks(schoolkid, desired_evaluations)
```

## Функция remove_chastisements
Также принимает на вход учетную запись ученика и удаляет все его замечения из журнала.

**Пример использования**
```python
remove_chastisements(schoolkid)
```

## Функция create_commendation
Функция добавляет поощрение выбранному ученику по указанному предмету. Похвала выбирается автоматически.
Принимает на вход 2 аргумента: 
- full_name - имя ученика
- subject_title - название предмета

**Пример использования**
```python
create_commendation('Алексей', 'Математика')
```

Приятного использования!
