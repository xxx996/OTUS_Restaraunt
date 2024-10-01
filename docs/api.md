# API Интеграция

## Описание endpoint

| Метод | Endpoint                      |  Описание            |
|-------|-------------------------------|---------------------|
|GET| **/order/{orderID}/status**       |  Получение статуса по заказу. |
|GET| **/сart**                         |  Получение сформированной корзины. |
|GET| **/users/{userID}/orders**        |  Получение истории заказов. |
|GET| **/orders/{orderID}**             |  Получение информации по заказу. |
|PUT| **/orders/{orderID}**             |  Обновление информации по заказу. |
|DELETE| **/orders/{orderID}**          |  Удаление заказа. |
|GET| **/reviews**                      |  Получение списка отзывов. |
|POST| **/orders/{orderID}/reviews**    |  Добавление отзыва о заказе. |
|GET| **/reviews/{reviewsID}**          |  Получение конкретного отзыва. |
|GET| **/menu**                         |  Получение текущего меню. |
|GET| **/menu/category**                |  Получение категорий. |
|POST| **/menu/category**               |  Добавление новой категории. |
|GET| **/menu/category/dish/{dishID}**  |  Получение конкретного блюда из выбранной категории. |
|POST| **/menu/category/dish**          |  Добавление нового блюда. |
|POST| **/users/login**                 |  Аутентификация клиента. |
|POST| **/users/register**              |  Регистрация клиента. |
|GET| **/users/{UserID}**               |  Получение информации о профиле клиента. |
|POST| **/recovery**                    |  Восстановление пароля. |

## Swagger

<swagger-ui src="https://raw.githubusercontent.com/xxx996/OTUS_Restaraunt/main/docs/assets/swagger.yaml" />



