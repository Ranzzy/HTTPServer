# Лабораторная работа №7 Установка и настройка HTTP Server

**Цель работы:** провести установку и настройку HTTPServer и практиковаться в написании кода.

**Ход работы:**

Для первого примера (папка sample1) создать файлы:

a)    tasks.json – конфигурация для компиляции первого примера

Пример задачи компиляции:

    {
            "label": "sample1",
            "type": "shell",
            "command": "g++
             sample1/main.cpp -std=c++11 -levent
             -o sample1.exe",
            "group": {<
                "kind": "build",
                "isDefault": true
            }
    }

b)    launch.json – конфигурация для запуска веб-приложения

    {
            "name": "Запуск sample1",
            "type": "cppdbg",
            "request": "launch",
            "program": "${workspaceFolder}/main1",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": true,
            "MIMode": "gdb",
            "setupCommands": [
                {
                    "description": "Enable   pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ]
        },

Для задач sample2 и sample3 прописаны аналогичные конфигурации в файлах tasks.json и launch.json.

**Вывод:** в данных кодах для компиляции были допущены ошибки, которые были исправлены. Для каждой задачи были прописаны инструкции сборки и запуска.