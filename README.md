# Cybersecurity 150 Lab

## Name of Project
Metro-ESP32 Cool WhatsApp Project

## Purpose
Send messages through a WhatsApp API to my personal number.

## Equipment
* [Metro-ESP32](https://www.adafruit.com/product/4775)

* [USB-C Cable](https://www.adafruit.com/product/4473?gad_source=1&gclid=Cj0KCQjw2PSvBhDjARIsAKc2cgMPclKTXZy_pNRaR5M0IUoAdL4i_ZRS04h3fJkgNfEqf-jbmhlW_jYaAn4UEALw_wcB)

## Link to Documentation Followed
- [Random Nerd Tutorials – ESP32: Send Messages to WhatsApp](https://randomnerdtutorials.com/esp32-send-messages-whatsapp/)

##### Youtube Video 1: https://www.youtube.com/watch?v=roMjPoaFAZ8&t=2s

##### Youtube Video 2: https://www.youtube.com/watch?v=UvXTB-bi4Sw&t=87s

##### Other Links: 
https://www.reddit.com/r/esp32/comments/tks9k3/download_mode/
https://docs.arduino.cc/tutorials/generic/DriverInstallation/
https://forum.arduino.cc/t/a-fatal-error-occurred-failed-to-connect-to-esp32-no-serial-data-received/1185060/9

## Steps I followed
1.	Download Arduino
2.	Install Esp32 Tool from library
3.	Add the number: +34 632 331 709 to your contacts in WhatsApp and text: “I allow callmebot to send me messages”
4.	Install URLEncode from library.
5.	Write/Paste code on Arduino and insert your network credentials/API Key/Phone Number- where it is prompted.
6.	Select the correct board and port to use (In my case: Adafruit Metro ESP32-S2 | Port: COM6)
7.	**Recheck** your input and make sure it is correct. When finished- run the program
8.	Check WhatsApp for API Bot message. (Should send after a few seconds of uploading)

## Problems
1. Program tried to run without any drivers. I installed a universal driver: | Failed | Error 2: No serial data received. 
2. Same error. Reset the Metro-ESP32-S2 board, plugged it in and out, checked to see for any broken hardware issues. None found.
3. Only COM1 Port available, switched to upload mode to use COM4 port. Did not work either | Error 1: Wrong chip?
4. Incorrectly selected board was switched from DEVKIT to Deneyap Mini and used COM3 Port | Error: Potentially hardware/driver erorr
6. The Metro-32-S2 repeats error code 2, so I connected to Port COM6 (Adafruit Metro ES32-S2) successfully.
7. Wrong chipset error. Selected Adafruit Metro ESP32-S2 as the board.
8. The board refused to connect to my computer. After observing the SSID/Passwd I connected to a new router successfully.
9. The board reported a wrong chipset. I manually reset the hash on the Metro-32-S2 and it worked!
    
    Final Answer: Select the exact board that you have, reset the board and select the correct port. Once the correct options have been selected run the code. Double check code and ports religiously.
