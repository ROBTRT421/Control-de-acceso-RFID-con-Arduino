# Video: https://youtube.com/shorts/hkY7HuaxGY0?feature=share


# Tutorial
1. Obtenga las piezas, instale [Arduino IDE] (https://www.arduino.cc/en/Main/Software), instale los controladores para Arduino (si tiene un clon de Arduino Y está utilizando Windows)
2. Copie y pegue [el código](https://github.com/ROBTRT421/Control-de-acceso-RFID-con-Arduino/blob/main/control_de_acceso_rfid.ino) en la IDE de Arduino
3. Instalar la librería 'MFRC522' 'Servo' 'SPI' usando Arduino IDE [Library Manager](https://www.arduino.cc/en/Guide/Libraries#toc2)
4. Conecte todo _(vea el diagrama de cableado)_
5. Conecte su Arduino y selecciónelo en 'Tools > Board' y 'Tools > Port'
6. Carguielo a la placa
7. _(opcional)_ Modifica las variables, explora el código :guiño:


# Partes
Part Name            |      Amazon link       | Note
:------------------- | ---------------------- | :------------------------------------------------
Arduino UNO  (clone) | https://shre.ink/HqM3
LED's                | https://shre.ink/HqMl
Resistencias 220oms  | https://shre.ink/HqYu 
RFID-RC522           | https://shre.ink/HqYp
Some wires           | https://www.amazon.com/s?k=arduino+wires | 12 wires needed
Micro Servo SG90     | https://shre.ink/Hq4E | 
Breadboard           | https://www.amazon.com/s?k=arduino+breadboard | 



# Wiring diagram
Pin           | Arduino UNO
:------------ | :------------------
RC522 SDA     | 10
RC522 SCK     | 13
RC522 MOSI    | 11
RC522 MISO    | 12
RC522 RST     | 9
Led Rojo      | 5
Led verde     | 4
Servo         | 3


![wiring diagram]( https://github.com/ROBTRT421/Control-de-acceso-RFID-con-Arduino/blob/main/Plano%20RFID.png "wiring diagram")

El orden exacto de los pines para el RC522 o el SERVO puede ser diferente del que se muestra en la imagen, así que sea inteligente y use la tabla anterior.

# IMPORTANTE
Todas los tags de acceso, ya vienen configuradas de fabrica, para poder darles el acceso desde el IDLE de Arduino hay
que configurarlas, en la linea 16 y 17 del codigo vienen los tags de acceso, basta con abrir el "serial monitor" una vez desarrollado el proyecto leer la tarjeta y de forma manual, poner el "Card UID" del tag en las lineas del codigo antes mencionadas 
EJEMPLO : {0xC1, 0xBB, 0x7E, 0x21}; ese es el tag que viene en el codigo y ustedes solo modificaran los ultimos dos digitos con los que 
viene su tag configurado.




