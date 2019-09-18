# Изучение Composer

Composer — это пакетный менеджер уровня приложений для языка программирования PHP
https://ru.wikipedia.org/wiki/Composer

Ссылка на скачивание https://getcomposer.org/

## ArchLinux

В ArchLinux Composer можно установить через pacman:
`pacman -Syu composer`

## Основы

Создаём файл `composer.json` с содержимым:
`{
    "require": {
        "monolog/monolog": "1.0.*"
    }
}`
затем выполняем команду `composer install`

Полученный `composer.lock` нужно добавить в репозиторий, а папки с библиотеками в `.gitignore`
