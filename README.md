# EXPERIMENT--01-INTERFACING-DIGITAL-INPUT-SENSOR-WITH-ARDUINO-PIR-SENSOR
EXPERIMENT -01  INTERFACING DIGITAL INPUT SENSOR WITH ARDUINO PIR SENSOR

# Name:RAMKUMAR S
# Reg no:212225240115

## AIM: 

To interface a digital input sensor (PIR Sensor )with arduino .

## COMPONENTS REQUIRED:


1.      Arduino Uno

2.     Bread board

3.      Tinker cad

## ALGORITHM:

 STEP 1:  Start the program, declare an integer variable sensorstate and initialize it to 0.
 
STEP 2: Configure digital pin 2 as INPUT and the built-in LED pin as OUTPUT.

STEP 3:  Initialize serial communication at 9600 baud rate. Read the PIR sensor output using digitalRead(2). 

STEP 4:  If the sensor output is HIGH, turn ON the built-in LED and display "Sensor activated" on the Serial Monitor. 

STEP 5:  Otherwise, turn OFF the built-in LED

STEP 6:  Repeat the process continuously.

## PROCEDURE:
  1. Connect the VCC pin of the PIR sensor to 5V, GND pin to GND, and OUT pin to digital pin 2 of Arduino. 
  
  2. Connect the Arduino to the computer using a USB cable.
  
  3. Open the Arduino IDE, type the given program, verify and upload it to the Arduino board. 
  
  4. Open the Serial Monitor and set the baud rate to 9600.
  
  5. Move in front of the PIR sensor and observe the output. 
 
  6. When motion is detected, the built-in LED glows and the message "Sensor activated" is displayed on the Serial Monitor. 
  
  7.When no motion is detected, the LED turns OFF.

## PROGRAM:

```C++
int sensorstate = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  sensorstate = digitalRead(2);
  
  if (sensorstate == HIGH) { 
    digitalWrite(LED_BUILTIN, HIGH);
    Serial.println("Sensor activated");
  }
  else
  {
    digitalWrite(LED_BUILTIN, LOW); // Fixed: Corrected 'LED_BUILTN' typo
  }
  delay(10);
}
```

## OUTPUT:

Led ON Working state:


<img width="601" height="632" alt="Screenshot 2026-10-13 143100" src="https://github.com/user-attachments/assets/afa4205d-f015-4215-80a7-977bf2121921" />


## RESULT:

Thus,To interface a digital input sensor (PIR Sensor )with arduino was executed successfully and the output is verified.
