# <center>  Homework 1 </canter>

| Задание | Решение |
|---------|---------|
|1. Посмотреть где я|`pwd`|
|2. Создать папку|`mkdir` dir_1|
|3. Зайти в папку|`cd` dir_1/|
|4. Создать 3 папки|`mkdir` dir_1.1 dir_1.2 dir_1.3|
|5. Зайти в любоую папку|`cd` dir_1.2|
|6. Создать 5 файлов (3 txt, 2 json)|`touch` file_1.txt file_2.txt file_3.txt file_4.json file_5.json|
|7. Создать 3 папки|`mkdir` dir_1 dir_2 dir_3|
|8. Вывести список содержимого папки|`ls -al`|
|9. Открыть любой txt файл|`vim` file1.txt |
|10. Написать туда что-нибудь, любой текст.| Ввойти в режи редактировния нажатием на кнопку `i` и ввести текст|
|11. Сохранить и выйти.| Нажать комбинацию кнопок `esc` > `:` > `wq` > `enter`|
|12. Выйти из папки на уровень выше|`cd ..`|
|13. Переместить любые 2 файла, которые вы создали, в любую другую папку.|`mv` file_1.txt file_4.json /d/Testing/Vadim\'s\ QA\ course/Terminal_Git/dir_1|
|14. Скопировать любые 2 файла, которые вы создали, в любую другую папок|`cp` file_2.txt file_5.json /d/Testing/Vadim\'s\ QA\ course/Terminal_Git/dir_1|
|15. Найти файл по имени|`find ./ -name` file_3.txt|
|16. Просмотреть содержимое в реальном времени (команда grep) изучите как она работает.|`tail -f` ~/AppData/Local/Temp/|
|17. Вывести несколько первых строк из текстового файла|`head -n 3` ~/AppData/Local/Temp/|
|18. Вывести несколько последних строк из текстового файла|`tail -n 3` ~/AppData/Local/Temp/|
|19. Просмотреть содержимое длинного файла (команда less) изучите как она работает.|`less` ~/AppData/Local/Temp/|
|20. Вывести дату и время|`date`|
|21. Отправить http запрос на сервер.|`cURL` http://162.55.220.72:5005/terminal-hw-request|

# <center> Script </center>

 > Написать скрипт который зайдет в папку, создаст там 3 папки, зайдет в любую из новосозданных папок, создаст в ней 5 файлов (3 txt, 2 json), создаст 3 папки, выведет список содержимого папки, переместит 2 созданных файла в другую папку и выведет содержимое папки после перемещения файлов.

    #!/bin/bash  
    #  
    echo 'First script'
    echo '------------'
    echo 'Go to the directory'
    cd Script
    echo 'Create 3 folders'
    mkdir folder1 folder2 folder3
    echo 'Folders are created'
    echo 'Go to the second folder'
    cd folder2
    echo 'Folder is opened'
    echo 'Create 5 files (3 txt, 2 json)'
    touch f1.txt f2.txt f3.txt f4.json f5.json
    echo 'Files are created'
    echo 'Create 3 folders'
    mkdir folder1 folder2 folder3
    echo 'Folders are created'
    echo 'Display content list before moving'
    ls -al
    echo 'Content list is displayed'
    echo 'Move any 2 files'
    mv f1.txt f5.json /d/Testing/Folders_from_script
    echo 'File are moved'
    echo 'Display content list after moving'
    ls -al
    echo 'Content list is displayed'