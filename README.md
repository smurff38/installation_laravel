
# Создание проекта Laravel 

## Файлы
 - [PHP, Composer](https://cloud.mail.ru/public/5Fpz/Rzw7QZdr3)
___

## Установка PHP
После скачивания php и Composer нужно добавить php в переменные среды, для этого необходимо распаковать папку `php` на диск C: 

Затем нажимаем `Win + R` и вводим:
```bash
sysdm.cpl
```
 В открывшемся окне выбираем `Дополнительно`

![Дополнительно](https://i.ibb.co/n3R3Gcy/image.png)

Затем выбираем `Переменные среды`

![](https://i.ibb.co/rFV6tVk/image.png)

В открывшемся окне в `Системные переменные` ищем `Path` и нажимаем 2 раза ПКМ

![](https://i.ibb.co/7QcGkjL/image.png)

И прописываем полный путь где находиться папка `php`
```bash
C:\php
```
![](https://i.ibb.co/F5Lw3rc/image.png)
____

## Установка Composer
Запускаем установочный файл `Composer-Setup.exe` и следуем инструкции
___



## Создание проекта
Создаем папку для проекта в любом удобном месте и открываем её в `Visual Studio Code`
![](https://i.ibb.co/0hhqRzT/image.png)

После открытия VS Code необходимо открыть `терминал`

![](https://i.ibb.co/fdp47NV/image.png)

В терминале необходимо написать 
```bash
composer create-project laravel/laravel example-app
```
Где `example-app` - название вашего проекта

![](https://i.ibb.co/VJYMxhW/image.png)
![](https://i.ibb.co/44pLWtT/image.png)

После того как все компоненты будут скачаны у вас появиться папка вашего проекта 
![](https://i.ibb.co/LC7Wq95/image.png)

В терминале необходимо написать команду, для того что бы перейти в каталог с вашим проектом (в дальнейшем открыть в VS Code нужно будет созданную папку)
```bash
cd <название вашего проекта>
```
____
## Конфигурация Laravel
Для начала нужно открыть файл `.env` и настроить подключение к БД

ищем следующие строки, их нужно раскоментировать, а так же ввести данные для подключения
```bash
Исходный код

DB_CONNECTION=sqlite
# DB_HOST=127.0.0.1
# DB_PORT=3306
# DB_DATABASE=laravel
# DB_USERNAME=root
# DB_PASSWORD=
```

```bash
Отредактированный код для XAMPP

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=<название вашей БД>
DB_USERNAME=root
DB_PASSWORD=
```

После того, как отредактировали файл, можно сделать первую миграцию, для создания стандартныйх таблиц Laravel

Для этого необходимо в терминале написать команду 

```bash
php artisan migrate
```

После в терминале увидите состояние миграций

![](https://cdn.buttercms.com/JeiJPC2TRxOIUkEOICFJ)

Как миграция заверщиться можно выполнить команду для запуска веб-сервера
```bash
php artisan serve
```

![](https://i.ibb.co/xgg5Ck6/image.png)

Можно нажать на http://127.0.0.1:8000

Или в браузере перейти по адресу `localhost:8000`

Документация на русском языке доступна на странице Российского комьюнити
https://laravel.su/docs/11.x/installation
