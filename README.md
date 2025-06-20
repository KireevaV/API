[DemoShopping.json](https://github.com/user-attachments/files/20837501/DemoShopping.json)[DemoShopping.json](https://github.com/user-attachments/files/20837452/DemoShopping.json)[DemoShopping.json](https://github.com/user-attachments/files/20837442/DemoShopping.json)# API

# Тестирование API
[ссылка на документ]
https://www.postman.com/supply-explorer-36567248/workspace/my-workspace/folder/40399380-ddeb2a73-49f7-4771-a1ee-85d3b0778091?action=share&creator=40399380&ctx=documentation&active-environment=40399380-cd14339a-ed62-48a9-b3d7-0b5e4503a912

# Первые автотесты

[Uploading DemoShopping.json…]()
{
	"id": "f5fad9b5-e054-4ab5-a8c9-b74e7145511a",
	"name": "DemoShopping",
	"timestamp": "2025-06-20T12:52:20.145Z",
	"collection_id": "40399380-999bb358-2e73-49a9-b5c9-252b03bf270f",
	"folder_id": 0,
	"environment_id": "40399380-cd14339a-ed62-48a9-b3d7-0b5e4503a912",
	"totalPass": 24,
	"delay": 0,
	"persist": true,
	"status": "finished",
	"startedAt": "2025-06-20T12:52:14.082Z",
	"totalFail": 1,
	"results": [
		{
			"id": "b7c8c65f-09ab-4f8f-a5b3-9d15219cbeea",
			"name": "200 - Возвращает список всех продуктов",
			"url": "https://qa.demoshopping.ru/products",
			"time": 94,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус-код 200": true,
				"Ответ — массив": true,
				"В массиве 50 продуктов": false,
				"Каждый продукт содержит необходимые поля с правильными типами": true,
				"Первый продукт соответствует ожиданиям": true
			},
			"testPassFailCounts": {
				"Статус-код 200": {
					"pass": 1,
					"fail": 0
				},
				"Ответ — массив": {
					"pass": 1,
					"fail": 0
				},
				"В массиве 50 продуктов": {
					"pass": 0,
					"fail": 1
				},
				"Каждый продукт содержит необходимые поля с правильными типами": {
					"pass": 1,
					"fail": 0
				},
				"Первый продукт соответствует ожиданиям": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				94
			],
			"allTests": [
				{
					"Статус-код 200": true,
					"Ответ — массив": true,
					"В массиве 50 продуктов": false,
					"Каждый продукт содержит необходимые поля с правильными типами": true,
					"Первый продукт соответствует ожиданиям": true
				}
			]
		},
		{
			"id": "e0fcf7e7-8e67-4b9a-bd83-9896bb22512f",
			"name": "200- Добавление нового продукта",
			"url": "https://qa.demoshopping.ru/add-product",
			"time": 41,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус 201 или 200": true,
				"Ответ — строка": true,
				"Ответ содержит 'Продукт успешно добавлен'": true,
				"ID успешно извлечен из текста": true
			},
			"testPassFailCounts": {
				"Статус 201 или 200": {
					"pass": 1,
					"fail": 0
				},
				"Ответ — строка": {
					"pass": 1,
					"fail": 0
				},
				"Ответ содержит 'Продукт успешно добавлен'": {
					"pass": 1,
					"fail": 0
				},
				"ID успешно извлечен из текста": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				41
			],
			"allTests": [
				{
					"Статус 201 или 200": true,
					"Ответ — строка": true,
					"Ответ содержит 'Продукт успешно добавлен'": true,
					"ID успешно извлечен из текста": true
				}
			]
		},
		{
			"id": "ef8cbc44-d632-4720-9ed6-199534dc8205",
			"name": "400 - Добавление нового продукта",
			"url": "https://qa.demoshopping.ru/add-product",
			"time": 21,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {
				"Статус-код 400 при пустом поле price": true,
				"Ответ содержит сообщение об ошибке по price": true,
				"Время ответа < 1000 мс": true
			},
			"testPassFailCounts": {
				"Статус-код 400 при пустом поле price": {
					"pass": 1,
					"fail": 0
				},
				"Ответ содержит сообщение об ошибке по price": {
					"pass": 1,
					"fail": 0
				},
				"Время ответа < 1000 мс": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				21
			],
			"allTests": [
				{
					"Статус-код 400 при пустом поле price": true,
					"Ответ содержит сообщение об ошибке по price": true,
					"Время ответа < 1000 мс": true
				}
			]
		},
		{
			"id": "0b9d9e61-fb96-40a4-8bfa-3c7312f0d150",
			"name": "200 - Поиск товара по ID",
			"url": "https://qa.demoshopping.ru/products/id/21647",
			"time": 22,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус-код 200": true,
				"Поля присутствуют": true,
				"Типы данных корректны": true,
				"Цена — положительное число": true,
				"Время ответа < 1000 мс": true
			},
			"testPassFailCounts": {
				"Статус-код 200": {
					"pass": 1,
					"fail": 0
				},
				"Поля присутствуют": {
					"pass": 1,
					"fail": 0
				},
				"Типы данных корректны": {
					"pass": 1,
					"fail": 0
				},
				"Цена — положительное число": {
					"pass": 1,
					"fail": 0
				},
				"Время ответа < 1000 мс": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				22
			],
			"allTests": [
				{
					"Статус-код 200": true,
					"Поля присутствуют": true,
					"Типы данных корректны": true,
					"Цена — положительное число": true,
					"Время ответа < 1000 мс": true
				}
			]
		},
		{
			"id": "ebbd3be8-2c0d-46d4-946a-ce53545d709b",
			"name": "200 - Полное обновление товара",
			"url": "https://qa.demoshopping.ru/products/id/21647",
			"time": 27,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус-код 200 или 204": true,
				"Ответ — строка": true,
				"Ответ содержит 'Товар обновлён'": true,
				"Время ответа < 1000 мс": true
			},
			"testPassFailCounts": {
				"Статус-код 200 или 204": {
					"pass": 1,
					"fail": 0
				},
				"Ответ — строка": {
					"pass": 1,
					"fail": 0
				},
				"Ответ содержит 'Товар обновлён'": {
					"pass": 1,
					"fail": 0
				},
				"Время ответа < 1000 мс": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				27
			],
			"allTests": [
				{
					"Статус-код 200 или 204": true,
					"Ответ — строка": true,
					"Ответ содержит 'Товар обновлён'": true,
					"Время ответа < 1000 мс": true
				}
			]
		},
		{
			"id": "62dfc383-61a6-451d-9e5c-9b7c2cf1213d",
			"name": "200 - Частичное обновление товара по ID",
			"url": "https://qa.demoshopping.ru/products/id/21647",
			"time": 22,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {
				"Статус-код 200 или 204": true,
				"Ответ — строка": true,
				"Ответ содержит 'Товар частично обновлён'": true,
				"Время ответа < 1000 мс": true
			},
			"testPassFailCounts": {
				"Статус-код 200 или 204": {
					"pass": 1,
					"fail": 0
				},
				"Ответ — строка": {
					"pass": 1,
					"fail": 0
				},
				"Ответ содержит 'Товар частично обновлён'": {
					"pass": 1,
					"fail": 0
				},
				"Время ответа < 1000 мс": {
					"pass": 1,
					"fail": 0
				}
			},
			"times": [
				22
			],
			"allTests": [
				{
					"Статус-код 200 или 204": true,
					"Ответ — строка": true,
					"Ответ содержит 'Товар частично обновлён'": true,
					"Время ответа < 1000 мс": true
				}
			]
		},
		{
			"id": "e1d791ed-b1d9-4996-93af-ff518ce6262b",
			"name": "200 Авторизация пользователя",
			"url": "https://qa.demoshopping.ru/login",
			"time": 38,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				38
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "a1ed16fe-4570-406d-9b9f-5b87ebf245b1",
			"name": "400 Авторизация пользователя",
			"url": "https://qa.demoshopping.ru/login",
			"time": 24,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				24
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "175ba19f-6a48-4094-832a-12038c0f80e5",
			"name": "200 Регистрация нового пользователя",
			"url": "https://qa.demoshopping.ru/register",
			"time": 24,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				24
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "999fd4e0-1a91-4923-9cc0-9d8bb13185a2",
			"name": "400 регистрация нового пользователя",
			"url": "https://qa.demoshopping.ru/register",
			"time": 30,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				30
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "140ff404-955c-49a3-9fcf-f7aee04b2d28",
			"name": "400 Добавление нового пользователя",
			"url": "https://qa.demoshopping.ru/users",
			"time": 40,
			"responseCode": {
				"code": 400,
				"name": "Bad Request"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				40
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "a676422d-72a2-4220-8872-bfbbd0890b1c",
			"name": "200 Получение всех user_id и login пользователей",
			"url": "https://qa.demoshopping.ru/users",
			"time": 111,
			"responseCode": {
				"code": 200,
				"name": "OK"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				111
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "33873dc0-f763-4a0f-b6fc-b5c5b38bcc3c",
			"name": "200 Удаляет пользователя по ID",
			"url": "https://qa.demoshopping.ru/users/3018",
			"time": 31,
			"responseCode": {
				"code": 404,
				"name": "Not Found"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				31
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "2a71f978-2eca-4b70-bb86-b7bc10e6f2e2",
			"name": "Удаляет пользователя по ID",
			"url": "https://qa.demoshopping.ru/users/3018",
			"time": 21,
			"responseCode": {
				"code": 404,
				"name": "Not Found"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "0bf37d4f-b05f-4001-8ccd-173583e8a360",
			"name": "200 Добавляет товар в корзину",
			"url": "https://qa.demoshopping.ru/cart",
			"time": 22,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				22
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "1b157590-3b6b-4fe5-9f68-5489046535d0",
			"name": "401 Добавляем товар в корзину пользователя",
			"url": "https://qa.demoshopping.ru/cart",
			"time": 27,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				27
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "d8cef620-6ee0-4965-aa75-c5da644bcb01",
			"name": "200 Возвращает содержимое корзины пользователя",
			"url": "https://qa.demoshopping.ru/getCart",
			"time": 307,
			"responseCode": {
				"code": 500,
				"name": "Internal Server Error"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				307
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "24e1909c-8769-4db3-bf82-8968c651c91d",
			"name": "401 Возвращает содержимое корзины пользователя",
			"url": "https://qa.demoshopping.ru/getCart",
			"time": 21,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "aa1880b7-33bb-48a6-a860-693777d23477",
			"name": "200 Обновляет количество товара в корзине пользователя",
			"url": "https://qa.demoshopping.ru/cart/18402",
			"time": 24,
			"responseCode": {
				"code": 500,
				"name": "Internal Server Error"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				24
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "15af4622-d950-4e8f-b242-db5c048d9f78",
			"name": "401 Обновляет количество товара в корзине пользователя",
			"url": "https://qa.demoshopping.ru/cart/18403",
			"time": 27,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				27
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "f24e96a0-dec0-44f2-a5ba-a884aa0f28db",
			"name": "200 Удаляет товар из корзины пользователя",
			"url": "https://qa.demoshopping.ru/cart/18403",
			"time": 21,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "e505a4f5-da58-49d4-972e-86562bbfaa1d",
			"name": "401 Удаляет товар из корзины пользователя",
			"url": "https://qa.demoshopping.ru/cart/18402",
			"time": 21,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "6b927cb1-044c-4ffe-85be-49949679212e",
			"name": "201 Создание заказа из товаров в корзине пользователя",
			"url": "https://qa.demoshopping.ru/orders",
			"time": 21,
			"responseCode": {
				"code": 500,
				"name": "Internal Server Error"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "8eccc6cd-6813-420c-a45b-dcc172dbc9cf",
			"name": "401 Создание заказа из товаров в корзине пользователя",
			"url": "https://qa.demoshopping.ru/orders",
			"time": 27,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				27
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "1967e9e2-89ed-4fa0-9128-13b7def500f5",
			"name": "200 Изменение количества товара в корзине",
			"url": "https://qa.demoshopping.ru/orders/5881/products/18405",
			"time": 21,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "99403e4b-8aa7-45a7-849a-088c348db88c",
			"name": "401 Изменение количества товара в корзине",
			"url": "https://qa.demoshopping.ru/orders/5881/products/18405",
			"time": 22,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				22
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "4c00f65a-89a2-456d-91c0-d89cbcd6b1a6",
			"name": "404 Изменение количества товара в корзине",
			"url": "https://qa.demoshopping.ru/orders/5891/products/18",
			"time": 21,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "9a76e206-702d-4aad-823e-af5f28b8591d",
			"name": "200 Обновление общей суммы заказов пользователя",
			"url": "https://qa.demoshopping.ru/update-orders-total",
			"time": 20,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				20
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "953dbe65-02ab-4650-9b21-a01aba33c465",
			"name": "401 Обновление общей суммы заказов пользователя",
			"url": "https://qa.demoshopping.ru/update-orders-total",
			"time": 21,
			"responseCode": {
				"code": 401,
				"name": "Unauthorized"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				21
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "b45406ce-ebca-49a6-a448-117727e30d27",
			"name": "200 Получение данных об оплаченных заказах",
			"url": "https://qa.demoshopping.ru/api/orders-history",
			"time": 26,
			"responseCode": {
				"code": 500,
				"name": "Internal Server Error"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				26
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "e7a5c1e4-3ef3-4a40-beb1-a360943861ee",
			"name": "200 Удаление товара из заказа",
			"url": "https://qa.demoshopping.ru/orders/5884/products/1",
			"time": 62,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				62
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "188ff941-43da-4f77-92db-1eb719632f2c",
			"name": "401 Удаление товара из заказа",
			"url": "https://qa.demoshopping.ru/orders/5884/products/1",
			"time": 20,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				20
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "266f1e86-b111-42b2-9c8c-f69149ee3540",
			"name": "404 Удаление товара из заказа",
			"url": "https://qa.demoshopping.ru/orders/5884/products/1",
			"time": 31,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				31
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "7d8b0f5c-20b8-4fe4-8ad6-648519d67596",
			"name": "200 Оплата заказов пользователя",
			"url": "https://qa.demoshopping.ru/pay",
			"time": 23,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				23
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "6f3b3514-78f3-4a0b-964d-516b67296bcb",
			"name": "400 Оплата заказов пользователя",
			"url": "https://qa.demoshopping.ru/pay",
			"time": 20,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				20
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "6ba0cdb7-b37e-431b-89cc-b6c767ce02d9",
			"name": "401 Оплата заказов пользователя",
			"url": "https://qa.demoshopping.ru/pay",
			"time": 22,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				22
			],
			"allTests": [
				{}
			]
		},
		{
			"id": "6118c8a3-d1af-47dd-b5a7-ad70722bd757",
			"name": "200 Обновление балансов карт и PayPal через GET запрос",
			"url": "https://qa.demoshopping.ru/updateBalances",
			"time": 18,
			"responseCode": {
				"code": 502,
				"name": "Bad Gateway"
			},
			"tests": {},
			"testPassFailCounts": {},
			"times": [
				18
			],
			"allTests": [
				{}
			]
		}
	],
	"count": 1,
	"totalTime": 1391,
	"collection": {
		"requests": [
			{
				"id": "b7c8c65f-09ab-4f8f-a5b3-9d15219cbeea",
				"method": "GET"
			},
			{
				"id": "e0fcf7e7-8e67-4b9a-bd83-9896bb22512f",
				"method": "POST"
			},
			{
				"id": "ef8cbc44-d632-4720-9ed6-199534dc8205",
				"method": "POST"
			},
			{
				"id": "0b9d9e61-fb96-40a4-8bfa-3c7312f0d150",
				"method": "GET"
			},
			{
				"id": "ebbd3be8-2c0d-46d4-946a-ce53545d709b",
				"method": "PUT"
			},
			{
				"id": "62dfc383-61a6-451d-9e5c-9b7c2cf1213d",
				"method": "PATCH"
			},
			{
				"id": "e1d791ed-b1d9-4996-93af-ff518ce6262b",
				"method": "POST"
			},
			{
				"id": "a1ed16fe-4570-406d-9b9f-5b87ebf245b1",
				"method": "POST"
			},
			{
				"id": "175ba19f-6a48-4094-832a-12038c0f80e5",
				"method": "POST"
			},
			{
				"id": "999fd4e0-1a91-4923-9cc0-9d8bb13185a2",
				"method": "POST"
			},
			{
				"id": "140ff404-955c-49a3-9fcf-f7aee04b2d28",
				"method": "POST"
			},
			{
				"id": "a676422d-72a2-4220-8872-bfbbd0890b1c",
				"method": "GET"
			},
			{
				"id": "33873dc0-f763-4a0f-b6fc-b5c5b38bcc3c",
				"method": "DELETE"
			},
			{
				"id": "2a71f978-2eca-4b70-bb86-b7bc10e6f2e2",
				"method": "DELETE"
			},
			{
				"id": "0bf37d4f-b05f-4001-8ccd-173583e8a360",
				"method": "POST"
			},
			{
				"id": "1b157590-3b6b-4fe5-9f68-5489046535d0",
				"method": "POST"
			},
			{
				"id": "d8cef620-6ee0-4965-aa75-c5da644bcb01",
				"method": "GET"
			},
			{
				"id": "24e1909c-8769-4db3-bf82-8968c651c91d",
				"method": "GET"
			},
			{
				"id": "aa1880b7-33bb-48a6-a860-693777d23477",
				"method": "PATCH"
			},
			{
				"id": "15af4622-d950-4e8f-b242-db5c048d9f78",
				"method": "PATCH"
			},
			{
				"id": "f24e96a0-dec0-44f2-a5ba-a884aa0f28db",
				"method": "DELETE"
			},
			{
				"id": "e505a4f5-da58-49d4-972e-86562bbfaa1d",
				"method": "DELETE"
			},
			{
				"id": "6b927cb1-044c-4ffe-85be-49949679212e",
				"method": "POST"
			},
			{
				"id": "8eccc6cd-6813-420c-a45b-dcc172dbc9cf",
				"method": "POST"
			},
			{
				"id": "1967e9e2-89ed-4fa0-9128-13b7def500f5",
				"method": "PATCH"
			},
			{
				"id": "99403e4b-8aa7-45a7-849a-088c348db88c",
				"method": "PATCH"
			},
			{
				"id": "4c00f65a-89a2-456d-91c0-d89cbcd6b1a6",
				"method": "PATCH"
			},
			{
				"id": "9a76e206-702d-4aad-823e-af5f28b8591d",
				"method": "POST"
			},
			{
				"id": "953dbe65-02ab-4650-9b21-a01aba33c465",
				"method": "POST"
			},
			{
				"id": "b45406ce-ebca-49a6-a448-117727e30d27",
				"method": "GET"
			},
			{
				"id": "e7a5c1e4-3ef3-4a40-beb1-a360943861ee",
				"method": "DELETE"
			},
			{
				"id": "188ff941-43da-4f77-92db-1eb719632f2c",
				"method": "DELETE"
			},
			{
				"id": "266f1e86-b111-42b2-9c8c-f69149ee3540",
				"method": "DELETE"
			},
			{
				"id": "7d8b0f5c-20b8-4fe4-8ad6-648519d67596",
				"method": "POST"
			},
			{
				"id": "6f3b3514-78f3-4a0b-964d-516b67296bcb",
				"method": "POST"
			},
			{
				"id": "6ba0cdb7-b37e-431b-89cc-b6c767ce02d9",
				"method": "POST"
			},
			{
				"id": "6118c8a3-d1af-47dd-b5a7-ad70722bd757",
				"method": "GET"
			}
		]
	}
}
