# Тестирование https://lawyer.front.softwarecenter.ru/

# Задание №1. Составить чек-лист проверок раздела “Быстрые заметки” и его влияние на иные элементы системы.

Чек-лист по тестированию данного раздела сайта оформлен в Trello по ссылке: https://trello.com/invite/b/6864324dc11ade403f48f651/ATTI53fe1290ace6ae379f38a4945124898b7ACC8849/lawyerfront.

# Задание №2.Составить список запросов к API. 

Оформил HTTP запросы Postman, ниже приведена ссылка на workspace с
соответствующими запросами :
https://planetary-water-7036938.postman.co/workspace/lawyer~1749a781-b684-4fe4-9c91- 711bf57009f6/collection/44392157-e6a472b7-ab44-4bd1-839c- 4b62f48335f5?action=share&creator=44392157&active-environment=44392157-0042ed21- 63e5-4c35-86fb-b4a5efc7683a.


# Задание №3. Что нужно для тестирования API.

1. Адрес API базовый URL сайта. Предоставляется разработчиком.
2. Авторизация - токен (Bearer) или логин/пароль/SMS. Предоставляется разработчиком, или самостоятельная регистрация.
3. Ссылка на Swagger с API docs, которые уже есть для данного продукта или экспорт JSON
из Postman от коллег, которые уже работали над этим проектом ранее. Получается из
рабочей документации.
4. Как данные API производит авторизацию. Из документации или методом Try&Errors.
5. Четкое понимание где именно на сайте можно вызвать данную функцию. Получить
можно при исследовательском тестировании или через документацию, например из
макетов (Figma).
6. Наименование метода HTTP запроса, тело, payload, код ответа. Получается через
Devtools, вкладка network. При использовании тестируемой фичи, обратить внимание на
появление нового запроса, скопировать Curl запроса и вставить в Postman для дальнейшей
работы с ним. 
7. Текстовые значения - валидные, невалидные, что предполагается, что пользователь
будет менять своими действиями, которые мы отправляем сразу в виде запроса на сервер. 
8. Среда, в какой среде подразумевается использование этого приложения, windows/linux
или например mobile.


# Обнаруженный баг.

Самый основной баг, который есть у этого приложения - то, что можно отправлять запросы, получать информацию, редактировать информацию без необходимости в како-либо
авторизации. Это критический дефект безопасности. Ниже привожу ссылку на
документацию в Jira по этому багу:
https://test5011.atlassian.net/browse/LF- 1?atlOrigin=eyJpIjoiYzZjZDViNWU5YWE1NDNiNzkzNGNhMTU3NjM1MjUzNWUiLCJwIjoiaiJ9



