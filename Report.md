# Отчет по лабораторной работе №5

## Цель работы:
Используя навыки работы с Git и ветками, создать скрипт на языке Bash, который будет проверять наличие текста в текстовом файле перед коммитом (Задание 1) и поработать с моделью ветвления GitFlow (Задание 2).

## Ход работы:
### Задание 1
#### 1. Переходим в GitHooks и создаем bash-скрипт
> cd .git/hooks

> touch pre-commit_git.bash

<img width="703" alt="Снимок экрана 2024-12-27 в 13 02 54" src="https://github.com/user-attachments/assets/0d0d91e0-a9ca-403a-9ac7-2e0514a72fc9" />

#### 2. Создаем файл "pre-commit" и добавляем в него код скрипта
>   touch pre-commit
>   nano pre-commit

<img width="797" alt="Снимок экрана 2024-12-27 в 13 05 59" src="https://github.com/user-attachments/assets/53c72dc2-65f0-4a14-ac58-48c38ccf84e7" />


#### 3. Делаем данный файл исполняемым
>    chmod +x pre-commit

#### 4. Проверяем работу
##### Если файл пустой:
> touch test_empty_file_5.txt

> git add test_empty_file_5.txt

> git commit -m "Добавлен файл empty_file_test_5.txt"

<img width="698" alt="Снимок экрана 2024-12-27 в 13 25 56" src="https://github.com/user-attachments/assets/4fb258bb-c73d-44fb-b810-70abed914fd5" />


##### Если файл не пустой:
> touch test_file_6.txt

> open test_file_6.txt

> git add test_file_6.txt

и записываем текст

<img width="603" alt="Снимок экрана 2024-12-27 в 13 44 08" src="https://github.com/user-attachments/assets/88366824-0d9d-4d86-bd80-eb0b35a6731c" />


### Задание 2



##### 1. Установка GitFlow и проверяем версию
> brew install git-flow-avh

> git flow version

##### 2. Инициализируем GitFlow для нашего проекта 
> git flow init

##### 3. Начало работы с новой веткой для функции
> git flow feature start improving_skills

<img width="566" alt="Снимок экрана 2024-12-27 в 16 46 52" src="https://github.com/user-attachments/assets/9baba076-269d-4049-befb-183cc1225b11" />


##### 4. Вносим изменения в файл improve_skill.py и коммитим их
> git add improve_skill.py

> git commit -m "Изменен файл improve_skill.py"

<img width="569" alt="Снимок экрана 2024-12-27 в 16 55 07" src="https://github.com/user-attachments/assets/b586b290-98d8-435b-8893-5bb7e42dc093" />


##### 5. Завершаем работу над новой функциональностью

> git flow feature finish improving_skills

<img width="608" alt="Снимок экрана 2024-12-27 в 16 58 33" src="https://github.com/user-attachments/assets/df3b863b-27e0-47de-9b3c-0556dfdc3ed6" />


##### 6. Начинаем создание релиза

> git checkout develop

> git flow release start v2.0.0

> echo "v2.0.0" > version.txt
git add version.txt
git commit -m "Обновление версии для релиза v2.0.0"

>git flow release finish v2.0.0

##### 7. Сохраняем изменения
> git flow hotfix start hotfix-2.0.1

<img width="560" alt="Снимок экрана 2024-12-27 в 17 27 25" src="https://github.com/user-attachments/assets/e59e8b4a-1914-4286-9003-b9eb4101ef66" />


> git add improve_skill.py
git commit -m "Исправление ошибки в логике программы"

> git flow hotfix finish hotfix-2.0.1

##### 8. Отправляем изменения

> git push origin main

> git push origin develop

> git push origin --tags

#
### Вывод:
В данной лабораторной работе получилось создать bash-скрипт для проверки текстовых файлов на наличие текста в них, а также поработать с GitFlow.
