# О проекте
Это учебный проект - Домашнее задание по курсу обучения по git от yandex education.
[Ссылка на курс](https://practicum.yandex.ru/profile/git-basics/)
Пример файла .md в репозитарии github c краткой шпаргалкой по типовым операциям 
# Шпаргалка по GIT
## бщие сведения
**GIT** –система контроля версий с активной поддержкой и открытым исходным кодом. Консольное приложение GitBrush позволяет работать с локальными репозиториями (хранилищами файлов) и синхронизировать их с облачными репозиториями.
Подробнее:  
[Книжка по Git](https://git-scm.com/book/ru/v2)

**GITHUB** – облачное решение от Microsoft для контроля версий с хранением репозиториев в облаке. Это облачная платформа где программисты могут хранить свои проекты, контролировать их версии и публиковать их.  
[Ссылка на GitHub](https://github.com/)

## Начало работы с Git:
1. Скачать и поставить дистрибутив под нужную ОС:  
https://git-scm.com/download/

## Создать локальный репозитарий (на примере простейшего проекта с одним файлом): 
1. Запустить GitBrush
2. Переходим в домашний каталог  
cd  ~
3. Создаем папку для своих локальных проектов git в домашнем каталоге:  
mkdir git
4. Создаем папку проекта:  
mkdir ~\git\testprogect
5. Заходим в папку проекта  
cd ~\git\testprogect
6. Создаем пустой файл с описанием проекта:  
touch readme.md
7. Инициализируем локальный репозитарий git:  
git init
8. Проверяем, что в папке проекта появилась папка репозитрия .git  
ls –al
9. Проверяем статус репозитария  
git status
10. Добавляем все файлы из текущей папки к коммиту (можно добалять все –all или отдельные файла по именам). Далее в рамках коммита будет зафиксирвоана версия добавленных файлов  
git add .
11. Выполняем коммит (фиксируем состояние добавленных файлов, чтобы впоследствии контролировать внесенные в них изменения). К каждому коммиту (слепку, состоянию) можно добавлятькомментарий  
git commit -m "Пустой репозиторий"

## Настройка GitHub и синхронизация с локальным репозитарием
1. Заходим на github и создаем аккаунт, набор ключей доступа и репозитарий для нашего проекта по документации:  
[Быстрый старт по GitHub](https://docs.github.com/ru/get-started/quickstart)
2. В разделе "Quick setup — if you’ve done this kind of thing before" созданного репозитария копируем путь к репозитарию и связываем локальный репозитарий с созданным репозитарием на github:  
git remote add origin <сюда вставить путь к репозитория>
3. Проверить репозитарий:  
git remote –v
4. Передать локальный репозитарий на GitHub (ключ –u и название origin и ветки master нужно только первый раз):  
git push -u origin master
5. В любом текстовом редакторе заполняем файл readme.md используя разметку MarkDown, описание разметки здесь:  
https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c
6. Добаить измененный файл к коммиту  
git add readme.md
7. Коммит репозитария  
git commit -m "V1 readme.md – ВВЕДЕН ТЕКСТ" 
8. Отпраить на GitHub обновленную версию репозитария  
git push
9. Проверить результат на GITHUB  
