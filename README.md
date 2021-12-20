# whatsappBot

import pywhatkit as kit


class WhatsappBot:
    def __init__(self, phone_number, message, hours, minutes):
        self.phone_number = phone_number
        self.message = message
        self.hours = hours
        self.minutes = minutes

    def send_message(self):
        try:
            kit.sendwhatmsg(self.phone_number, self.message, self.hours, self.minutes)
            print("Message sent successfully")
        except:
            print("Error sending messages")

msg_sender = WhatsappBot("+13095699705", "Good morning.", 12, 45)

msg_sender.send_message()

msg_receiver = WhatsappBot("+12243231834", "Good morning", 12, 46)



# kit.sendwhatmsg("+3128381977", "Welcome to python", 22, 24)ex
