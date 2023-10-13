# esp32Cam
ESP32 CAM module 


**INTERFACING ESP32 CAM WITH ARDUINO UNO TO UPLOAD THE CODE**


![esp32CamWithArduinoUno](https://github.com/niteshnidarshan/esp32Cam/assets/8472412/4f874fb3-0bcd-4e95-928a-2095c85e0d2a)

From the above schematic diagram you can see that there are two jumper cables connected one is for ESP32CAM connected between GND and IO0, and another is for Arduino UNO GND and RESET pins. ESP32CAM module is powered from the Arduino UNO 5v and GND pins connected to same on ESPCAM. The data transfer pins UOT and UOR from the ESP32CAM are connected to TX and RX pins of Arduino respectively.

Thats it for connections now you can connect the Arduino UNO board to PC and follow the below steps to upload the code.

**Setting up Arduino IDE**
Download and install Arduino IDE on your PC, where Arduino UNO board is connected.

Now add ESP32 board manager by opening File -> Preferences and paste the below URL in the Additional boards manager URLs field.

https://dl.espressif.com/dl/package_esp32_index.json

Now open Tools -> Board:xxxxx -> ESP32 Arduino -> select : ESP32 Wrover module

Set the Tools menu settings as shown below
+ Board: “ESP32 Wrover Module” >
+ Upload Speed: “115200” >
+ Flash Frequency: “80MHz” >
+ Flash Mode: “Q10” >
+ Partition Scheme: “Huge APP (3MB No OTA/1 MB SPIFFS)” >
+ Core Debug Level: “None” >
+ Port: “COMx’ > According to your port connection

Uploading the code: ESP32CAM webserver
As an example lets use the code from the ESP32 Examples library by opening File -> Examples -> ESP32 -> Camera -> CameraWebServer. An example ready made code will be loaded, you just need to change the WiFi credentials in the code and click on Upload button.


After clicking on upload icon you can see the connecting dots as the above image, when you see them press the RST(Reset button) on the board which leads to code upload, with in few seconds you will see the message “Done uploading” on status bar of Arduino IDE means code uploaded successfully.

Now remove the jumper connection between GPIO1(IO0) and GND on ESP32 CAM module. Open serial monitor and set the baud rate to the value which we mentioned in the code i.e., 115200 and press RST button on the ESP cam board.

Now you can see the IP address of the webserver from where we can access the ESP32 CAM features, camera etc. 


documentation credit: https://www.circuitschools.com/how-to-program-upload-the-code-to-esp32-cam-using-arduino-or-programmer/#:~:text=As%20we%20already%20learnt%20ESP32,converters%20such%20as%20FTDI%20programmer.

Arduino IDE -> prefrences -> Additional board manager URLs:
http://arduino.esp8266.com/stable/package_esp8266com_index.json
https://dl.espressif.com/dl/package_esp32_index.json
https://github.com/adamvr/arduino-base64/blob/master/library.properties
https://github.com/ambiot/ambpro2_arduino/raw/main/Arduino_package/package_realtek.com_amebapro2_index.json
https://github.com/espressif/arduino-esp32/blob/master/libraries/ESPmDNS/library.properties
https://github.com/espressif/arduino-esp32/blob/master/package.json
https://github.com/khoih-prog/FTPClient_Generic/blob/main/library.json
https://github.com/khoih-prog/FTPClient_Generic/blob/main/library.properties
https://github.com/me-no-dev/ESPAsyncWebServer/blob/master/library.json
https://github.com/witnessmenow/Universal-Arduino-Telegram-Bot/blob/master/library.json
https://github.com/zhouhan0126/WIFIMANAGER-ESP32/blob/master/library.json
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_dev_index.json
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
