Conference Room Booking API
Опис проєкту
Цей проєкт представляє REST API для управління орендою конференц-залів. API дозволяє бронювати зали, обирати додаткові послуги, а також автоматично застосовувати знижки залежно від часу бронювання. Система також містить механізм для збору аналітики щодо популярності залів, сервісів та часу оренди.

Основні функції
Бронювання конференц-залів із різною місткістю та ціною.
Вибір додаткових послуг, таких як оренда проєктора, Wi-Fi та звукового обладнання.
Автоматичне застосування знижок або націнок відповідно до часу бронювання.
Інтеграція з MongoDB для зберігання даних про зали, послуги, знижки та бронювання.
Звіти та аналітика для відслідковування популярності залів, часу бронювань і сервісів.
Стек технологій
ASP.NET Core – основний фреймворк для розробки API.
MongoDB – NoSQL база даних для зберігання інформації.
Swagger – для документування та тестування API.
Docker – для контейнеризації додатка (опціонально).
Вимоги
.NET 6 або новіший
MongoDB 4.4 або новіший
Docker (опціонально для контейнеризації)
Налаштування
Клонувати репозиторій:

bash
Copy code
git clone https://github.com/yourusername/conference-room-booking-api.git
Перейти в директорію проєкту:

bash
Copy code
cd conference-room-booking-api
Встановити залежності:

bash
Copy code
dotnet restore
Налаштувати MongoDB у файлі appsettings.json:

json
Copy code
{
  "MongoDbSettings": {
    "ConnectionString": "mongodb+srv://<username>:<password>@cluster-url",
    "DatabaseName": "ConferenceRoomBookingDB"
  }
}
Запустити проєкт:

bash
Copy code
dotnet run
Ініціалізація бази даних
Щоб заповнити базу даних початковими даними, запустіть клас SeedDatabase, який додасть зали, послуги, знижки та тестові бронювання.

Використання API
Після запуску проєкту можна використовувати Swagger для взаємодії з API. Відкрийте браузер і перейдіть за адресою:

bash
Copy code
https://localhost:5001/swagger
Основні ендпоінти:
GET /api/conferenceRooms – Отримати список всіх конференц-залів.
POST /api/bookings – Створити бронювання.
GET /api/reports – Отримати звіт щодо найбільш популярних залів та сервісів.
Тестування
Щоб виконати тести, використовуйте команду:

bash
Copy code
dotnet test
Безпека та масштабованість
Проєкт побудований із дотриманням принципів чистого коду та SOLID, що забезпечує легку підтримку та масштабованість. Використовуються рекомендації для безпечного доступу до бази даних, включно з правильним зберіганням конфіденційних даних (паролів, ключів) у змінних середовища.

Ліцензія
Цей проєкт ліцензований на умовах ліцензії MIT.
