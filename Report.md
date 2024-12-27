#
## Цель работы:
Используя навыки работы с Git и ветками, создать скрипт на языке Bash, который будет проверять наличие текста в текстовом файле перед коммитом (Задание 1) и поработать с моделью ветвления GitFlow (Задание 2).

## Ход работы:
### Задание 1
#### 1. Переходим в GitHooks и создаем bash-скрипт
> cd .git/hooks

> touch pre-commit_git.bash

![alt text](<Снимок экрана 2024-12-27 в 13.02.54.png>
#### 2. Создаем файл "pre-commit" и добавляем в него код скрипта
>   touch pre-commit
>   nano pre-commit

![alt text](<Снимок экрана 2024-12-27 в 13.05.59.png>)

#### 3. Делаем данный файл исполняемым
>    chmod +x pre-commit

#### 4. Проверяем работу
##### Если файл пустой:
> touch test_empty_file_5.txt

> git add test_empty_file_5.txt

> git commit -m "Добавлен файл empty_file_test_5.txt"

![alt text](<Снимок экрана 2024-12-27 в 13.25.56.png>)

##### Если файл не пустой:
> touch test_file_6.txt

> open test_file_6.txt
