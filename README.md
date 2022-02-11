import telebot
from telebot import types

# Все, что тебе нужно:
token = "" # токен основного бота
id = "" # Твой ид, что-бы бот кидал тебе все, что происходит в боте
site = "" # Cсылка оплаты(в конце ссылки пишите ваш ник QIWI)
channel = "" # Канал
channel1 = "" # Канал1
op = "" # Аккаунт оператора
admins = [] # Твой ид
 


bot = telebot.TeleBot(token)

@bot.message_handler(commands=["start"])
def repeat_all_messages(message):
  bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Написал: " + str(message.text))
  keyboard = types.InlineKeyboardMarkup()
  button1 = types.InlineKeyboardButton(text="Москва", callback_data="button1")
  button2 = types.InlineKeyboardButton(text="Воронеж", callback_data="button2")
  button3 = types.InlineKeyboardButton(text="Норильск", callback_data="button3")
  button4 = types.InlineKeyboardButton(text="Томск", callback_data="button4")
  button5 = types.InlineKeyboardButton(text="Краснодар", callback_data="button5")
  button6 = types.InlineKeyboardButton(text="Красноярск", callback_data="button6")
  button7 = types.InlineKeyboardButton(text="Иркутск", callback_data="button7")
  button8 = types.InlineKeyboardButton(text="Улан-Удэ", callback_data="button8")
  button9 = types.InlineKeyboardButton(text="Бийск", callback_data="button9")
  button10 = types.InlineKeyboardButton(text="Борисоглебцк", callback_data="button10")
  button11 = types.InlineKeyboardButton(text="Пермь", callback_data="button11")
  button12 = types.InlineKeyboardButton(text="Екатеринбург", callback_data="button12")
  button13 = types.InlineKeyboardButton(text="Сургут", callback_data="button13")
  button14 = types.InlineKeyboardButton(text="Сочи", callback_data="button14")
  button15 = types.InlineKeyboardButton(text="Ханты-Мансийский", callback_data="button15")
  button16 = types.InlineKeyboardButton(text="Абакан", callback_data="button16")
  button17 = types.InlineKeyboardButton(text="Оренбург", callback_data="button17")
  button18 = types.InlineKeyboardButton(text="Санкт-Петербург", callback_data="button18")
  keyboard.add(button1, button2, button3, button4, button5, button6, button7, button8, button9, button10, button11, button12, button13, button14, button15, button16, button17, button18)
  bot.send_message(message.chat.id, "🛍Добро пожаловать в наш бот-магазин.\nℹЕсли вашего города нету пишите сюда: @Phunra1\nНовости: "+str(channel)+"\n📕Отзывы: "+str(channel1)+"\n⚙️Оператор: "+str(op)+"\n☘️Пожалуйста, выберите город:", reply_markup=keyboard)

def button(message, city):
  keyboard1 = types.InlineKeyboardMarkup()
  button1 = types.InlineKeyboardButton(text="💨HQD CUVIE PLUS💨 (1200 тяг)", callback_data="red")
  button2 = types.InlineKeyboardButton(text="💨HQD KING💨 (2000 тяг)", callback_data="blue")
  bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Выбрал: " + str(city))
  keyboard1.add(button1)
  keyboard1.add(button2)
  bot.send_message(message.chat.id, "✅Вы выбрали город "+str(city)+".\n☘️Теперь выберите товар:", reply_markup=keyboard1)

def red(message, name):
  keyboard2 = types.InlineKeyboardMarkup()
  button1 = types.InlineKeyboardButton(text="Тархун 299р", callback_data="r1")
  button2 = types.InlineKeyboardButton(text="Кактусовый Лимонад 299р", callback_data="r2")
  button3 = types.InlineKeyboardButton(text="Клубника Питайя 299р", callback_data="r3")
  button4 = types.InlineKeyboardButton(text="Клубничный Милкшейк 299р", callback_data="4")
  button5 = types.InlineKeyboardButton(text="Лайм Кола 299р", callback_data="r5")
  button6 = types.InlineKeyboardButton(text="Ванильное мороженое 299р", callback_data="r6")
  button7 = types.InlineKeyboardButton(text="Банан 299р", callback_data="r7")
  button8 = types.InlineKeyboardButton(text="Клубника 299р", callback_data="r8")
  button9 = types.InlineKeyboardButton(text="Мультифрукт 299р", callback_data="r9")
  button10 = types.InlineKeyboardButton(text="Черника 299р", callback_data="r10")
  button11 = types.InlineKeyboardButton(text="Манго гуава 299р", callback_data="r11")
  button12 = types.InlineKeyboardButton(text="Яблоко 299р", callback_data="r12")
  button13 = types.InlineKeyboardButton(text="Энергетик 299р", callback_data="r13")
  button14 = types.InlineKeyboardButton(text="Арбузная жвачка 299р", callback_data="r14")
  button15 = types.InlineKeyboardButton(text="Розовый лимонад 299р", callback_data="r15")
  button16 = types.InlineKeyboardButton(text="Ананас 299р", callback_data="r16")
  button17 = types.InlineKeyboardButton(text="Виноград 299р", callback_data="r17")
  button18 = types.InlineKeyboardButton(text="Ледяная мята 299р", callback_data="r18")
  button19 = types.InlineKeyboardButton(text="Черника-малина-виноград  299р", callback_data="r19")
  button20 = types.InlineKeyboardButton(text="Йогурт лесные ягоды 299р", callback_data="r20")
  button21 = types.InlineKeyboardButton(text="Малина-лимон 299р", callback_data="r21")
  bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Выбрал: " + str(name))
  keyboard2.add(button1)
  keyboard2.add(button2)
  keyboard2.add(button3)
  keyboard2.add(button4)
  keyboard2.add(button5)
  keyboard2.add(button6)
  keyboard2.add(button7)
  keyboard2.add(button8)
  keyboard2.add(button9)
  keyboard2.add(button10)
  keyboard2.add(button11)
  keyboard2.add(button12)
  keyboard2.add(button13)
  keyboard2.add(button14)
  keyboard2.add(button15)
  keyboard2.add(button16)
  keyboard2.add(button17)
  keyboard2.add(button18)
  keyboard2.add(button19)
  keyboard2.add(button20)
  keyboard2.add(button21)
  bot.send_message(message.chat.id, "✅Вы выбрали "+str(name)+".\n☘️Теперь выберите вкус:", reply_markup=keyboard2)

def blue(message, name):
  keyboard1 = types.InlineKeyboardMarkup()
  button1 = types.InlineKeyboardButton(text="Кола 399р", callback_data="b1")
  button2 = types.InlineKeyboardButton(text="Персик 399р", callback_data="b2")
  button3 = types.InlineKeyboardButton(text="Мохито 399р", callback_data="b3")
  button4 = types.InlineKeyboardButton(text="Черника 399р", callback_data="b4")
  button5 = types.InlineKeyboardButton(text="Энергетик 399р", callback_data="b5")
  button6 = types.InlineKeyboardButton(text="Виноград 399р", callback_data="b6")
  button7 = types.InlineKeyboardButton(text="Мандарин 399р", callback_data="b7")
  button8 = types.InlineKeyboardButton(text="Клубника киви 399р", callback_data="b8")
  button9 = types.InlineKeyboardButton(text="Двойное яблоко 399р", callback_data="b9")
  button10 = types.InlineKeyboardButton(text="Клубника пиноколада 399р", callback_data="b10")
  button11 = types.InlineKeyboardButton(text="Банановое мороженное 399р", callback_data="b11")
  button12 = types.InlineKeyboardButton(text="Банан 399р", callback_data="b12")
  button13 = types.InlineKeyboardButton(text="Ананас-лимон 399р", callback_data="b13")
  button14 = types.InlineKeyboardButton(text="Манго-клубника 399р", callback_data="b14")
  button15 = types.InlineKeyboardButton(text="Манго лёд 399р", callback_data="b15")
  button16 = types.InlineKeyboardButton(text="Лесная ягода 399р", callback_data="b16")
  button17 = types.InlineKeyboardButton(text="Банан-папайя 399р", callback_data="b17")
  button18 = types.InlineKeyboardButton(text="Ванильное мороженное 399р", callback_data="b18")
  bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Выбрал: " + str(name))
  keyboard1.add(button1)
  keyboard1.add(button2)
  keyboard1.add(button3)
  keyboard1.add(button4)
  keyboard1.add(button5)
  keyboard1.add(button6)
  keyboard1.add(button7)
  keyboard1.add(button8)
  keyboard1.add(button9)
  keyboard1.add(button10)
  keyboard1.add(button11)
  keyboard1.add(button12)
  keyboard1.add(button13)
  keyboard1.add(button14)
  keyboard1.add(button15)
  keyboard1.add(button16)
  keyboard1.add(button17)
  keyboard1.add(button18)
  bot.send_message(message.chat.id, "✅Вы выбрали "+str(name)+".\n☘️Теперь выберите вкус:", reply_markup=keyboard1)

def buy(message):
  keyboard = types.InlineKeyboardMarkup()
  button1 = types.InlineKeyboardButton(text="Оплатить сейчас",url=site, callback_data="by")
  keyboard.add(button1)
  bot.send_message(message.chat.id, "✅Для оплаты нажмите на кнопку:", reply_markup=keyboard)

@bot.callback_query_handler(func=lambda call: True)
def callback_inline(call):
  message = call.message
  if call.message:
   if call.data == "button1":
      button(call.message, "Москва")
   elif call.data == "button2":
      button(call.message, "Воронеж")
   elif call.data == "button3":
      button(call.message, "Норильск")
   elif call.data == "button4":
      button(call.message, "Томск")
   elif call.data == "button5":
      button(call.message, "Краснодар")
   elif call.data == "button6":
      button(call.message, "Красноярск")
   elif call.data == "button7":
      button(call.message, "Иркутск")
   elif call.data == "button8":
      button(call.message, "Улан-Удэ")
   elif call.data == "button9":
      button(call.message, "Бийск")
   elif call.data == "button10":
      button(call.message, "Борисоглебцк")
   elif call.data == "button11":
        button(call.message, "Пермь")
   elif call.data == "button12":
      button(call.message, "Екатеринбург")
   elif call.data == "button13":
      button(call.message, "Сургут")
   elif call.data == "button14":
      button(call.message, "Сочи")
   elif call.data == "button15":
      button(call.message, "Ханты-Мансийский")
   elif call.data == "button16":
      button(call.message, "Абакан")
   elif call.data == "button17":
      button(call.message, "Оренбург")
   elif call.data == "button18":
      button(call.message, "Санкт-Петербург")
   elif call.data == "button19":
      button(call.message, "Устроиться на работу курьером")
   elif call.data == "red":
      red(call.message, "💨HQD CUVIE PLUS💨 (1200 тяг)")
   elif call.data == "blue":
      blue(call.message, "💨HQD KING💨 (2000 тяг)")
   elif call.data == "r1":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Тархун (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Тархун (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r2":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Кактусовый Лимонад (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Кактусовый Лимонад (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r3":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Клубника Питайя (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Клубника Питайя (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r4":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Клубничный Милкшейк (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Клубничный Милкшейк (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r5":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Лайм Кола (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Лайм Кола (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r6":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Ванильное мороженое (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Ванильное мороженое (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r7":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Банан (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Банан (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r8":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Клубника (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Клубника (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r9":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Мультифрукт (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Мультифрукт (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r10":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Черника (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Черника (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r11":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Манго гуава (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Манго гуава (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r12":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Яблоко (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Яблоко (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r13":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Энергетик (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Энергетик (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r14":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Арбузная жвачка (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Арбузная жвачка (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r15":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Розовый лимонад (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Розовый лимонад (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r16":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Ананас (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Ананас (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r17":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Виноград (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Виноград (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r18":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Ледяная мята (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Ледяная мята (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r19":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Черника-малина-виноград (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Черника-малина-виноград (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r20":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Йогурт лесные ягоды (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Йогурт лесные ягоды (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "r21":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD CUVIE PLUS💨 Малина-лимон (1200 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Малина-лимон (1200 тяг)\nК оплате: 299р.\nКоментарий: "+str(message.chat.id))
      buy(message)



   elif call.data == "b1":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Кола (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Кола (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b2":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Персик (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Персик (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b3":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Мохито (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Мохито (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b4":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Черника (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Черника (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b5":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Энергетик (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Энергетик (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b6":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Виноград (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Виноград (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b7":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨💨HQD KING💨 Мандарин (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Мандарин (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b8":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Клубника киви (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Клубника киви (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b9":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Двойное яблоко (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Двойное яблоко (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b10":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Клубника пиноколада (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Клубника пиноколада (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b11":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Банановое мороженное (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Банановое мороженное (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b12":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Банан (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Банан (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b13":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Ананас-лимон (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Ананас-лимон (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b14":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Манго-клубника (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Манго-клубника (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b15":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Манго лёд (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Манго лёд (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b16":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Лесная ягода (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Лесная ягода (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b17":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Банан-папайя (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Банан-папайя (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
   elif call.data == "b18":
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Оплачивает: 💨HQD KING💨 Ванильное мороженное (2000 тяг)")
      bot.send_message(message.chat.id, "Оплата-QIWI\nВы выбрали Ванильное мороженное (2000 тяг)\nК оплате: 399р.\nКоментарий: "+str(message.chat.id))
      buy(message)
@bot.message_handler(commands=['send'])
def notify(message):
    command_sender = message.from_user.id
    if command_sender in admins:
        with open(r'C:\id.txt') as ids:
            for line in ids:
                user_id = int(line.strip("\n"))
                try:
                    bot.send_message(user_id,  f'Если вашего города нету в списке, пишите сюда')
                except Exception as e:
                    bot.send_message(command_sender, f'ошибка отправки сообщения юзеру - {user_id}')
    else:
        bot.send_message(command_sender, f'у вас нет прав для запуска команды')


if __name__ == "__main__":
    try:
        bot.polling(none_stop=True)
    except Exception as e:
        pass

@bot.message_handler(content_types=['text'])
def echo_all(message):
      bot.send_message(id, str(message.chat.first_name) + " [ "+ str(message.chat.id)+" ] |Написал: " + str(message.text))
      bot.send_message(message.chat.id, "Вы что-то делаете не так, пожалуйста нажмите - /start")

