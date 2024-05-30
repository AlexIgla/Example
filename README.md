Пояснительная записка

Автоматизированное тестирование UI сайта: https://b2c.passport.rt.ru/

Про технику тест-дизайна:

Выполнялось позитивное и негативное тестирование при помощи следующих техник:
разделение на классы эквивалентности и анализ граничных значений - при регистрации пользователя пароль и данные ограничиваются видом и количеством символов;
предугадывание ошибки - предугадываем ошибку и выполняем тестирование с заведомо неверными вводными данными.
Выбрал эти техники, т.к пользователи часто ошибаются при вводе данных и необходимо проверить поведение сайта при вводе верных и неверных данных. 
Сможет ли пользователь успешно произвести вход в систему или авторизоваться без посторонней помощи - задача моего тестирования.


Инструменты:

1. Google-таблицы;
2. Среда программирования PyCharm последней версии;
3. Интерпретатор Python 3.12; 
4. Библиотеки - selenium 4.9.0, pytest-selenium 4.0.0, pytest 6.2.5; 
5. Браузер Google Chrome 114.0.5735.199;
6. Драйвер ChromeDriver 114.0.5735.90.

Багов не обнаружено.
Три потенциально  возможных дефекта - не отправляется код восстановления пароля, нечитаемая капча, отсутствие нужного региона на странице регистрации.
С тест-кейсами можно ознакомиться по ссылке: https://docs.google.com/spreadsheets/d/1JvrkekYm-PMxkd0aQb3cd77HIu412sDE/edit?usp=sharing&ouid=113009641680443339722&rtpof=true&sd=true
В папке pages в файле main_page.py находится конструктор webdriver и общие для всех тестируемых страниц методы.
В папке pages в файлах main_page.py, recovery_page.py, passwordrecovery_page.py, registration_page.py находятся методы для соответствующих тестируемых страниц.
В папке pages в файле locators.py находятся все локаторы.
В корне проекта в файле conftest.py находится фикстура с функцией открытия и закрытия браузера. Для запуска тестов необходимо поменять путь до webdriver на свой.
В корне проекта в файлах test_main_page.py, test_recovery_page.py, test_passwordrecovery_page.py, test_registration_page.py находятся тесты. Все тесты идут по порядку в соответствии с номерами тест-кейсов. Во всех файлах с тестами находятся закомментированные команды для запуска тестов из командной строки (# pytest -v --tb=line test_main_page.py)


Данные для регистрации/автоизации
почта - sanchez.ig.94@mail.ru
телефон - 8-951-888-00-11
логин - rtkid_1716278020835
пароль - AzwX1223
