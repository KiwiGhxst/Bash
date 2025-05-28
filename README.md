# 🖥️ Bash

## 📌 Описание

Этот раздел демонстрирует, как я использую Bash в macOS для автоматизации повседневных задач QA-инженера: от работы с файлами и логами до API-запросов и мониторинга.  
Все команды протестированы и адаптированы под macOS (zsh / bash), включая поддержку `grep`, `sed`, `find`, `curl` и других системных утилит.

---

<h2>Task 1: Работа с файловой системой</h2>

<table>
  <thead>
    <tr><th>№</th><th>Действие</th><th>Команда</th></tr>
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
    <tr><td>11</td><td>Создать test3 и добавить 2 файла</td><td><code>mkdir test3 &amp;&amp; touch test3/file4.txt test3/file5.txt</code></td></tr>
    <tr><td>12</td><td>Удалить папку test3</td><td><code>rm -r test3</code></td></tr>
    <tr><td>13</td><td>Создать test4</td><td><code>mkdir test4</code></td></tr>
    <tr><td>14</td><td>Переместить файлы 1 и 3 в test4</td><td><code>mv test1/1.txt test1/3.txt test4/</code></td></tr>
    <tr><td>15</td><td>Добавить 3 строки в файл 1</td><td><code>echo -e "line1\nline2\nline3" &gt; test4/1.txt</code></td></tr>
    <tr><td>16</td><td>Посмотреть содержимое файла 1</td><td><code>cat test4/1.txt</code></td></tr>
    <tr><td>17</td><td>Добавить 3 строки в файл 3</td><td><code>echo -e "line31\nline32\nline33" &gt; test4/3.txt</code></td></tr>
    <tr><td>18</td><td>Просмотреть содержимое 1 и 3 одновременно</td><td><code>cat test4/1.txt test4/3.txt</code></td></tr>
    <tr><td>19</td><td>Заменить строки в файле вручную</td><td><code>nano test4/1.txt</code></td></tr>
  </tbody>
</table>

---

<h2>Task 2: grep, find, curl и процессы</h2>

<table>
  <thead>
    <tr><th>№</th><th>Действие</th><th>Команда</th></tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>Создать папку test3</td><td><code>mkdir test3</code></td></tr>
    <tr><td>2</td><td>Создать файлы 4–6 с 4 строками</td><td><code>echo -e "row1\nrow2\nrow3\nrow4" > file4.txt
echo -e "row1\nrow2\nrow3\nrow4" > file5.txt
echo -e "row1\nrow2\nrow3\nrow4" > file6.txt</code></td></tr>
    <tr><td>3</td><td>Найти строку row2 в файле 5</td><td><code>grep "row2" test3/5.txt</code></td></tr>
    <tr><td>4</td><td>Найти строку row во всех файлах</td><td><code>grep "row" test3/*</code></td></tr>
    <tr><td>5</td><td>Посчитать количество "row" в файле</td><td><code>grep -c "row" test3/6.txt</code></td></tr>
    <tr><td>6</td><td>Найти файл 5 внутри test3</td><td><code>find test3 -name "5.txt"</code></td></tr>
    <tr><td>7</td><td>Удалить файл через find</td><td><code>find test3 -name "5.txt" -exec rm {} \;</code></td></tr>
    <tr><td>8</td><td>Добавить слово test в файл 4</td><td><code>echo "test" &gt;&gt; test3/4.txt</code></td></tr>
    <tr><td>9</td><td>Заменить "test" на "fail"</td><td><code>sed -i '' 's/test/fail/g' test3/4.txt</code></td></tr>
    <tr><td>10</td><td>Снова добавить "test"</td><td><code>echo "test" &gt;&gt; test3/4.txt</code></td></tr>
    <tr><td>11</td><td>Посмотреть процессы</td><td><code>ps aux</code></td></tr>
    <tr><td>12</td><td>Завершить процесс</td><td><code>pkill -f название процесса</code></td></tr>
    <tr><td>13</td><td>Проверить ping сайта</td><td><code>ping rusau.net</code></td></tr>
    <tr><td>14</td><td>Отправить 5 пакетов</td><td><code>ping -c 5 rusau.net</code></td></tr>
    <tr><td>15</td><td>GET-запрос к Swagger API</td><td><code>curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=available"</code></td></tr>
    <tr><td>16</td><td>POST-запрос: создать пользователя</td><td><code>curl -X POST "https://petstore.swagger.io/v2/user" -H "Content-Type: application/json" -d '{"id": 0, "username": "newuser", "firstName": "John", "lastName": "Doe", "email": "john@example.com", "password": "123456", "phone": "1234567890", "userStatus": 1}</code></td></tr>
  </tbody>
</table>

---

<h2>Task 3: Bash-скрипты для автоматизации</h2>

<table>
  <thead>
    <tr><th>№</th><th>Название</th><th>Что делает</th><th>Файл</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>1</td><td>Массовый запуск коллекций</td><td>Цикличный newman по .json</td><td><code>run_postman_collections.sh</code></td><td>Находит и запускает все коллекции Postman</td></tr>
    <tr><td>2</td><td>Проверка API авторизации</td><td>curl-запрос + валидация JSON</td><td><code>test_login_api.sh</code></td><td>Проверка наличия <code>token</code> через <code>jq</code></td></tr>
    <tr><td>3</td><td>Очистка логов</td><td>Удаляет старые файлы</td><td><code>clear_logs.sh</code></td><td>Удаление логов старше 7 дней в каталоге <code>/logs</code></td></tr>
    <tr><td>4</td><td>Проверка доступности сайта</td><td>HEAD-запрос + статус</td><td><code>check_service.sh</code></td><td>Проверяет, что HTTP 200</td></tr>
  </tbody>
</table>
