# Тестирование приложения с http интерфейсом

 * Реализовать простейший HTTP echo сервер
  * Обработка HTTP на сервере должна обеспечиваться не окружением (Djanga, rails), а Вашим приложением.
  * Для приложений на Java логично реализовать Ваше приложение в виде сервлета, работающего под управлением какого либо http контейнера, например, tomcat или jetty.
  * Для приложений на С++ Ваше приложение должно представлять собой CGI приложение.
  * Для языков, таких как Python, Ruby, Вы можете пользоваться Web сервером, например, Apache с соответствующими модулями, например, mod_passenger.
  * Тем не менее, Вы, разумеется, можете использовать библиотеки, которые обеспечат Вам обработку запросов, парсинг заголовков и тела и т.д.
 * Реализовать простейший HTTP клиент. Клиент должен обладать интерфейсом командной строки и поддерживать следующиее операции:
  * отправить заданное сообщение на сервер и убедиться, что оно вернулось правильно
  * отправить сообщение из файла и убедиться, что оно вернулось правильно
  * отправить сообщение заданного размера заполненного одним и тем же или случайными (из заданного множества) символами и убедиться, что оно вернулось правильно
  * отправить пустое сообщение и убедиться, что оно вернулось правильно
 * Придумать технологию тестирования сервера одним скриптом
  * Порт, на котором работает сервер должен выбираться случайно из диапазона \[40000; 65535\]
  * Клиент должен стартоваться после того, как стартован сервер
  * В конце работы необходимо корректно погасить сервер (но только свой! обратите внимание, что в системе могут работать другие аналогичные сервера)
 * Залить клиент и сервер в репозиторий
 * Реализовать тестирование Вашего сервера при помощи клиента
  * Сделать прогоны тестов на сборочном сервере
  * Сделать скрипт преобразования результатов прогона Ваших тестов в формат, понятный сборочному серверу, как модульные тесты
  * Примечания:
   * Для того, чтобы убедиться, что все работает корректно, Вам нужно будет внести какую нибудь ошибку в Ваш сервер, что бы увидеть, что тесты падают
   * Лог сервера должен прилагаться к тестовому логу, который будет отображаться в отчете сборочного сервера
