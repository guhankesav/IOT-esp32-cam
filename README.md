# IOT-esp32-cam
## Smart Door Lock System using esp32-cam and Telegram chatbot 


Home automation gives you access to control devices in your home from a mobile device anywhere in the world. One of the biggest advantages of home automation is that it keeps your abode safe, and prevents accidental fires, water leaks, gas leaks, and other disasters. This project shows how we can use Telegram in our IoT and Home Automation projects. Home Security System using ESP32 CAM which will notify us on Telegram App about person entering the house by capturing and sending his photo to us and Door can be controlled by chatbot. With this project we can take multiple photos, unlock and lock the door from anywhere in the world with the Telegram app.

## Version 1: [Code](esp32cam_telegram_smart_door_lock.ino)

When anyone presses the doorbell, home owner  will get a notification in the telegram app with a photo of that person. After that, we can easily unlock and lock the door from the telegram app.





## Version 2: [Code](esp32-cam_Facerecognition_and_telegram_smartlock.ino)

Some images of authorized people are registered in the esp32-cam with SD card .

when someone is at the door , if the person is recognizable by the esp32cam as an authorized user then Door unlocks , else capture and send an image of the person to the home owner and let him / her take the decision.

## Flowchart :
![Flowchart](flowchart.png)


##  Demo : 

Click on the image below for demo
[![Watch the video](https://img.youtube.com/vi/Woi7MhA4UIs/maxresdefault.jpg)](https://youtu.be/Woi7MhA4UIs)


### Changes to be made to reuse the code :

#### Importing Libraries
Start by importing the required libraries.
```ino
#include <Arduino.h>
#include <WiFi.h>
#include <WiFiClientSecure.h>
#include "soc/soc.h"
#include "soc/rtc_cntl_reg.h"
#include "esp_camera.h"
#include <UniversalTelegramBot.h>
#include <ArduinoJson.h>
```
#### Network Credentials
Insert your network credentials in the following variables.
```ino
const char* ssid = "REPLACE_WITH_YOUR_SSID";
const char* password = "REPLACE_WITH_YOUR_PASSWORD";
```

#### Telegram User ID
Insert your chat ID. The one you’ve got from the IDBot.
```ino
String CHAT_ID = "XXXXXXXXXX";
```



#### Telegram Bot Token
Insert your Telegram Bot token you’ve got from Botfather on the BOTtoken variable.
```ino
String BOTtoken = "XXXXXXXXXX:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX";
```
