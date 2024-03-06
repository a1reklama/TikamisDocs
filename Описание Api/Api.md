## Краткое описание методов

## Раздел Customer
- POST `mobile-api/customer/ask-sms` - Запросить смс для входа. Подробнее описан [здесь](Авторизация.md)
- POST `mobile-api/customer/login` - Ввести код из смс и тем самым завершить аутентификацию, получив авторизационные токены. Подробнее описан [здесь](Авторизация.md) 
- POST `mobile-api/customer/refresh` - Обновить токены, если от API приходит ошибка **401 Unauthorized**. [здесь](Авторизация.md)
- GET `mobile-api/customer/user_agreement.html` - Страница с пользовательским сообщением.
- GET `mobile-api/customer/qr-code` - получить QR Код (вкладка отдельная)

## Раздел CarCenter
- GET `mobile-api/carcenter/get-cities` - Получить список городов. Нужно для выбора на этапе записи.
- GET `mobile-api/carcenter/{city}` - Получить список автосервисов, которые есть в определенном городе. Для этапа заказа.
- GET `mobile-api/carcenter/{centerId}` - Получить список работ по городу и ID автосервиса. Для этапа заказа.

## Раздел Cart
- POST `mobile-api/cart` - добавить работу в корзину для заказа.
- GET `mobile-api/cart` - получить корзину клиента.
- DELETE `mobile-api/cart/{id}` - удалить услугу из корзины клиента.

## Раздел Order
- GET `mobile-api/order/available-time/{centerId}` - Получить временные окна для записи на обслуживание.
- POST `mobile-api/order` - создать заказ. 
- GET `mobile-api/order` - Получить **предстоящие** заказы.
- POST `mobile-api/order/get-history` - получить **сервисную историю**.
- DELETE `mobile-api/order` - отменить заказ.

## Раздел Work
- GET `mobile-api/work/all/{centerId}` - получить все услуги. Этот метод нужен для фильтрации

## Подробное описание методов

#### POST `-api/login`

Для директора и суперадмина интерфейс одинаковые.  
