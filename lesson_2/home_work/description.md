### Как выполнить домашнее задание ?

1. Напишите тесты для всех функций в директории tests/functions_test

например:
```python

from unittest import TestCase

from lesson_2.home_work import functions as f


class FunctionsTest(TestCase):
    def test_get_max(self):
        a, b = 33, 77
        result = f.get_max(a, b)
        self.assertEqual(b, result) 
```

В терминале наберите:

`python3 -m unittest lesson_2/home_work/tests/functions_test.py `


в результате у вас должен быть один не прошедший тест

`AssertionError: 77 != None`


Реализуйте функции `get_max(a, b)` так, чтобы она возвращала 
корректный результат

```python
def get_max(a, b):
    return a if a > b else b
```

Снова в терминале наберите:

`python3 -m unittest lesson_2/home_work/tests/functions_test.py `

`Ran 7 tests in 0.001s OK`

Поздравляю вы реализовали функцию, которая прошла тестирование успешно.

Этот принцип разработки называется **TDD** - Test Driven Development.
Поэтому принципу сперва пишется тест а потом реализация.


Далее точно таким же образом допишите остальные функции.


