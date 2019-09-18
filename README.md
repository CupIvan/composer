# Изучение Composer

Composer — это пакетный менеджер уровня приложений для языка программирования PHP
https://ru.wikipedia.org/wiki/Composer

Ссылка на скачивание https://getcomposer.org/

## ArchLinux

В ArchLinux Composer можно установить через pacman:
`pacman -Syu composer`

## Основы

Создаём файл `composer.json` с содержимым:
```json
{
    "require": {
        "monolog/monolog": "1.0.*"
    }
}
```
затем выполняем команду `composer install`

Полученный `composer.lock` нужно добавить в репозиторий, а папки с библиотеками в `.gitignore`

Подключить библиотеки достаточно просто:
```php
require __DIR__ . '/vendor/autoload.php';
$log = new Monolog\Logger('name');
```

Чтобы обновить библиотеки есть команда `composer update`, при этом также обновится файл `composer.lock`

## Библиотеки

Основной источник библиотек — сайт https://packagist.org

## Подключение библиотеки с github

```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/username/hello-world"
        }
    ],
    "require": {
        "acme/hello-world": "dev-master"
    }
}
```
