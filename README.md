# Домашнее задание к занятию 3. «MySQL» - Сергей Ситкарёв

## Задача 1

Используя Docker, поднимите инстанс MySQL (версию 8). Данные БД сохраните в volume.

Изучите бэкап БД и восстановитесь из него.

![Задание1](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/1-1.jpg)

Перейдите в управляющую консоль mysql внутри контейнера.

Используя команду \h, получите список управляющих команд.

Найдите команду для выдачи статуса БД и приведите в ответе из её вывода версию сервера БД.

![Задание1](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/1-2.jpg)

Подключитесь к восстановленной БД и получите список таблиц из этой БД.

![Задание1](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/1-3.jpg)

Приведите в ответе количество записей с price > 300.

![Задание1](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/1-4.jpg)

В следующих заданиях мы будем продолжать работу с этим контейнером.

## Задача 2

Создайте пользователя test в БД c паролем test-pass, используя:

плагин авторизации mysql_native_password
срок истечения пароля — 180 дней
количество попыток авторизации — 3
максимальное количество запросов в час — 100
аттрибуты пользователя:
Фамилия "Pretty"
Имя "James".
Предоставьте привелегии пользователю test на операции SELECT базы test_db.

Используя таблицу INFORMATION_SCHEMA.USER_ATTRIBUTES, получите данные по пользователю test и приведите в ответе к задаче.

![Задание2](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/2.jpg)

## Задача 3

Установите профилирование SET profiling = 1. Изучите вывод профилирования команд SHOW PROFILES;.

![Задание3](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/3-1.jpg)

Исследуйте, какой engine используется в таблице БД test_db и приведите в ответе.

![Задание3](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/3-2.jpg)

Измените engine и приведите время выполнения и запрос на изменения из профайлера в ответе:

на MyISAM,
 
на InnoDB.

![Задание3](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/3-3.jpg)

## Задача 4

Изучите файл my.cnf в директории /etc/mysql.

Измените его согласно ТЗ (движок InnoDB):

скорость IO важнее сохранности данных;
нужна компрессия таблиц для экономии места на диске;
размер буффера с незакомиченными транзакциями 1 Мб;
буффер кеширования 30% от ОЗУ;
размер файла логов операций 100 Мб.
Приведите в ответе изменённый файл my.cnf.

![Задание4](https://github.com/SSitkarev/06-db-03-mysql/blob/main/img/4.jpg)