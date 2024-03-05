## Краткое описание методов

## Раздел Customer
- POST `mobile-api/customer/ask-sms` - Запросить смс для входа. Подробнее описан [здесь](Авторизация.md)
- POST `mobile-api/customer/login` - Ввести код из смс и тем самым завершить аутентификацию, получив авторизационные токены. Подробнее описан [здесь](Авторизация.md) 
- POST `mobile-api/customer/refresh` - Обновить токены, если от API приходит ошибка **401 Unauthorized**. [здесь](Авторизация.md)
- GET `mobile-api/customer/user_agreement.html` - Страница с пользовательским сообщением.
- GET `mobile-api/customer/qr-code` - получить QR Код (вкладка отдельная)

## Раздел CarCenter
- GET `mobile-api/carcenter/get-cities` - Получить список городов. Нужно для выбора на этапе записи.
- GET `mobile-api/carcenter/{city}` - Получить список автосервисов, которые есть в определенном городе. 

## Подробное описание методов

#### POST `-api/login`

Для директора и суперадмина интерфейс одинаковые.  
