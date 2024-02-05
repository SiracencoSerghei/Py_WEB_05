## Домашнє завдання #5
# Основна обов'язкова частина
Публічне АПІ ПриватБанка дозволяє отримати інформацію про готівку курсах валют ПриватБанку та НБУ на обрану дату. Архів зберігає дані за останні 4 роки

Напишіть консольну утиліту, яка повертає курс EUR та USD ПриватБанку протягом останніх кількох днів. Встановіть обмеження, що в утиліті можна дізнатися курс валют не більше, ніж за останні 10 днів. Для запиту до АПІ використовуйте Aiohttp client. Дотримуйтесь принципів SOLID під час написання завдання. Обробляйте коректно помилки при мережевих запитах.

Приклад роботи:

py .\main.py 2

Результат програми:

[
  {
    '03.11.2022': {
      'EUR': {
        'sale': 39.4,
        'purchase': 38.4
      },
      'USD': {
        'sale': 39.9,
        'purchase': 39.4
      }
    }
  },
  {
    '02.11.2022': {
      'EUR': {
        'sale': 39.4,
        'purchase': 38.4
      },
      'USD': {
        'sale': 39.9,
        'purchase': 39.4
      }
    }
  }
]


# Додаткова частина
додайте можливість вибору, через передані параметри консольної утиліти, додаткових валют у відповіді програми
візьміть чат на веб-сокетах з лекційного матеріалу та додайте до нього можливість введення команди exchange. Вона показує користувачам поточний курс валют у текстовому форматі. Формат представлення виберіть на власний розсуд
розширте додану команду exchange, щоб була можливість переглянути курс валют в чаті за останні кілька днів. Приклад exchange 2
за допомогою пакетів aiofile та aiopath додайте логування до файлу, коли була виконана команда exchange у чаті

## console 

 # first part
      examples:

       python3 main.py 2 -c USD,EUR,PLN
       or 
       python3 main.py 2 --currencies USD,EUR,PLN

 # extra task
  
  python3 server.py  + min 2 браузера 

  



## Docker
1. створення image
   '''docker build . -t siracencoserghei/hw_5:0.0.1'''
2. завантаження image в dockerhub
   '''docker push siracencoserghei/hw_5:0.0.1'''
3. скачування image з dockerhub
  '''docker pull siracencoserghei/hw_5:0.0.1'''
4. запускаемо docker container на  сервері
   '''docker run -d \
    --name HW-05 \ 
    -p 8081:8081 -p 8000:8000 \ 
    siracencoserghei/hw_5:0.0.1
'''