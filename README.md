Abstract

Temperature Control Fan


This project presents the design and implementaƟon of a Temperature
Controlled Fan system using the 8051 Microcontroller. The system is aimed at
automaƟcally regulaƟng the speed of a fan in response to changes in ambient
temperature, thereby ensuring energy efficiency and user convenience.

In this design, the LM35 temperature sensor conƟnuously measures the
surrounding temperature and produces an Analog voltage proporƟonal to it. This
signal is converted into a digital value using the ADC0804, which is then
processed by the 8051 Microcontroller. Based on the programmed temperature
thresholds, the microcontroller controls the fan speed through a driver circuit
consisƟng of an optocoupler and MOSFET, ensuring safe switching of the motor.
The current temperature and fan status are also displayed on an LCD module for
real-Ɵme monitoring.

The system automaƟcally increases fan speed when the temperature rises and
decreases or turns off the fan when the temperature falls below the threshold.
This makes it highly useful in Home appliances, computer cooling units, and
industrial automaƟon, where maintaining opƟmal temperature is essenƟal. The
project demonstrates effecƟve integraƟon of sensor technology, Analog-todigital conversion, microcontroller programming, and motor control, all
implemented on a PCB for pracƟcal applicaƟon.


| Component                | Connection                              |
| ------------------------ | --------------------------------------- |
| **LM35 VCC**             | +5V                                     |
| **LM35 GND**             | GND                                     |
| **LM35 OUT**             | ADC0804 analog input                    |
| **ADC0804 D0–D7**        | AT89C51 Port 1 (P1.0–P1.7)              |
| **ADC0804 control pins** | AT89C51 Port 3                          |
| **AT89C51**              | +5V and GND                             |
| **Crystal**              | XTAL1 & XTAL2 with 33 pF capacitors     |
| **L293D input**          | AT89C51 output/control pin              |
| **L293D output**         | DC fan                                  |
| **L293D logic supply**   | +5V                                     |
| **Fan supply**           | External supply according to fan rating |
| **All GNDs**             | Common ground                           |
