Занятие 3
=========

## Материал

Изученные команды:

* [`grep`](http://linux.die.net/man/1/grep)
* [`su`](http://linux.die.net/man/1/su)

Материал:

* Стандартные потоки ввода-вывода (input, output, errors)
* Конвейер (или _pipeline_)
* Регулярные выражения

## Домашнее задание №3

__К 31 октября!__

### Теоретическая подготовка

1. **Почитайте** про команду `su`, посмотрите, что она ещё умеет. **Выясните**, чем отличается результат выполнения команд `su den` и `su - den`.
* Для чего нужен ключ `-P` команде `grep`?
* **Закрепите**, что такое `.`, `?`, `*`, `+`, `{}`, `()`, `^` и `$` в регулярных выражениях.

Необязательно, но интересно: про конвейеры и потоки ввода-вывода можете подробнее почитать, например, [тут](http://xgu.ru/wiki/%D0%A1%D1%82%D0%B0%D0%BD%D0%B4%D0%B0%D1%80%D1%82%D0%BD%D1%8B%D0%B5_%D0%BF%D0%BE%D1%82%D0%BE%D0%BA%D0%B8_%D0%B2%D0%B2%D0%BE%D0%B4%D0%B0/%D0%B2%D1%8B%D0%B2%D0%BE%D0%B4%D0%B0), [тут](https://docs.altlinux.org/current/modules/linux_pipeline/index.html) или [тут](http://habrahabr.ru/post/195152/), источников много :)

### Практические задания

#### О выполнении заданий

1. В качестве ответа засчитывается не просто цифра/строчка, получившаяся в результате, но и сама программа!
* У себя в домашнем каталоге создайте директорию `hw3`, где вы будете записывать результаты.
* Результаты работы программы сохраняйте в созданной директории `hw3`; для каждого задания создайте свой файл, названием которого будет являться номер задания, и запишите туда результат.

  > _Подсказка_! Вместо того, чтобы вручную создавать файлы и вписывать туда результат, просто перенаправляйте вывод вашей программы. Например:
  > 
  > Второе задание просит вас вывести строчку `hi`. Для этого вы написали программу `echo "hi"`. Значит, в директории `hw3` у вас должен быть файл с названием `2`, в котором будет эта строка — `hi`. Вы можете просто перенаправить вывод сразу в файл (он создастся автоматически, но директория `hw3` уже должна существовать): `echo "hi" | cat > /home/*your-login*/hw3/2`.
* Помимо результата попрошу предоставить мне саму программу. Пока проще всего, если вы пришлёте её мне на email, не надо прикреплять никаких файлов, просто голый текст вставьте в сообщение (в теме письма подпишите, какое (какие) задание (задания) вы отсылаете, а так же не забудьте представиться, если ваш email не очень говорит о том, какая у вас фамилия :) ). Чтобы скопировать в PuTTY текст, выделите его, нажмите правой кнопкой мыши — это поместит выделенный фрагмент в буфер обмена (контекстное меню не появится).

#### Задания

1. Сколько пользователей в системе имеют восьмибуквенный логин согласно файлу [`/etc/passwd`](https://ru.wikipedia.org/wiki/%2Fetc%2Fpasswd)?
* У скольки пользователей (согласно этому же файлу) shell'ом является **не** `/bin/bash`?

  > Два комментария. _Первый_: shell указан в последнем столбце файла. _Второй_: почитайте `man grep`, есть один ключ, которым вам облегчит выполнение задания.
* В файле `/home/enf/rollcall` записаны фамилии и языки. Сколько всего слов в файле? Сколько человек знает русский язык? Ответ запишите подряд на разных строчках одного файла.
* Сколько пользователей что-нибудь изменяли последний раз в своей домашней директории 24-го октября?

  > Подсказка: подробный список директорий в `/home/` вам поможет.
