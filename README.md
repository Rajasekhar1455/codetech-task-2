COMPANY: CODTECH IT SOLUTIONS

NAME:KINTALI RAJASEKHAR

INTERN ID:CT04DF1855

DOMAIN: Embedded Systems

DURATION: 4 WEEKS

MENTOR: Neela Santhosh Kumar# codetech-task-2

DESCRIPTION : HC-05 Blutooth ModuleHi-Link (5V) 5V Relay - 4 Nos ATMEGA328P IC 28 Pin IC Base 16 Mhz Crystal Oscillator BC547 Transistor - 4 Nos 22pF Capacitor - 2 NosLED 5mm - 5 Nos IN4007 Diode - 5 Nos 1K Resistor - 9 Nos 2 Pin Screw Connector 3 Pin Screw Connector - 4 Nos TOOLS NEEDED Soldering Iron Soldering Wire FluxConnect Arduino Uno on PC Open Arduino IDE (Software) Then Go To Tools>Board>Select Arduino UnoSelect Correct Port Upload code below.

CIRCUIT DIAGRAM:
![image](https://github.com/user-attachments/assets/c47882ff-e65c-4595-a81e-2709458ef685)

CODE :

/* Relay IN1 connected to PinOut 2 Arduino Relay IN2 connected to PinOut 3 Arduino Relay IN3 connected to PinOut 4 Arduino Relay IN4 connected to PinOut 5 Arduino --->you can connected to relay modul 4 channel Serial data sending from Arduino Bluetooth Relay 4CH.apk data '1'-'4' to on is Ralay CH 1-4 data 'A'-'D' to off is Ralay CH 1-4 data '9' to on ALL CH 1-4 data 'I' to off ALL CH 1-4 */

#define relay1 2 #define relay2 3 #define relay3 4 #define relay4 5 char val; void setup() { pinMode(relay1,OUTPUT); pinMode(relay2,OUTPUT); pinMode(relay3,OUTPUT); pinMode(relay4,OUTPUT); digitalWrite(relay1,LOW); digitalWrite(relay2,LOW); digitalWrite(relay3,LOW); digitalWrite(relay4,LOW); Serial.begin(9600); Serial.begin(9600); } void loop() { //cek data serial from bluetooth android App if( Serial.available() >0 ) { val = Serial.read(); Serial.println(val); } //Relay is on if( val == '1' ) { digitalWrite(relay1,HIGH); } else if( val == '2' ) { digitalWrite(relay2,HIGH); } else if( val == '3' ) { digitalWrite(relay3,HIGH); } else if( val == '4' ) { digitalWrite(relay4,HIGH); } //relay all on else if( val == '9' ) { digitalWrite(relay1,HIGH); digitalWrite(relay2,HIGH); digitalWrite(relay3,HIGH); digitalWrite(relay4,HIGH); } //relay is off else if( val == 'A' ) { digitalWrite(relay1,LOW); } else if( val == 'B' ) { digitalWrite(relay2,LOW); } else if( val == 'C' ) { digitalWrite(relay3,LOW); } else if( val == 'D' ) { digitalWrite(relay4,LOW); } //relay all off else if( val == 'I' ) { digitalWrite(relay1,LOW); digitalWrite(relay2,LOW); digitalWrite(relay3,LOW); digitalWrite(relay4,LOW); } }

OUTPUT:
![image](https://github.com/user-attachments/assets/0c4f0eb3-3130-41fd-9f7c-221e0e160f74)
![image](https://github.com/user-attachments/assets/6ce5550f-a07b-4a35-8db2-3e40a95dbe05)

![image](https://github.com/user-attachments/assets/28cd0469-38ef-4519-a10c-3565dc0a67a3)

WORKING DEMO :

https://www.youtube.com/watch?v=OmyzJ_P9TJs



