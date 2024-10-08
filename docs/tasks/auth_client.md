# Аутентификация клиента

## Задача

[UC-1 Аутентификация клиента](../req.md#uc1)

**`Задача 1.1:`** Реализация интерфейса аутентификации [Форма аутентификации](../uix.md#wf3)
<br>
**Описание задачи:** Разработать и интегрировать интерфейс аутентификации пользователя:

1. Добавить реквизит "Номер телефона" (тип - строка, ограничение - начало с "+7")
2. Добавить реквизит "Пароль" (тип - строка)
3. Добавить кнопку "Войти"

**`Задача 1.2:`** Реализация проверки номера телефона в базе данных программы лояльности
<br>
**Описание задачи:** При нажатии на кнопку "Войти" система должна проверять указанный номер на соответствие и проверять наличие номера телефона и пароля в базе данных. 
<br>
Если номер не найден, тогда выдавать ошибку "Номер не зарегистрирован в программе лояльности"
<br>
Если введен не соответствующий номер телефона, тогда выдавать ошибку "Некоретно введен номер телефона, повторите попытку"

**`Задача 1.3:`** Интеграция с компонентом программы лояльности
<br>
**Описание задачи:** Разработать бэкенд-логику для взаимодействия интерфейсса аутентификации с компоненотом программы лояльности. 




## Тест-кейсы

###  Основной сценарий

| Шаг | Описание шага                                               | Результат                                  |
|-----|-------------------------------------------------------------|--------------------------------------------|
| 1   | Открыть форму для аутентификации          | Клиент видит форму для аутентификации с полями (номер,пароль) |
| 2   | Ввод номера телефона (+7.......) и пароля в поля     | Клиент видит заполненные логин и пароль           |
| 3   | Нажать кнопку "Войти"                    | Клиент успешно аутентифицирован                               |

### Негативный сценарий

| Шаг | Описание шага                                    | Результат                                             |
|-----|--------------------------------------------------|-------------------------------------------------------|
| 1   | Открыть форму для аутентификации                 | Клиент видит форму для аутентификации                 |
| 2   | Ввод номера телефона (8.....) и пароля в поля    | Клиент видит заполненные логин и пароль               |
| 3   | Нажать кнопку "Войти"                            | Вывод ошибки, номер не зарегистрирован                |



**`Критерии приемки для UC1`**

1. Клиенты могут успешно аутентифицироваться, вводя свой номер телефона и пароль.
2. Интерфейс аутентификации отзывчив и загружает формы без задержек, а все поля ввода активны и доступны.
3. Все персональные данные передаются и хранятся в зашифрованном виде, обеспечивая конфиденциальность информации.

**`Критерии готовности для UC1`**

1. Интерфейс аутентификации клиента полностью реализован и интегрирован с основной системой.
2. Система аутентификации успешно интегрирована с базой данных для проверки уникальности номеров телефонов.
3. Все тест-кейсы выполнены, включая положительные и отрицательные сценарии, и успешно пройдены.
4. Все требования к безопасности и конфиденциальности выполнены, данные пользователей защищены.
