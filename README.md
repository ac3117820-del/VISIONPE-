import os
import telebot

TOKEN = os.getenv("BOT_TOKEN")

bot = telebot.TeleBot(TOKEN)

@bot.message_handler(commands=['start'])
def start(message):
    bot.reply_to(message, "Bienvenue sur VISIONPE ! 🚀")

bot.infinity_polling()
