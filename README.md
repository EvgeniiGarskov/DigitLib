# Библиотечная система учета книг

## Описание проекта

Этот проект представляет собой веб-приложение для цифрового учета книг в местной библиотеке. Библиотекари могут легко управлять читателями и книгами, а также отслеживать выдачу и возврат книг.

## Функционал

В приложении реализованы следующие функции:

1. **Управление читателями**:
    - Страницы для добавления, изменения и удаления данных о читателе.
    
2. **Управление книгами**:
    - Страницы для добавления, изменения и удаления данных о книге.
    
3. **Список читателей**:
    - Страница с полным списком всех читателей (каждый читатель кликабельный, переход на страницу читателя).

    <details>
    [![Index People][1]][1]
    [1]: (https://github.com/user-attachments/assets/e7e5fc70-824f-4914-9a6c-62dbcd7c1eef)
    </details>
    
4. **Список книг**:
    - Страница с полным списком всех книг (каждая книга кликабельная, переход на страницу книги).
   
    ![Index Books](https://github.com/user-attachments/assets/224f82f4-7a92-49e3-9949-bfaed3405597)
    
5. **Страница читателя**:
    - Отображает данные читателя и список книг, которые он взял. Если книги отсутствуют, выводится сообщение: "Человек пока не взял ни одной книги".
   
    ![Show people](https://github.com/user-attachments/assets/8a70a8fc-ec7c-474c-a646-e9b680804a32)

6. **Страница книги**:
    - Показывает данные книги и имя читателя, который ее взял. Если книга свободна, отображается сообщение: "Эта книга свободна".
   
    ![Show book](https://github.com/user-attachments/assets/60d987e4-12e6-4f66-8482-bd5c930e7bb8)
    
7. **Освобождение книги**:
    - Если книга взята, рядом с именем читателя кнопка "Освободить книгу". Библиотекарь использует эту кнопку, чтобы вернуть книгу в библиотеку.
    
8. **Назначение книги**:
    - Если книга свободна, предоставляется выпадающий список с читателями и кнопка "Назначить книгу". После нажатия на кнопку книга назначается выбранному читателю.
   
    ![Show book2](https://github.com/user-attachments/assets/408edfb8-5825-4ae8-ac25-5a4302a5693b)

## Технологии

- Java
- Spring MVC
- JdbcTemplate
- HTML/Thymeleaf
- Maven
- PostgreSQL

## Установка и запуск в IntelliJ IDEA
1. **Клонируйте репозиторий:**
    - Клонируйте репозиторий: git clone https://github.com/EvgeniiGarskov/DigitLib.git
  
2. **Откройте проект в IntelliJ IDEA:**
    - Запустите IntelliJ IDEA.
    - Выберите "Open" (Открыть) и укажите путь к папке, в которую вы клонировали репозиторий.
  
3. **Импортируйте проект как Maven:**
    - В панели проекта (Project) найдите файл pom.xml, нажмите на него правой кнопкой мыши и выберите Maven > Reload Project для загрузки всех необходимых зависимостей.
    - Дождитесь завершения импорта зависимостей.
  
4. **Создание базы данных:**
    - В данном проекте используется СУБД PostgreSQL. Код для создания таблиц находится в файле sql/project1.sql.

5. **Установите плагин Smart Tomcat:**
    - Перейдите в "File" -> "Settings" -> "Plugins".
    - Найдите "Smart Tomcat" и установите его, если он еще не установлен.
    - Перезапустите IntelliJ IDEA, если это необходимо.

6. **Настройте Smart Tomcat:**
    - После установки плагина, откройте "File" -> "Settings" -> "Tomcat Server".
    - Нажмите на иконку "+" для добавления нового сервера.
    - Укажите путь к установленному Tomcat.

7. **Добавьте проект в Smart Tomcat:**
    - Перейдите в "Run" -> "Edit Configurations".
    - Нажмите на иконку "+" для добавления новой конфигурации Smart Tomcat.
    ![Tomcat Configuration](https://github.com/user-attachments/assets/0b4fa030-ec6a-4d3b-bbb5-c5ffc0320535)

  
8. **Запустите сервер Tomcat:**
    - Нажмите на кнопку "Run" (Запуск) в правом верхнем углу или используйте сочетание клавиш Shift + F10.
    - Откройте браузер и перейдите по адресам: http://localhost:8080/people и http://localhost:8080/books.
