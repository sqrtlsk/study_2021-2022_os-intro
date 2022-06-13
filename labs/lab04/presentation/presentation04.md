---
## Front matter
lang: ru-RU
title: Лабораторная работа №4 Основы интерфейса взаимодействия пользователя с системой Unix на уровне командной"
author: Камкина Арина Леонидовна
institute: RUDN University, Moscow, Russian Federation
date: NEC--2022

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Цель работы

Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.

---

# Задание

1. Определите полное имя вашего домашнего каталога. Далее относительно этого каталога будут выполняться последующие упражнения.
2. Выполните следующие действия:
    1. Перейдите в каталог /tmp.
    2. Выведите на экран содержимое каталога /tmp. Для этого используйте команду ls с различными опциями. Поясните разницу в выводимой на экран информации.
    3. Определите, есть ли в каталоге /var/spool подкаталог с именем cron?
    4. Перейдите в Ваш домашний каталог и выведите на экран его содержимое. Определите, кто является владельцем файлов и подкаталогов?

--- 

3. Выполните следующие действия:
    1. В домашнем каталоге создайте новый каталог с именем newdir.
    2. В каталоге ~/newdir создайте новый каталог с именем morefun.
    3. В домашнем каталоге создайте одной командой три новых каталога с именами letters, memos, misk. Затем удалите эти каталоги одной командой.
    4. Попробуйте удалить ранее созданный каталог ~/newdir командой rm. Проверьте, был ли каталог удалён.
    5. Удалите каталог ~/newdir/morefun из домашнего каталога. Проверьте, был ли каталог удалён.
4. С помощью команды man определите, какую опцию команды ls нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов,
входящих в него.

---

5. С помощью команды man определите набор опций команды ls, позволяющий отсортировать по времени последнего изменения выводимый список содержимого каталога
с развёрнутым описанием файлов.
6. Используйте команду man для просмотра описания следующих команд: cd, pwd, mkdir,
rmdir, rm. Поясните основные опции этих команд.
7. Используя информацию, полученную при помощи команды history, выполните модификацию и исполнение нескольких команд из буфера команд.

---

# Предварительные сведения
**Команда man** 
 используется для просмотра (оперативная помощь) в диалоговом режиме руководства (manual) по основным командам операционной системы типа Linux.
> man <команда>

**Команда cd**
  используется для перемещения по файловой системе операционной системы типа Linux.
 > cd <каталог>

 **Команда ls**
 используется для просмотра содержимого каталога.
Формат команды:
> ls [-опции] [путь]

**Команда pwd**
для определения абсолютного пути к текущему каталогу используется
команда pwd (print working directory).
> pwd

---

**Команда mkdir**
используется для создания каталогов.
> mkdir имя_каталога1 [имя_каталога2...]

**Команда rm**
используется для удаления файлов и/или каталогов.
> rm [-опции] [файл]

**Команда history**
для вывода на экран списка ранее выполненных команд используется команда 
> history

---

# Ход работы

1. Перешла в доиашний каталог и посмотрела его полное имя командой pwd (рис. [-@fig:001])

![Полное имя домашнего каталога](image/1.png)
{ #fig:001 width=70% }

2. Перешла в каталог tmp (рис. [-@fig:002])

![Переход в каталог tmp](image/2.png)
{ #fig:002 width=70% }

---

3. Посмотрела содержимое каталогa tmp, используя функции  ls и ls -a (рис. [-@fig:003])

![Содержимое каталога tmp](image/3.png)
{ #fig:003 width=70% }

4. Посмотрела содержимое каталога /var/spool, чтобы определить есть ли там cron (его нет) (рис. [-@fig:004])

![Содержимое /var/spool](image/4.png)
{ #fig:004 width=70% }

---

5. Перешла в домашний каталог и посмотрела его содержимое (рис. [-@fig:005])

![Содержимое домашнего каталога](image/5.png)
{ #fig:005 width=70% }


6. В домашнем каталоге создала каталог newdir (рис. [-@fig:006])

![Создание каталога newdir](image/6.png)
{ #fig:006 width=70% }

---

7. Перешла в каталог newdir и создала каталог morefun (рис. [-@fig:007])

![Создание каталога morefun](image/7.png)
{ #fig:007 width=70% }

8. Cоздала одной командой mkdir три новых каталога с именами
letters, memos, misk, затем удалила эти каталоги одной командой rm -r, каждый раз просматривая содержимое (рис. [-@fig:008])

![Создание и удаление каталогов letters, memos, misk](image/8.png)
{ #fig:008 width=70% }

---

9. Попробовала удалить каталог newdir командой rm, не получилось (рис. [-@fig:009])

![Попытка удаления newdir через rm](image/9.png)
{ #fig:009 width=70% }

10. Удалила каталог morefun командой rm -r (рис. [-@fig:0010])

![Удаление каталога morefun через rm -r](image/10.png)
{ #fig:0010 width=70% }

---

11. Посмотрела информацию по ls через man и выяснила, что -R нужно использовать для просмотра содержимое не только указанного каталога, но и подкаталогов,
входящих в него (рис. [-@fig:0011])

![ls -R](image/11.png)
{ #fig:0011 width=70% }

12. Посмотрела информацию по ls через man и выяснила, что -c -lt  позволет отсортировать по времени последнего изменения выводимый список содержимого каталога с развёрнутым описанием файлов (рис. [-@fig:0012])

![ls -c -lt](image/12.png)
{ #fig:0012 width=70% }

---

13. Использовала команду man для просмотра описания следующих команд: cd, pwd, mkdir,
rmdir, rm (рис. [-@fig:0013])

![man cd, pwd, mkdir, rmdir, rm](image/13.png)
{ #fig:0013 width=70% }

14. Использовала команду history (рис. [-@fig:0014])

![history](image/14.png)
{ #fig:0014 width=70% }

---

# Вывод

Я приобрела практические навыки работы с системой посредством командной строки.
---