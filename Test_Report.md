# 🧪 Отчёт о тестировании API сервиса **Яндекс.Прилавок**

![Проект](https://img.shields.io/badge/Проект-Яндекс.Прилавок-orange)  
![Спринт](https://img.shields.io/badge/Спринт-5-blue)  
![Статус](https://img.shields.io/badge/Статус-Тестирование_завершено-brightgreen)  
![Тип теста](https://img.shields.io/badge/Тип_тестирования-Функциональное_+_Негативное-green)
![Баги](https://img.shields.io/badge/Найдено_багов-26-red)  
![Критические](https://img.shields.io/badge/Критические-18-red)  
![Блокирующие](https://img.shields.io/badge/Блокирующие-8-darkred)  

---

## 📝 Цель тестирования
Проверка стабильности и корректности новой функциональности **API Яндекс.Прилавок**, включающей работу с наборами, корзинами и курьерской доставкой.  
Тестирование проводилось после добавления новых эндпоинтов в бэкенд.

---

## 🔍 Объект тестирования

**Тестируемая версия API:** `v3.3.1`  
**Тестовый стенд:** `https://{id}.serverhub.praktikum-services.ru/`  
**Документация:** `https://{id}.serverhub.praktikum-services.ru/docs/`

---

## 🧾 Артефакты

- ✅ [Чек-лист функционального тестирования](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit?gid=2006427015#gid=2006427015)
- ✅ [Таблица баг-репортов (26 дефектов)](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit?gid=2107688692#gid=2107688692)
- ✅ [Требования к бэкенду](https://code.s3.yandex.net/qa/files/backend_requirements.pdf)

---

## 📊 Результаты тестирования

- Всего проверок: **144**  
- Пройдено успешно: **42**  
- Не пройдено: **102**

---

## 🐞 Список обнаруженных дефектов

### 🔴 Блокирующие дефекты (8)
| ID | Название | Приоритет |
|----|-----------|------------|
| [BUG_01](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1268697266) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке пустого массива [ ] в теле ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_04](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=381142893) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром id, содержащим строку с английскими буквами "qwerty" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_05](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=3722855) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром id, содержащим массив [1,2,3] | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_07](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1955037002) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром quantity, содержащим дробное число 1,5 | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_10](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=304805320) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром quantity, содержащим массив [1,2,3] | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_11](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1695991182) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку возможности доставки без элемента потомка productsCount | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_19](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1280226422) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с параметром productList, содержащим строку с числом "123" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |
| [BUG_23](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1394821330) | ![500 Internal Server Error](https://img.shields.io/badge/500_Internal_Server_Error-darkred) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с параметром id, содержащим строку с англисйкими буквами "qwerty" | ![Блокирующий](https://img.shields.io/badge/Блокирующий-darkred) |

---

### 🔴 Критические дефекты (18)
| ID | Название | Приоритет |
|----|-----------|------------|
| [BUG_02](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=361344914) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке в теле ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` без элемента потомка id на добавление продуктов в набор | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_03](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=2037921325) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке в теле ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продукта с несуществующим id в набор | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_06](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=2075647037) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром quantity, содержащим отрицательное число -1 | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_08](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=398576962) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром quantity = 0 | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_09](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=785937866) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/api/v1/kits/id/products` на добавление продуктов в набор с параметром quantity, содержащим строку с числом "10" | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_12](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=177733890) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с отрицательным числом -1 в параметре productsCount | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_13](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=152745932) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с отрицательным числом -1 в параметре productsWeight | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_14](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1557623866) | Отсутствует тело ответа при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки в нерабочее время | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_15](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1795141980) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с отрицательным числом -1 в параметре deliveryTime | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_16](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=402429906) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![POST](https://img.shields.io/badge/POST-blue) запроса `/fast-delivery/v3.1.1/calculate-delivery.xml` на проверку недоступности доставки с числом ввиде строки "15" в параметре deliveryTime | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_17](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1844017944) | ![409 Conflict](https://img.shields.io/badge/409_Conflict-darkorange) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину без элемента потомка id | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_18](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1934258068) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину пустым массивом в productList [ ] | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_20](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=87349439) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину пустым массивом в productList [ ] | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_21](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=798978636) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину без элемента родителя productList | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_22](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=88141479) | ![409 Conflict](https://img.shields.io/badge/409_Conflict-darkorange) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с отрицательным числом id -1 | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_24](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1839930380) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину с числом в виде строки в id | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_25](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=2056867305) | ![200 OK](https://img.shields.io/badge/200_OK-brightgreen) при отправке при отправке ![PUT](https://img.shields.io/badge/PUT-yellow) запроса `/api/v1/orders/id` на добавление продуктов в корзину отрицательным quantity | ![Критический](https://img.shields.io/badge/Критический-red) |
| [BUG_26](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1549481457) | ![404 Not Found](https://img.shields.io/badge/404_Not_Found-red) при отправке при отправке ![DELETE](https://img.shields.io/badge/DELETE-red) запроса `/api/v1/orders/id` на удаление корзины с существующим id | ![Критический](https://img.shields.io/badge/Критический-red) |


---

## 📊 Распределение дефектов по приоритетам

| Приоритет | Кол-во | Примеры |
|------------|--------|----------|
| 🔴 **Блокирующие** | 8 | BUG_01, BUG_04, BUG_05, BUG_07, BUG_10, BUG_11, BUG_19, BUG_23 |
| 🟠 **Критические** | 18 | BUG_02, BUG_03, BUG_06, BUG_08, BUG_09, BUG_12, BUG_13, BUG_14, BUG_15, BUG_16, BUG_17, BUG_18, BUG_20, BUG_21, BUG_22, BUG_24, BUG_25, BUG_26 |

---

## 🔍 Рекомендации по повторному тестированию

После исправления дефектов рекомендуется:

- Повторно проверить обработку поля `quantity` в наборах и корзинах.  
- Перепроверить структуру ответов JSON на соответствие документации.  
- Провести smoke-тест всех эндпоинтов после фиксов.  
- Проверить корректность XML-валидации для ручки `/fast-delivery/v3.1.1/calculate-delivery.xml`.

---

## 📌 Итоги

- Критические и блокирующие дефекты **затрагивают ключевые пользовательские сценарии**.  
- API не готово к выпуску — требуется доработка бэкенда и повторное тестирование.  
- После фиксов необходимо выполнить **регрессионное тестирование**.
