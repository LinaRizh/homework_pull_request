# Инструкция по работе с git

## Начало работы с репозиторием
Узнать автора
* _git config --global user.name_
* _git config --global user.email_

Если имя и email пользователя не были заданы необходимо их задаь с помощью:
* _git config --global user.name **"name"**_
* _git config --global user.email "**mail@mail.ru"**_

> **git init**
* _создаёт локальный репозиторий_
## Добавление файлов в репозиторий
> **git add file_name**
* _добавляет файл _**file_name**_ для отслеживания_ 

При использовании git add необязательно писать наименование файла полностью (если файлы не повторяются), можно начать писать наименование и git допишет его за вас.

> **git add .**
* *добавляет все файлы*
> **git add *.__"расширение"__**
* добавляет файлы определённого расширения

> **git commit -m "some message"**
* _Фиксирует файлы, которрые были добавлены для отслеживания. Фиксирует версии с учётом изменений_

* _При использовании __git commit -a -m "some message"__ можно не добавлять файл через git add. __Git commit -a -m "some message"__ зафиксирует все файлы которые не закомиитили_

## Переход между коммитами
> **git checkout commit_code**
* _Переходит к commit с кодом commit_code (сам код можно посмотреть по git log, можно не писать весь код, а указать только первые 4 символа)_
> **git checkout master**
* _Вернуться к актуальному состоянию_

Если забыли какую либо команду смотрите раздел **"Справка"**.

## Отслеживание состояния репозитория

> **git status**
* _Показывает изменённые файлы и файлы, готовые для commita_
> **git log**
* _Показывает все commiti_ 
> **git log --graph**
* визуализирует ветки в виде графа
> **git diff**
* _Показывает разницу между текущей версией и зафиксированной_
## Оформление
### Стили текста в Git

    Для выделения текса **жирным шрифтом** необходимо обрамить его ** или __ 
    Для выделения текста *курсивом* необходимо обрамить его * или _
    Для того, чтобы ~~зачеркнуть текст~~, необходимо обрамить его ~~

### Списки в Git
* Для создания нумерованного списка ставим в начале каждой строки цифру с точкой. 
    1. Текст 1
    2. Текст 2
    3. Текст 3

* Для создания ненумерованного списка в начале каждой строки ставим *
    * Текст 1
    * Текст 2
    * Текст 3 

## Ветки в Git
> **git branch**
* посмотреть все существующие ветки
> **git branch "branch_info"**
* создание новой ветки c имененм branch_info
> **git checkout branch_info**
* переключение на ветку branch_info

## Удаление веток
> **git branch -d "branch_info"**
* удаляет ветку "branch_info". Работает только если все изменения удаляемой ветки сохранены и перенесены в другую ветку
> **git branch -D "branch info"**
* удаляет ветку "branch_info" в любом случае (даже если изменения не сохранены и не перенесены в другую ветку)

## Слияние веток и решение конфликтов
> git merge branch_info
* добавляет ветку branch_info в текущую ветку

Для решения конфликта при слиянии папок необходимо выбрать __*AcceptCurrentChange или AcceptIncomingChange или AcceptBothChanges или CompareChange*__ и, при необходимости, отредактировать текст.

## Справка
Чтобы вызвать справку для какой-то команды необходимо добавить тег:
> --help 
Например: 
* git add --help
* git commit --help
* git branch --help
## Работа с удалённым репозиторием 
__*GitHub*__ - наиболее распростран1нный сервис по работе с удалёнными репозиториями.

>**git clone "ссылка на репозитрий"**
* Копирует удалённыё репозиторий на ПК. Ссылку на репозиторий копируме на странице GitHub (code)
>**git pull**
* Копирует всё из удалённого репозитория в текущий и сливает всё воедино, при возникновении конфликта запрашивает дальнейшие действия. Конфликты решаются аналогично конфликтам при слиянии веток.
>**git push**
* позволяет отправить текущую версию репозитория на внешний репозиторий. Данная команда требует обязательной авторизации на GitHub, т.е. у Вас должны быть права на внесения изменений в репозиторий.
>**git remote** 
* проверяе наличие соединений с удалёнными репозиториями

## **Делаем pull request**
1. Делаем **fork** удалённого репозитория
2. Делаем **clone** своей версии репозитория 
3. Создаём новую ветку и в неё вносим свои изменения
4. Фиксируем изменения 
5. Отправляем свою версию в свой GitHub
6. На сайте GitHub нажимаем кнопку **pull request**

End

![no image](Git.png)