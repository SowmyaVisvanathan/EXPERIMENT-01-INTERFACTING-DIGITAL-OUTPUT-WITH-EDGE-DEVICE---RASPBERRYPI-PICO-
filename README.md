# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---RASPBERRYPI-PICO-
## NAME: Sowmya V
## DEPARTMENT: CSE(IoT)
## ROLL NO: 212222110045
## DATE OF EXPERIMENT: 24-02-25

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

APPARATUS REQUIRED
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
Computer with Thonny IDE
## THEORY
Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.

Digital Output refers to controlling external devices like LEDs, buzzers, or relays using GPIO (General Purpose Input Output) pins. A GPIO pin can be set to HIGH (3.3V) or LOW (0V) to turn the device ON or OFF.

## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython)
### 1. 
```
from machine import Pin
from utime import sleep
print("Pi Pico")
led=Pin(0,Pin.OUT)
while True:
  led.Toggle()
  sleep(0.5)
```
### 2.
```
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
led2=Pin(3,Pin.OUT)
led3=Pin(9,Pin.OUT)
while True:
  led1.toggle()
  sleep(0.5)
  led2.toggle()
  sleep(0.5)
  led3.toggle()
  sleep(2)
```
### 3.
```
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
led2=Pin(3,Pin.OUT)
led3=Pin(9,Pin.OUT)
buzzer=Pin(9,Pin.OUT)
while True:
  led1.toggle()
  sleep(0.5)
  led2.toggle()
  sleep(0.5)
  led3.toggle()
  buzzer.toggle()
  sleep(2)
```
## OUPUT 
### 1. 
![Screenshot 2025-02-24 103935](https://github.com/user-attachments/assets/5e021560-f585-4fba-8df5-8a7489dad22d)

### 2.
![Screenshot 2025-02-24 104812](https://github.com/user-attachments/assets/c042048f-e48a-43d5-a4eb-11fda7de4c0a)

### 3.
![Screenshot 2025-02-24 111856](https://github.com/user-attachments/assets/fff9224e-ab21-4a12-b990-46dbc6d61337)

## RESULTS
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at 1-second intervals, confirming the proper interfacing of a digital output.
