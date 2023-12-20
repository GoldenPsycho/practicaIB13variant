# Practiсe

## Вариант 13

### Состав команды:
* Гиоев Георгий Давидович
* Иманаев Данила Иванович
* Богатова Екатерина Руслановна
* Алексеев Дмитрий Игоревич

### Обязанности каждого участника в группе:
* Гиоев Георгий - описание проекта, построение схемы взаимодействия компонентов системы и поднятие ИС; -- Выполнено
* Иманаев Данила - работа с БДУ ФСТЭК, построение модели нарушителя ИБ; -- Выполнено
* Богатова Екатерина - разработка сценариев с матрицей Mitre ATT&CK; -- Выполнено
* Алексеев Дмитрий - работа с БДУ ФСТЭК, построение модели угроз. -- Выполнено

### Описание проекта:

#### Структурные элементы проекта:

1. Сервера системного программного обеспечения (СПО):
* Веб-сервер (Apache) - отвечает за обработку запросов и предоставление веб-страниц пользователю.
* Базы данных Microsoft SQL Server (MSSQL) - хранят информацию о блоге, пользователях, комментариях и других данных.
* Веб-браузеры - позволяют пользователям просматривать и взаимодействовать с блогом.

2. Приложения:

* Bitwarden - менеджер паролей с открытым кодом, который имеет приложения нескольких форматов, включая веб-интерфейс, настольные приложения, расширение браузера, мобильные приложения и CLI.
Bitwarden использует облачный сервис, а также возможность развёртывания решения локально.

3. СУБД (Система управления базами данных):

* Bitwarden работает с системой управления реляционными базами данных Microsoft SQL Server (MSSQL).
#### Взаимодействие структурных элементов:

### Описание проекта:

### Описание места установки системы:
MacOS server во внутренней сети, в офисе дизайнерской студии.

### Решаемые задачи:
	Управление учётными записями и доступом к удалённым хранилищам: Bitwarden — менеджер паролей с открытым кодом. Имеет приложения нескольких форматов, включая веб-интерфейс, настольные приложения, расширение браузера, мобильные приложения и CLI. Bitwarden использует облачный сервис, а также возможность развёртывания решения локально.

### Роли пользователей и варианты доступа:
	Администратор сервера:  Развёртывает локальный (офисный) сервер во внутренней сети компании и контролирует его работоспособность. Самый высокий уровень доступа
	Пользователи: самый низкий уровень доступа. Подключение из внутренней сети к веб интерфейсу.

### Структурные элементы системы:
	Сервера системного программного обеспечения (СПО):
	сервер (MAC OS) - отвечает за работоспособность развёрнутого на нём Docker контейнера .
	Docker — развёрнутый контейнер приложения
	Базы данных (MySQL/ SQLite) - хранит хэш паролей.
	Веб-браузеры - позволяют пользователям просматривать и взаимодействовать с приложением.

### Взаимодействие структурных элементов:
	Когда пользователь заходит через браузер на ip развернутого в докере приложения.
	Регистрация или авторизация в приложении. 
	Запрос в бд и ответ согласно роли и правам . Возвращение ответа пользователю в виде веб-страницы.
