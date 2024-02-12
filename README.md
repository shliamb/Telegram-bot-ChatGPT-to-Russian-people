
# RU

Что это?
Это простой телеграм бот. Он дает прямой доступ к ChatGPT 3.5, ChatGPT 4 Turbo, ChatGPT 4 и др.

Для кого это?
Для тех кто вынужден находиться под санкциями, а VPN постоянно блокируется и постоянно виснет. Для тех, кто не может себе позволить 20$ в месяц на последнюю версию ChatGPT от OpenAI.
Этот бот позволяет пользоваться оригинальным ChatGPT экономно, дозированно. Оплата только за токены. К примеру, я пользуюсь на постоянной основе GPT-3.5, но когда он не справляется, переключаюсь на GPT-4, выходит очень дешево.

Как пользоваться?
1. Если вы в теме программирования. Выбрать сервер без санкций, установить приложение, зарегиться в OpenAI, закинуть 5$ и пользоваться.
2. Можете просто пользоваться моим - https://t.me/shliamb2_bot Можно просто попробовать.



Технологии:
1. Aiogram 3
2. SQLAlchimi...
3...

Как работает, очень коротко.


Как работает просто коротко.


Как работает подробно.



- Общение с OpenAI идет асинхронно, но не в стриме, так как телеграм не будет стримить, как я понял. Асинхрон, но надо еще попрактиковать, так как не отскакивает.

- Думаю даза SQLite в GitHab будет пустая но с таблицами. Если забуду и будет пустая или вы сами удалите, то можно запусть файл init_db.py - он разметит и внесет все по умолчанию.

- Файл .env.example нужно переписать в .env и после деплоя на сервер, в ручную вписать в него через Bash ключ от OpenAI. Так как скомпроментированный ключ в GitHab тут же удаляется из панели на сайте OpenAI, проверенно.

- Использую SQLite, из-за того что он не использует ОЗУ, проэкт маленький, пока будет плюсом не дорогая виртуалка.

- при первом нажатии /start бот здоровается пороходясь по наличию из всех имен, если нет ничего, ну мало ли, то обращается "друг" и так происходит постоянно при нажатии /start.  Так же происходит проверка user_id пользователя телеграм в базе. если его нет, то в базу добавляется user_id пользователя, имена и клички в таблицу users_telegram. Так же проставляются умолчания и соотвествующий id в таблицу chatgpt_setings настроек чата гпт пользователя. Если пользователь поменяет свое имя в телеграм, то при нажатии /start будет браться первое из существующих актуального, в базе останется то что внеслось в первый раз.



# EN

ChatGPT + Telegram bot. There are a lot of them on the Internet, mine is probably no better. I did it because I needed it. Unfortunately, in Russia, using standard methods is the art of launching a VPN. Therefore, it was decided to quickly make a telegram bot with ChatGPT. Which will allow you to get an answer in the simplest format and quickly.

Features:
1. Logging on logging,
2. Bot on the telebot library,
3. If the waiting is exceeded, it is automatically re-logged,
4. ..

На кофе под развитие - 
