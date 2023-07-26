<h1>План автоматизации тестирования функционала "Запись на обучение профессии 'Тестировщик ПО'".</h1>

<h2>Перечень автоматизируемых сценариев:</h2>
 
 1.1. Навигация к форме записи:

* Переход на страницу с профессией "Тестировщик ПО" через меню "Каталог курсов".

* Переход на страницу с профессией "Тестировщик ПО" через контент на главной странице

* Пролистывание страницы профессии "Тестировщик ПО" до формы записи.

* Нажатие на кнопку "Записаться" на странице профессии.

* Нажатие на другую кнопку "Записаться" на странице профессии.

1.2. Сценарии заполнения и отправки формы:

***Позитивные сценарии:***

- Ввод валидных данных во все обязательные поля формы, например:
  
- Имя: "Иван"
 
- Фамилия: "Иванов"
  
- Email: "ivanov@example.com"
  
- Телефон: "+79999999999"
  
- Отправка заполненной формы.
  
   Ожидаемый результат: Форма успешно отправляется, и пользователь перенаправляется на страницу подтверждения или получает уведомление об успешной записи на курс.

 ***Негативные сценарии:***

1. Отправка формы с пустыми обязательными полями :

- Оставить поля имя, телефон, email формы пустыми.

- Нажатие на кнопку "Отправить".

   Ожидаемый результат: Появляется сообщение об ошибке, указывающее на необходимость заполнения всех обязательных полей.

2. Ввод некорректного email:

- Ввести некорректный email, например: "ivanov.example.com" или "ivanov@"

- Заполнение остальных полей формы валидными данными.

- Нажатие на кнопку "Отправить".

  Ожидаемый результат: Появляется сообщение об ошибке, указывающее на некорректный формат email.

3. Ввод некорректного телефона:

- Ввести некорректный телефон, например: "123456" или "invalidphone"

- Заполнение остальных полей формы валидными данными.

- Нажатие на кнопку "Отправить".

  Ожидаемый результат: Появляется сообщение об ошибке, указывающее на некорректный формат телефона.

4. Ввод недопустимых символов в поля:

- Ввести недопустимые символы, например: "<>&$%" в поле имя, телефон или email.

- Заполнение остальных полей формы валидными данными.

- Нажатие на кнопку "Отправить".

   Ожидаемый результат: Появляется сообщение об ошибке, указывающее на недопустимые символы в поле.

5. Отправка формы с уже зарегистрированным email:

- Ввод валидного email, который уже зарегистрирован в системе.

- Заполнение остальных полей формы валидными данными.

- Нажатие на кнопку "Отправить".

   Ожидаемый результат: Появляется сообщение об ошибке, указывающее на уже существующий email в системе.

6. Ввод слишком длинных значений в поля:

- Ввод очень длинных значений (более 100 символов) в одно или несколько полей формы.

- Заполнение остальных полей формы валидными данными.

- Нажатие на кнопку "Отправить".

   Ожидаемый результат: Появляется сообщение об ошибке, указывающее на превышение допустимой длины данных в поле.


<h2>Перечень используемых инструментов с обоснованием выбора:</h2>

 ***2.1. Selenium, Selenide:***

* Selenium и Selenide обеспечивают удобный и мощный интерфейс для взаимодействия с веб-элементами.

* Широкая поддержка различных браузеров.

* Легко интегрируются с Java.

***2.2. TestNG, JUnit:***

* TestNG и JUnit предоставляют возможности для структурирования и запуска тестовых сценариев.

* Удобное создание тестовых групп и настройка их выполнения.

* Хорошая интеграция с Maven и другими инструментами сборки проекта.

***2.3. JMeter:***

* JMeter используется для нагрузочного тестирования и проверки производительности сайта.

* Позволяет смоделировать большое количество одновременных запросов и проверить, как сайт справляется с нагрузкой.

***2.4. Cucumber:***

* Cucumber позволяет создавать и запускать тесты в стиле Behavior-Driven Development (BDD).

* Удобное описание сценариев на естественном языке, что улучшает понимание сценариев всеми членами команды.

***2.5. DevTools:***

* DevTools позволяет анализировать работу страницы, проверять сетевые запросы и элементы страницы.

* Удобный инструмент для отладки и проверки работы интерфейса сайта.

<h2>Перечень необходимых разрешений, данных и доступов:</h2>

   ***3.1. Доступ к исходному коду сайта для интеграции автоматизированных тестов.***
   
   * Для интеграции автоматизированных тестов с исходным кодом сайта и поиска элементов.
   
   ***3.2. Разрешения на использование автоматизации тестирования на сайте.***
   
   * Чтобы не нарушать политику сайта и не создавать нагрузку на сервер без разрешения.
   
   ***3.3. Доступы к базе данных и API сайта:***

* Доступ к базе данных позволит проверить сохранение данных после заполнения формы и выполнения других действий на сайте.

* Доступ к API сайта позволит тестировать взаимодействие с другими сервисами и проверить корректность обмена данными.

<h2>Перечень и описание возможных рисков при автоматизации:</h2>

   * Большие неоправданные затраты
   
   * Изменение структуры сайта: Если сайт будет переработан, локаторы элементов могут измениться, что повлияет на стабильность тестов.
   
   * Обновления платформы: Новые версии браузеров, операционных систем,могут повлиять на работу тестов.
   
   * Недоступность сервера: Если сервер тестируемого сайта недоступен, то тесты не смогут быть выполнены.


<h2>Перечень необходимых специалистов для автоматизации:</h2>
 
  ***5.1. QA-инженер: Ответственный за разработку автоматизированных тестов и их выполнение.***
   

# Интервальная оценка с учётом рисков в часах:

   Указание точной оценки сложно без непосредственного опыта с сайтом и тестовыми сценариями. Оценка времени будет зависеть от объема тестируемого контента и сложности автоматизируемых сценариев. В общем случае, планирование и написание тестовых сценариев может занять от 30 до 60 часов, а учет рисков и отладка еще 10-20 часов.
