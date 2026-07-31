# JVmeteo
JVmeteo COREON --- Weather station with support for pressure, temperature and humidity sensors, MQ-9 CO sensor and MPU6050 gyroscope

JVmeteo COREON verze HARDWARE 1.1JOHN

www.jvelektronika.cz
-
-
JVmeteo COREON HW 1.1JOHN a FIRMWARE 1.0

Aktuální vydání verze HW 1.1JOHN a FIRMWARE v 1.0

FW 1.0

-Podpora senzorů: BME280, BMP280, DHT22, MQ-9, MPU6050

-Uživatelská volba komunikačních pinů pro senzory I2C a ANALOG

-Obrazovka nastavení ( 2x stisk tlačítka RESET vytvoří na omezenou dobu WiFi síť -pevně nastavená IP adresa)

-V obrazovce nastavení lze změnit WiFi síť na kterou se JVmeteo připojuje, díky tomu je snadno přenositelný. Dále možnost vkládání API klíče pro zápis na thingspeak

-Optimalizovaná spotřeba pro solární panel, data se odesílájí každých 90s a poté se čip přepne do úsporného režimu.


HW 1.1JOHN

-Multi přepínač funkcí/nastavení

-USB C pro plnohodnotnou datovou komunikaci pomocí CP2102

-Druhé USB C pro připojení externího napájení/nabíjení akumulátoru

-Nově indikační led pro napětí 3,3V pro ESP

-Nově možnost externích indikačních 3mm led (vyjma indikace externího napájení z USB C)

-
-
-

PŘEDNÍ STRANA

<img width="1290" height="1230" alt="JVmeteo COREON" src="https://github.com/user-attachments/assets/1137029f-f17a-42b6-85e4-a4bb4146cd74" />

ZADNÍ STRANA

<img width="1090" height="1060" alt="JVmeteo COREON záda" src="https://github.com/user-attachments/assets/20b7ff2d-3e46-4227-a7c5-ac6c290ca4c3" />

TESTOVÁNÍ

<img width="1634" height="1674" alt="test1" src="https://github.com/user-attachments/assets/ad9c964d-e09f-481a-8516-1bb120afa471" />

<img width="4000" height="3000" alt="test2" src="https://github.com/user-attachments/assets/c6121d56-ed14-4a50-90ee-dc24416d29e1" />

<img width="832" height="1160" alt="obrazovka nastavení" src="https://github.com/user-attachments/assets/aae2610a-f4be-40f0-87ba-a9d745ad5831" />

<img width="486" height="552" alt="nastavení" src="https://github.com/user-attachments/assets/4c35a343-d1b7-4b31-be72-17850eb19204" />

31.7. 2026

Czech Republic

KNIHOVNY, KTERÉ JE POTŘEBA STÁHNOUT PŘED NAHRÁNÍM FIRMWARE

#include <WiFi.h>

#include <WebServer.h>

#include <WiFiClient.h>

#include <Wire.h>

#include <Preferences.h>

#include "ThingSpeak.h" // Oficialni knihovna pro bezpecny prenos dat


// Knihovny pro senzory

#include <Adafruit_Sensor.h>

#include <Adafruit_BME280.h>

#include <Adafruit_BMP280.h>

#include <Adafruit_MPU6050.h>

#include <DHT.h>

