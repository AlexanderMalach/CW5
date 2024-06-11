## Проект "Парсинг вакансий от конкретных компаний в БД PostgreSQL"


Этот проект предназначен для сбора, хранения и анализа данных о вакансиях с использованием базы данных PostgreSQL. Он включает в себя создание базы данных, заполнение ее данными о вакансиях, а также возможность выполнения различных запросов к базе данных.

## Структура проекта

- `src/`
  - `config.py`: Модуль для чтения конфигурационных параметров для подключения к базе данных.
  - `db_manager.py`: Модуль для работы с базой данных PostgreSQL.
  - `get_vacancy.py`: Модуль для получения данных о вакансиях.
  - `utils.py`: Вспомогательные функции, включая создание базы данных и вставку данных.
- `main.py`: Главный файл проекта, в котором инициализируется база данных и запускается взаимодействие с пользователем.
- `tkinter.py`: Альтернативный файл проекта, в котором инициализируется база данных и запускается взаимодействие с пользователем.
- `database.ini`: Файл конфигурации, в который необходимо ввести данные для доступа к PostgreSQL.

## Установка

1. **Клонируйте репозиторий:**
     https://github.com/AlexanderMalach/CW5

2. **Создайте виртуальное окружение и активируйте его:**
    poetry init, 

    poetry install

3. **Настройте базу данных PostgreSQL:**
    Убедитесь, что PostgreSQL установлен и работает. Создайте базу данных для проекта.

4. **Настройте файл конфигурации database.ini:**
 [postgresql]
    host=localhost
    user=your_db_user
    password=your_db_password
    port=5432

Использование
Запуск проекта:

Для запуска проекта выполните:
    python main.py
или
    python tkinter.py

Интерактивное взаимодействие с main.py:

После запуска программы вам будет предложено выбрать один из доступных запросов:

1 - Список всех компаний и количество вакансий у каждой компании.
2 - Список всех вакансий с указанием названия компании, названия вакансии, зарплаты и ссылки на вакансию.
3 - Средняя зарплата по вакансиям.
4 - Список всех вакансий, у которых зарплата выше средней по всем вакансиям.
5 - Список всех вакансий, в названии которых содержится запрашиваемое слово.
стоп - Выход из программы.

Файлы
main.py
Главный файл проекта, который управляет взаимодействием с пользователем и выполняет основные функции.

tkinter.py
Альтернативный файл проекта, который управляет взаимодействием с пользователем и выполняет основные функции с помощью визуального интерфейса.
Обратите внимание из окон результатов можно копировать нажав кнопку "копировать"

db_manager.py
Класс DBManager содержит методы для работы с базой данных PostgreSQL, такие как получение списка компаний и количества вакансий, получение всех вакансий, вычисление средней зарплаты, получение вакансий с зарплатой выше средней и поиск вакансий по ключевому слову.

config.py
Модуль для чтения конфигурационных параметров для подключения к базе данных PostgreSQL.

get_vacancy.py
Модуль для получения данных о вакансиях с внешнего источника.

utils.py
Вспомогательные функции, включая создание базы данных и вставку данных о вакансиях.


Автор
Александр Малахинский