# Bash

<h2>Task 1</h2>
<table>
  <thead>
    <tr>
      <th>№</th>
      <th>Действие</th>
      <th>Команда</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>Открыть домашнюю директорию</td><td><code>cd ~</code></td></tr>
    <tr><td>2</td><td>Узнать имя текущей папки</td><td><code>pwd</code></td></tr>
    <tr><td>3</td><td>Создать каталог test1</td><td><code>mkdir test1</code></td></tr>
    <tr><td>4</td><td>Перейти в test1</td><td><code>cd test1</code></td></tr>
    <tr><td>5</td><td>Создать файлы 1, 2, 3</td><td><code>touch 1.txt 2.txt 3.txt</code></td></tr>
    <tr><td>6</td><td>Посмотреть содержимое папки</td><td><code>ls</code></td></tr>
    <tr><td>7</td><td>Вернуться в домашнюю директорию</td><td><code>cd ~</code></td></tr>
    <tr><td>8</td><td>Создать папку test2</td><td><code>mkdir test2</code></td></tr>
    <tr><td>9</td><td>Удалить папку test2</td><td><code>rmdir test2</code></td></tr>
    <tr><td>10</td><td>Удалить файл 2 из test1</td><td><code>rm ~/test1/2.txt</code></td></tr>
    <tr><td>11</td><td>Создать test3 и добавить 2 файла</td><td><code>mkdir test3 && touch test3/file4.txt test3/file5.txt</code></td></tr>
    <tr><td>12</td><td>Удалить папку test3</td><td><code>rm -r test3</code></td></tr>
    <tr><td>13</td><td>Создать test4</td><td><code>mkdir test4</code></td></tr>
    <tr><td>14</td><td>Переместить файлы 1 и 3 в test4</td><td><code>mv test1/1.txt test1/3.txt test4/</code></td></tr>
    <tr><td>15</td><td>Добавить 3 строки в файл 1</td><td><code>echo -e "line1\nline2\nline3" > test4/1.txt</code></td></tr>
    <tr><td>16</td><td>Посмотреть содержимое файла 1</td><td><code>cat test4/1.txt</code></td></tr>
    <tr><td>17</td><td>Добавить 3 строки в файл 3</td><td><code>echo -e "line31\nline32\nline33" > test4/3.txt</code></td></tr>
    <tr><td>18</td><td>Просмотреть содержимое 1 и 3 одновременно</td><td><code>cat test4/1.txt test4/3.txt</code></td></tr>
    <tr><td>19</td><td>Заменить все строки в файле 1</td><td><code>nano test4/1.txt</code> *(заменить вручную)*</td></tr>
  </tbody>
</table>

<h2>Task 2</h2>
<table>
  <thead>
    <tr>
      <th>№</th>
      <th>Действие</th>
      <th>Команда</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>Создать папку test3</td><td><code>mkdir test3</code></td></tr>
    <tr><td>2</td><td>Добавить в неё файлы 4–6 с 4 строками</td><td><code>echo -e "row1\nrow2\nrow3\nrow4" > file4.txt
echo -e "row1\nrow2\nrow3\nrow4" > file5.txt
echo -e "row1\nrow2\nrow3\nrow4" > file6.txt</code></td></tr>
    <tr><td>3</td><td>Найти строку row2 в файле 5</td><td><code>grep "row2" test3/5.txt</code></td></tr>
    <tr><td>4</td><td>Найти строку row во всех файлах</td><td><code>grep "row" test3/*</code></td></tr>
    <tr><td>5</td><td>Посчитать строки "row" в файле 6</td><td><code>grep -c "row" test3/6.txt</code></td></tr>
    <tr><td>6</td><td>Найти файл 5 внутри test3</td><td><code>find test3 -name "5.txt"</code></td></tr>
    <tr><td>7</td><td>Удалить файл 5 через find</td><td><code>find test3 -name "5.txt" -exec rm {} \;</code></td></tr>
    <tr><td>8</td><td>Добавить "test" в файл 4</td><td><code>echo "test" >> test3/4.txt</code></td></tr>
    <tr><td>9</td><td>Заменить "test" на "fail"</td><td><code>sed -i 's/test/fail/g' test3/4.txt</code></td></tr>
    <tr><td>10</td><td>Добавить "test" не удаляя содержимое</td><td><code>echo "test" >> test3/4.txt</code></td></tr>
    <tr><td>11</td><td>Просмотреть все процессы в системе</td><td><code>ps aux</code></td></tr>
    <tr><td>12</td><td>Убить процесс (пример)</td><td><code>pkill -f process_name</code></td></tr>
    <tr><td>13</td><td>Проверить доступность rusau.net</td><td><code>ping rusau.net</code></td></tr>
    <tr><td>14</td><td>Отправить 5 пакетов</td><td><code>ping -c 5 rusau.net</code></td></tr>
    <tr><td>15</td><td>GET-запрос к Swagger API</td><td><code>curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=available"</code></td></tr>
    <tr><td>16</td><td>POST-запрос на создание пользователя</td><td><code>curl -X POST "https://petstore.swagger.io/v2/user" -H "Content-Type: application/json" -d '{"id": 0, "username": "newuser", "firstName": "John", "lastName": "Doe", "email": "john@example.com", "password": "123456", "phone": "1234567890", "userStatus": 1}'</code></td></tr>
  </tbody>
</table>


# Task 3

**Описание:**  
Подборка bash-скриптов и практик для автоматизации повседневных задач QA-инженера: запуск API-тестов, логирование, curl-запросы, работа с логами и очисткой окружения.

---

<h3>Примеры скриптов</h3>

<table>
  <thead>
    <tr>
      <th>№</th>
      <th>Название</th>
      <th>Что делает</th>
      <th>Команда / Файл</th>
      <th>Описание</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Массовый запуск Postman-коллекций</td>
      <td>Цикличный запуск всех .json коллекций</td>
      <td><code>run_postman_collections.sh</code></td>
      <td>Обходит все коллекции в папке и запускает через <code>newman</code> с логированием результатов</td>
    </tr>
    <tr>
      <td>2</td>
      <td>curl-тест запроса</td>
      <td>Запрос на API с валидацией ответа</td>
      <td><code>test_login_api.sh</code></td>
      <td>curl + jq проверка кода ответа и поля <code>token</code> в JSON</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Очистка логов</td>
      <td>Удаление старых логов локально или на CI</td>
      <td><code>clear_logs.sh</code></td>
      <td>Удаляет все логи старше 7 дней в папке <code>/logs</code>, уведомляет в консоль</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Проверка доступности сервиса</td>
      <td>ping + проверка статус-кода</td>
      <td><code>check_service.sh</code></td>
      <td>Отправляет HEAD-запрос и проверяет, что код 200</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Запуск тестов в Docker-контейнере</td>
      <td>Запуск скрипта автотестов в изолированной среде</td>
      <td><code>run_tests_docker.sh</code></td>
      <td>Стартует Docker-контейнер, копирует в него тесты, запускает и выгружает отчёт</td>
    </tr>
  </tbody>
</table>

---

