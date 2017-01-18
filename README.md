# Тестовое задание

Для выполнения этого задания сделайте форк этого репозитория, и по готовности сделайте пулл реквест. Руби 2.2 и только std-lib

## Вычисление выражения в обратной польской записи

Написать программу, которая вычисляет выражения в обратной польской нотации.

Например, если на вход ей дать выражение `5 1 2 + 4 * + 3` - (что эквивалентно `5 + ((1 + 2) * 4) - 3` в нормальной записи), то она даст ответ `14`.  Валидными операциями являются `+`, `-`, `\*`, `/`, `^`.

Если передано пустое выражение, программа возвращает `0`.


Программая должна выполняться из консоли и печатать ответ в `stdout`, например:

```
$ ruby calc_polish_notation.rb 5 1 2 + 4 * + 3 -
14
```

## Счастливый билет

Написать программу, которая получает на вход номер билета и вычисляет, счастливый он или нет. Счастливым билет считается, если сумма цифр справа от центра числа совпадает с суммой цифр слева от центра числа.


### Например:

```
003111     ->  3 == 1 + 1 + 1
813372     ->  8 + 1 + 3 == 3 + 7 + 2
17935       -> 1 + 7 == 3 + 5
56328116 ->  5 + 6 + 3 + 2 == 8 + 1 + 1 + 6
```

Программа должна выполняться из консоли и печатать ответ в stdout:

```
$ ruby check_lucky_ticket.rb 23334
false
$ ruby check_lucky_ticket.rb 253343
true
```

## Парсинг файла

Написать программу которой на вход подается файл с числами, каждое на отдельной строке (исходный файл прилагается). Выбрать первые 10 простых чисел.


Результат сложить в отдельный файл который можно указать в аргументах с ключем `-o`, в противном случае в stdout.
Основное требование чтобы файл не загружался целиком в память и разбирался потоково с помощью IO, потому как файл может весить очень много.


Программа должна выполняться из консоли:

```
$ ruby file_parser.rb ./production.log -o out.log
```

## Бонусное задание:

Нужно разобрать уже весь файл по тем же самым условиям, только в несколько потоков. Кол-во потоков указывается параметром `-n` и должно быть от 1 до 32, в случае если не указано, должно быть равно кол-ву процессоров в системе.

При возможности придумать как организовать хронологическую запись в файл.


Файл: https://www.dropbox.com/s/se16fytnquizfa5/numbers.txt.gz?dl=0
