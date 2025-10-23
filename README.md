# Домашнее задание к занятию «Работа с данными (DDL/DML)» Волкивский Андрей

Задание можно выполнить как в любом IDE, так и в командной строке.

Задание 1

1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

<img width="1724" height="465" alt="image" src="https://github.com/user-attachments/assets/0faec9e1-d602-44ed-baa1-53ac6a52fdfa" />

1.2. Создайте учётную запись sys_temp.

<img width="887" height="315" alt="image" src="https://github.com/user-attachments/assets/f39aecfe-73c7-4589-8e9b-b382c3f91be1" />

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

<img width="495" height="245" alt="image" src="https://github.com/user-attachments/assets/040da4ae-72aa-453a-87c8-d2a71e150e2a" />

1.4. Дайте все права для пользователя sys_temp.

mysql> GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost';

mysql> FLUSH PRIVILEGES;

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

<img width="1770" height="713" alt="image" src="https://github.com/user-attachments/assets/c33e2084-49bb-4b85-a1a8-cb27d66d9483" />

1.6. Переподключитесь к базе данных от имени sys_temp.

<img width="846" height="401" alt="image" src="https://github.com/user-attachments/assets/7e1e53bd-efd2-4606-a4dd-cfa90038dabf" />

Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

<img width="1011" height="185" alt="image" src="https://github.com/user-attachments/assets/96ef0c50-c83e-479f-bafe-53721e4b07e1" />

1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

<img width="1447" height="294" alt="image" src="https://github.com/user-attachments/assets/d54dda75-bb3d-49d4-98c2-b82cc78a2981" />

распаковываем архив: unzip sakila-db.zip

1.7. Восстановите дамп в базу данных.

mysql> SOURCE /home/andreyvolk/sakila-db/sakila-schema.sql

mysql> SOURCE /home/andreyvolk/sakila-db/sakila-data.sql

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

<img width="947" height="861" alt="image" src="https://github.com/user-attachments/assets/2621bfab-c5b8-4517-a010-43448f95fdce" />

Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

Задание 2

Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id

<img width="826" height="706" alt="image" src="https://github.com/user-attachments/assets/e99a26cb-7aeb-42ee-bb60-ec72e99e3ebc" />
