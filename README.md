```
___  ___  ___  __   _______ _   _ __   _________   _______  
|  \/  | / _ \ \ \ / /  _  | \ | |\ \ / /  _  \ \ / /  _  | 
| .  . |/ /_\ \ \ V /| | | |  \| | \ V /| | | |\ V /| | | | 
| |\/| ||  _  | /   \| | | | . ` | /   \| | | |/   \| | | | 
| |  | || | | |/ /^\ \ \_/ / |\  |/ /^\ \ \_/ / /^\ \ \_/ / 
\_|  |_/\_| |_/\/   \/\___/\_| \_/\/   \/\___/\/   \/\___/  
                                                            

```

# ESP8266 LCD Clock (Wi-Fi + NTP)

This project is a **custom-character big digit LCD clock** using an **ESP8266 NodeMCU** with **I2C LCD**.  
The time is fetched from the internet via **NTP** and automatically adjusted for **India Standard Time (UTC+5:30)**.  
It also supports:
- **12-hour format with AM/PM**
- **Custom greetings based on time of day**
- **Multiple Wi-Fi credentials for reliable connection**

![lcd2](https://github.com/user-attachments/assets/0217db36-2466-49df-b1bf-2aa55778d2b4)
![lcd](https://github.com/user-attachments/assets/1a481b98-79e7-4f9b-aa1b-20703cc2c927)
<img width="2490" height="1650" alt="circuit-diagram (9)" src="https://github.com/user-attachments/assets/649b6509-bbd8-421f-87d2-976b3dc93f21" />



---

## ✨ Features
- Large custom-digit display using LCD’s CGRAM.
- Time updates from NTP every minute.
- Greets user with:
  - `Good Morning` (6 AM to 12 PM)
  - `Good Afternoon` (12 PM to 10 PM)
  - `Good Night` (10 PM to 6 AM)
- Multiple stored Wi-Fi credentials — automatically connects to first available.
- Neatly arranged clock layout so AM/PM fits perfectly.

---

## 🛠 Hardware Required
- **ESP8266 NodeMCU**
- **I2C LCD Display** (20x4 recommended)
- USB cable & power supply
- Internet access

---

## 📦 Libraries Required
Install these libraries via Arduino IDE’s **Library Manager**:
- `ESP8266WiFi.h`
- `NTPClient.h`
- `WiFiUdp.h`
- `Wire.h`
- `LiquidCrystal_I2C.h`

---

## ⚡ How It Works
1. ESP8266 tries to connect to one of the stored Wi-Fi credentials.
2. Fetches time from NTP server (`pool.ntp.org`) with India time offset.
3. Displays the time in big digits on the LCD.
4. Shows a greeting message based on the hour of the day.
5. Refreshes every second for real-time updates.

---

## 🔧 Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/MaxonXOXO/CustomLCD.git
   ```
2. Open the `.ino` file in Arduino IDE.
3. Replace Wi-Fi credentials in the code:
   ```cpp
   #define WIFI_SSID_1 "YourFirstSSID"
   #define WIFI_PASSWORD_1 "YourFirstPassword"
   ```
4. Upload the code to your ESP8266.
5. Connect your I2C LCD to the correct pins and power up.

---

## 📷 Example Output
```
Good Morning
 08:45 AM
```

---

## 📜 License
This project is licensed under the MIT License — feel free to modify and share. 

---

**Made with ❤️ by MAXONXOXO**!


