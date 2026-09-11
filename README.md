# 🚀 Проект: Тестирование API сервиса **Яндекс.Прилавок**

![Проект](https://img.shields.io/badge/Проект-Яндекс.Прилавок-orange)  
![Спринт](https://img.shields.io/badge/Спринт-5-blue)  
![Статус](https://img.shields.io/badge/Статус-Завершён-brightgreen)  
![Платформа](https://img.shields.io/badge/Платформа-API-lightgrey)  
![Баги](https://img.shields.io/badge/Найдено_багов-26-red)  
![Критические](https://img.shields.io/badge/Критические-18-red)  
![Блокирующие](https://img.shields.io/badge/Блокирующие-8-darkred)  

---

## 📝 Описание

Проект выполнен в рамках **5-го спринта курса “Инженер по тестированию: от новичка до автоматизатора” (Яндекс Практикум)**.  
Задача — протестировать новую версию **API Яндекс.Прилавок (v3.3.1)** после обновления функциональности: работа с наборами, корзиной и доставкой.

Цель тестирования:
- Проверить корректность реализации новых эндпоинтов;
- Провести функциональное и негативное тестирование;
- Зафиксировать найденные дефекты и подготовить итоговый отчёт.

---

## 📎 Артефакты

| Тип документа | Ссылка |
|----------------|--------|
| 📑 Требования к бэкенду | [PDF](https://code.s3.yandex.net/qa/files/backend_requirements.pdf) |
| ✅ Чек-лист тестирования | [Google Sheets](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit?gid=2006427015#gid=2006427015) |
| 🐞 Таблица баг-репортов (29 дефектов) | [Google Sheets](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit?gid=2107688692#gid=2107688692) |
| 📄 Отчёт о тестировании | [GitHub](./Test_Report.md) |

---

## 🔍 Этапы тестирования

### 🔹 Этап 1. Подготовка
- Изучена документация API (Swagger / Apidoc);
- Определены тестовые данные и сценарии;
- Составлен функциональный чек-лист.

### 🔹 Этап 2. Проведение тестирования
- Выполнено 144 проверок в Postman;
- Зафиксировано 26 дефектов (8 блокирующих, 18 критических).

### 🔹 Этап 3. Анализ результатов
- Проведена классификация багов по приоритетам;
- Оценена готовность API к релизу;
- Подготовлен отчёт и рекомендации по ретесту.

---

## 📊 Результаты тестирования

- Всего проверок: **144**  
- Пройдено успешно: **42**  
- Не пройдено: **102**

| Приоритет | Кол-во | Примеры |
|------------|--------|----------|
| 🔴 **Блокирующие** | 10 | [BUG_01](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1268697266), [BUG_04](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=381142893), [BUG_05](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=3722855), [BUG_07](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1955037002), [BUG_10](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=304805320), [BUG_11](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1695991182), [BUG_19](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1280226422), [BUG_23](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1394821330)|
| 🔴 **Критические** | 19 | [BUG_02](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=361344914), [BUG_03](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=2037921325), [BUG_06](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=2075647037), [BUG_08](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=398576962), [BUG_09](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=785937866), [BUG_12](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=177733890), [BUG_13](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=177733890), [BUG_14](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1557623866), [BUG_15](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1795141980), [BUG_16](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=402429906), [BUG_17](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1844017944), [BUG_18](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1934258068), [BUG_20](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=87349439), [BUG_21](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=798978636), [BUG_22](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=88141479), [BUG_24](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1839930380), [BUG_25](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=2056867305), [BUG_26](https://docs.google.com/spreadsheets/d/1eHGrTqAJk5Yyb7hfFX5gaID3Q5rl4Gvkzy3Y1UnUw9Y/edit#rangeid=1549481457) |

---


## 🚀 Выводы

- Найдено **26 дефектов**, включая **8 блокирующих** и **16 критических**;  
- Продукт не готов к продакшн-релизу без доработки;  
- После исправления дефектов требуется провести **повторное регрессионное тестирование**.