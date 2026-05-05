# 🚀 WhatsApp Automation Using Python  
### 📱 GUI-Based WhatsApp Message Sender (Tkinter)

Automate sending WhatsApp messages using Python with a simple graphical interface.  
This project uses **Tkinter** for GUI and **pywhatkit** to send scheduled messages via WhatsApp Web.

---

## ✨ Features

- 📱 Send WhatsApp messages automatically  
- ⏰ Schedule messages at a specific time  
- 🖥️ Easy-to-use GUI (no terminal needed)  
- 🌐 Works with WhatsApp Web  
- ⚡ Lightweight and beginner-friendly  

---

## 🛠️ Tech Stack

- Python  
- Tkinter (GUI)  
- pywhatkit  
- pyautogui  
- pynput  

---

## 📦 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/whatsapp-automation.git
cd whatsapp-automation
2. Install Dependencies
pip install pywhatkit pyautogui pynput

⚠️ Tkinter usually comes pre-installed with Python

🔑 Prerequisites
✅ Python 3.x installed
✅ Logged into WhatsApp Web in your browser
✅ Stable internet connection
✅ Keep browser open while sending message
▶️ How to Run
python app.py
🖥️ Usage
Enter receiver's phone number with country code (e.g., +91XXXXXXXXXX)
Type your message
Set the time (hour & minute)
Click Send Message

➡️ WhatsApp Web will open automatically and send your message at the scheduled time.

💻 Source Code
import pywhatkit
import tkinter as tk
from tkinter.ttk import *

def send_whatsapp_message():
    number = phoneNumber.get()
    msg = message.get()
    hour = hours.get()
    minute = minutes.get()
    pywhatkit.sendwhatmsg(number, msg, hour, minute)

master = tk.Tk()
master.geometry("700x300")
master.configure(bg='#25D366')
master.title("WhatsApp Message Sender")

tk.Label(master, text='Enter Phone Number (+91):',
         font=('calibre',10,'bold'), bg='#25D366', fg='white').grid(row=0)

tk.Label(master, text='Enter Message:',
         font=('calibre',10,'bold'), bg='#25D366', fg='white').grid(row=1)

tk.Label(master, text='Hour:',
         font=('calibre',10,'bold'), bg='#25D366', fg='white').grid(row=2)

tk.Label(master, text='Minute:',
         font=('calibre',10,'bold'), bg='#25D366', fg='white').grid(row=3)

phoneNumber = tk.StringVar()
message = tk.StringVar()
hours = tk.IntVar()
minutes = tk.IntVar()

tk.Entry(master, textvariable=phoneNumber).grid(row=0, column=1)
tk.Entry(master, textvariable=message).grid(row=1, column=1)
tk.Entry(master, textvariable=hours).grid(row=2, column=1)
tk.Entry(master, textvariable=minutes).grid(row=3, column=1)

style = Style()
style.configure('TButton', font=('calibri', 15, 'bold'), borderwidth=4)
style.map('TButton',
          foreground=[('active', 'green')],
          background=[('active', 'black')])

Button(master, text='Send Message', command=send_whatsapp_message)\
    .grid(row=4, column=1)

tk.mainloop()
📸 Screenshots
🟢 GUI Interface

🟢 Enter Details

⚠️ Important Notes
Do not close the browser before the message is sent
Ensure correct time format (24-hour format recommended)
Phone number must include country code
🚀 Future Enhancements
📂 Send images/files
👥 Bulk messaging support
📇 Contact list integration
🎨 Improved UI (Dark Mode, Themes)
📄 License

This project is open-source and available under the MIT License.

🙌 Contributing

Contributions are welcome!
Feel free to fork this repo and submit a pull request.
