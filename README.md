# Cybersecurity 150 Lab

## Name of Project
Metro-ESP32 Cool Whatsapp Project

## Purpose
Send messages through a WhatsApp API to my personal number

## Equipment
* [Metro-ESP32](https://www.adafruit.com/product/4775)

* [USB-C Cable]([https://www.amazon.com/AmazonBasics-Male-Micro-Cable-Black/dp/B0711PVX6Z/ref=sr_1_1_sspa?keywords=micro+usb+data+cable&qid=1678902214&sprefix=Micro+USB+data+%2Caps%2C89&sr=8-1-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUFaU0NaUVZHU1RFUlAmZW5jcnlwdGVkSWQ9QTA3NTA4MDVFVERCS01HVlgxM1YmZW5jcnlwdGVkQWRJZD1BMDE4NTE1NTIwWUdONkdWSzU1M1Amd2lkZ2V0TmFtZT1zcF9hdGYmYWN0aW9uPWNsaWNrUmVkaXJlY3QmZG9Ob3RMb2dDbGljaz10cnVl](https://www.amazon.com/Amazon-Basics-Charger-480Mbps-Certified/dp/B01GGKYN0A/ref=sr_1_3?dib=eyJ2IjoiMSJ9.mkihZngY79OjjbASVIN5LnN4ad3WnVomzBC10k2Gco1iaQnyiP4agXKSJ8MKO_p8gn8rIOSr1EW1fUm3ciHb2i0MJD8jdvT5U3UJWX5CzeLYCuWiti6wiwNxBIqA-Kz1AUtydxY8bNrRwttDzJQ7Z4heTDw-H3vg6ILujh5BS41Rezf5UUnK66wEKh62uo57oKPMXrS-iGe9je7yN-pvlo9B5Nmdi3-WY_zVf9YUWWk._Zwkwy7zGDw5EoecQ4NYrfINuaABK_1rdfur1aNkwhY&dib_tag=se&hvadid=616989603041&hvdev=c&hvlocphy=9004164&hvnetw=g&hvqmt=e&hvrand=3184443193745420175&hvtargid=kwd-410290141842&hydadcr=19109_13454446&keywords=amazon+usb+c+cables&qid=1710971786&sr=8-3))

## Link to Documentation Followed
- [Random Nerd Tutorials – ESP32: Send Messages to WhatsApp]([https://github.com/martin-ger/esp32_nat_router](https://randomnerdtutorials.com/esp32-send-messages-whatsapp/))

##### Youtube Video 1: https://www.youtube.com/watch?v=roMjPoaFAZ8&t=2s

##### Youtube Video 2: https://www.youtube.com/watch?v=UvXTB-bi4Sw&t=87s

##### Other Links: 
https://docs.arduino.cc/tutorials/generic/DriverInstallation/
https://forum.arduino.cc/t/a-fatal-error-occurred-failed-to-connect-to-esp32-no-serial-data-received/1185060/9

## Steps I followed
1. 1.	Download Arduino
2.	Install Esp32 Tool from library
3.	Add the number: +34 632 331 709 to your contacts in WhatsApp and text: “I allow callmebot to send me messages”
4.	Install URLEncode from library.
5.	Write/Paste code on Arduino and insert your network credentials/API Key/Phone Number- where it is prompted.
6.	Turn on Upload Mode
7.	Select COM3 Port
8.	Follow the code, when finished run the program

## Problems
1. Program tried to run without any drivers. I installed a universal driver: | But it did not work | Error 2: No serial data received. 
2. Same error. Reset the Metro-ESP32-S2 board, plugged it in and out, checked to see for any broken hardware issues. None found.
3. Only COM1 Port available, switched to upload mode to use COM4 port. Did not work either | Error 1: Wrong chip?
4. Incorrectly selected board was switched from DEVKIT to Deneyap Mini and used COM3 Port | Error: Potentially hardware/driver erorr
5. Final Answer: On a clean wipe, or separate machine, re-install Arduino & tools respectively and rerun the code again in upload mode.

Example
1. Arduino code will not load on ESP32 Cam.
   Answer: Camera drivers were incorrect I needed to install the driver: [https://www.wch-ic.com/downloads/CH341SER_ZIP.html](https://github.com/martin-ger/esp32_nat_router).  I used file, "CH341SER.ZIP" and it worked.
