# TelegramWhisper
> In this git I will explain how to create a telegram bot and how you can get the chat id.


## Instalation

Install python3 and pip3

<pre> sudo apt install python3 </pre>
<pre> sudo apt install python3-pip</pre>

Install the dependencies via pip3:

<pre> pip3 install python-telegram-bot</pre>


#### Creating BotChat

For the development of our bot you have to make use of “The Botfather” (https://core.telegram.org/bots) which consists of an application created by Telegram that will act as a mediator between Telegram and our code.

To do this, you must access the “BotFather” channel through one of the platforms offered by Telefram (iOS, Android or Windows) or (Mac, Windows, Linux, web version).
In this case, I will use your web version (https://web.telegram.org/).

![ScreenShot](https://securitytrooper.com/wp-content/uploads/2017/12/2017-12-12-09_28_48-Telegram-Web.png)


Once inside that channel, just put “/start” then “/newbot” and then enter the name of your bot, remember that it has to go just “_bot” or “bot”.

![ScreenShot](https://securitytrooper.com/wp-content/uploads/2017/12/2017-12-12-09_55_25-Telegram-Web.png)

With the previous message, we will confirm that everything has been created correctly.
It is very important that we have our Bot in contacts because you will need to know the chat_id we have in common.
Surely there are ways to get this “chat_id” simpler but I will explain the one I use.

This Script will help you get the chat_id but for it to work you have to (previously) have talked to your bot (e. g. from the chat bot: t. me/XXXXXXXX_bot)
Remember to put your TOKEN previously obtained

<pre>
# -*- coding: utf-8 -*-
import telegram

#TOKEN de la API - Botfather
TOKEN = 'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX'
bot = telegram.Bot(token=TOKEN)

updates = bot.get_updates()
print([u.message.chat_id for u in updates])
</pre>

The chat_id will be in the style of 17XXXXX. This chat_id can also be a negative value (e. g. -17XXXXXX).
