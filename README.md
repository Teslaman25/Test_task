# Test_task
Тестовое Задание BA+SA
Кандидат: [Ваше имя]
Дата: Декабрь 2025
Статус: ✅ Выполнено

📋 Содержание
Задача 1: BPMN 2.0 Модель (Выдача IT-Оборудования)

Задача 2: User Stories и Use Cases (Маркетплейс)

Задача 3: REST API и Алгоритм Регистрации

Инструкция: Как push на GitHub

Задача 1: BPMN 2.0 Модель
Описание рабочего процесса
Выдача IT-оборудования в компании X осуществляется через систему заявок с участием:

Пользователя офиса (инициатор)

1-й линии техподдержки (L1)

Отдела снабжения

Логистики

Поставщика (при отсутствии оборудования)

Полное описание BPMN модели, диаграмма Mermaid и вопросы/противоречия см. в docs/TASK-1-BPMN.md

Задача 2: User Stories и Use Cases
User Story для маркетплейса
Как продавец книжного магазина,
я хочу опубликовать свой товар на маркетплейсе,
чтобы увеличить продажи и охватить больше клиентов.

Полное описание User Story, 3 Use Cases и диаграммы см. в docs/TASK-2-USERSTORIES.md

Задача 3: REST API и Алгоритм Регистрации
3.1 REST API спецификация
Эндпоинт: POST /api/v1/auth/register

Основные параметры:

Input: firstName, lastName, username, password, recaptchaToken

Output (201): userId, username, firstName, lastName

Errors: 400 (валидация), 409 (пользователь существует), 500 (сервер)

Полное описание см. в docs/TASK-3-API-REGISTRATION.md

3.2 Алгоритм создания пользователя
8-шаговый алгоритм с валидацией пароля, проверкой reCAPTCHA, хешированием и сохранением в БД.

Диаграмма (Activity) и текстовое описание см. в docs/TASK-3-ALGORITHM.md

📁 Структура репозитория
text
test-task-ba-sa/
├── README.md                          # Главная навигация
├── docs/
│   ├── TASK-1-BPMN.md                # BPMN модель + вопросы
│   ├── TASK-2-USERSTORIES.md         # User Story + Use Cases
│   ├── TASK-3-API-REGISTRATION.md    # REST API спецификация
│   ├── TASK-3-ALGORITHM.md           # Activity диаграмма + алгоритм
│   └── diagrams/
│       ├── equipment-flow.mmd         # BPMN Mermaid
│       ├── registration-activity.mmd  # Activity Mermaid
│       └── seller-usecase.mmd         # Use Case Mermaid
└── api/
    └── registration.yaml             # OpenAPI 3.0 спецификация
🎯 Ключевые аспекты
BPMN (Задача 1)
Gateway для условия "Оборудование есть?"

Параллельные потоки для уведомлений

Исключения для ошибок и откатов

Вопросы и противоречия к процессу

Use Cases (Задача 2)
User Story в формате: Как / я хочу / чтобы

3 Use Cases: Create, Update, Delete

Основные и альтернативные потоки

Предусловия, постусловия и исключения

REST API (Задача 3.1)
Методология: REST (POST, 201 Created, 409 Conflict, 400 Bad Request)

Валидация: пароль (сложность), username (уникальность), reCAPTCHA

Ошибки: 4xx (клиент), 5xx (сервер)

OpenAPI YAML спецификация

Алгоритм (Задача 3.2)
8 шагов валидации и обработки

Activity диаграмма (Mermaid)

Защита: bcrypt/Argon2 + reCAPTCHA v3

Обработка ошибок и исключений

📝 Использованные инструменты
Диаграммы: Mermaid (автоматический рендеринг в GitHub)

API спецификация: OpenAPI 3.0 (Swagger)

Документация: Markdown (.md)

Версионирование: Git + GitHub

Интерфейс: Book Store Register (анализ скриншотов)
