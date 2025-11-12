# Створення бронювання
## Use Case Diagram
![](https://github.com/user-attachments/assets/ec7a3a59-9205-4321-a0ad-5b88e1a1e9be)
## Sequence Diagram
![](https://github.com/user-attachments/assets/fd767ede-7f51-4a34-82e1-958242a100a0)
## Опис послідовності дій
Користувач створює бронювання, виконуючи дію CreateBooking() через інтерфейс UI, далі UI формує запит і надсилає його до Booking API. Booking API передає отримані дані до Booking Service для обробки, потім Booking Service викликає метод для перевірки, чи вибране місце вільне. Repository звертається до бази даних, виконує SQL-запит і повертає результат про доступність місця, після підтвердження що місце доступне Booking Service викликає метод SaveBooking() у Repository для збереження нового бронювання. Repository записує дані в базу даних, потім Booking Service повертає результат у Booking API, а API надсилає відповідь назад у UI, та UI повідомляє користувача про успішне створення бронювання.
