---
## Front matter
lang: ru-RU
title: Лабораторная работа №2 "Управление версиями"
author: Камкина Арина Лео
institute: РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
date: |
  \Москва
  \2021-2022

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

# **Цель работы**

- Изучить идеологию и применение средств контроля версий.
- Освоить умения по работе с git.

---

# **Задание**

- Создать базовую конфигурацию для работы с git.
- Создать ключ SSH.
- Создать ключ PGP.
- Настроить подписи git.
- Зарегистрироваться на Github.
- Создать локальный каталог для выполнения заданий по предмету.

---

# **Базовая информаци я о GIT**

## Установка git-flow в Fedora Linux

> cd /tmp

> wget --no-check-certificate -q https://raw.github.com/petervanderdoes/gitflow/develop/contrib/gitflow-installer.sh

> chmod +x gitflow-installer.sh

> sudo ./gitflow-installer.sh install stable
## Установка gh в Fedora Linux
> sudo dnf install gh
## Базовая настройка git
- Зададим имя и email владельца репозитория:
> git config --global user.name "Name Surname"

> git config --global user.email "work@mail"
-  Настроим utf-8 в выводе сообщений git:
> git config --global core.quotepath false
git config --global init.defaultBranch master
- Параметр autocrlf:
> git config --global core.autocrlf input
- Параметр safecrlf:
> git config --global core.safecrlf warn
## Создание ключей ssh
- по алгоритму rsa с ключём размером 4096 бит:
> ssh-keygen -t rsa -b 4096
- по алгоритму ed25519:
> ssh-keygen -t ed25519
## Создание ключа pgp
- Генерируем ключ
> gpg --full-generate-key

---

# **Ход работы**

1. Для начала создала учётную запись на github и заполнила основные данные.

2. Установила git-flow в Fedora Linux (рис. [-@fig:001])

![Установка git-flow](image/1.png)
{ #fig:001 width=70% }

3. Установила gh в Fedora Linux (рис. [-@fig:002])

![Установка gh](image/2.png)
{ #fig:002 width=70% }

4. Произвела базовую настройку git (рис. [-@fig:003])

![Базовая настройка](image/3.png)
{ #fig:003 width=70% }

5. Произвела базовую настройку git (рис. [-@fig:004] [-@fig:005])

![создание ключа ssh по алгоритму rsa с ключём размером 4096 бит](image/4.png)
{ #fig:004 width=70% }
![создание ключа ssh по алгоритму ed25519](image/5.png)
{ #fig:004 width=70% }

6. Создала ключ pgp и добавила его в github (рис. [-@fig:006])

![Список ключей pgp](image/6.png)
{ #fig:007 width=70% }

7. Добавила его в github и настроила автоматические подписи коммитов git и авторизовалась (рис. [-@fig:007])

![Настройка автоматических подписей коммитов git ](image/7.png)
{ #fig:007 width=70% }

8. Создала каталог и затем перешла в него (рис. [-@fig:008])

![Создание и переход в каталог ](image/8.png)
{ #fig:008 width=70% }

9. Создала репозиторий на основе шаблона (рис. [-@fig:009])

![Создание репозитория по шаблону](image/9.png)
{ #fig:009 width=70% }

10. Настроила каалог курса и отправила нужные файлы на сервер (рис. [-@fig:0010] [-@fig:0011)

![Настройка каталога 1 ](image/10.png)
{ #fig:0010 width=70% }
![Настройка каталога 2 ](image/11.png)
{ #fig:0011 width=70% }

---

# **Вывод**

Освоила работу с git и получила знания о некоторых его функциях.


