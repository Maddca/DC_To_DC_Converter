# DC-to-DC-Converter
## Overview
This is a DC-to-DC Converter Design for Walla Walla University's Power Electronics Course. The goal of this project was to create a 12-15V to 5V DC converter in order to be able to charge a phone from a voltage source ranging from 12-15V.
## Design Specifications
1. Takes a 12-15V input and outputs a 5V
2. Is able to charge both Android Devices as well as Iphones
3. Able to handle any 12-15V that might be used. (Up to 3A)
4. Power efficiency of atleast 80%
5. Small Board Size (less than10cm x 10cm)
6. Costs less than $25


## Schematic
### Buck Converter
<img width="940" alt="12-15V to 5V DC Buck Converter" src="https://user-images.githubusercontent.com/103593959/172689317-0575e362-160b-45d4-ad98-937e967e6ca4.png">
Shown above is the final schematic for our project. Our input is delived from a 12-15V source to the screw terminal. For our final version we used a set of 8 AA batteries to generate 12V into the screw terminal. The input then passes a ferrite bead in order to limit noise coming from the input. It then passes into a LM25765-5 Buck Converter. The LM25765 works as a simple switcher in conjuction with our inductor and schottky diode in order to create an average duty cyle resulting in 5V. From the USB 5V are generated with a current ranging from about 20-30mA. This is entirely dependent on what kind of battery you use. The converter itself is designed to handle up to 3A so you are able to charge your phone with a car battery.
### Data Pin Voltage Divider
<img width="629" alt="Data Pin Voltage Divider" src="https://user-images.githubusercontent.com/103593959/172690697-4c113191-cb47-44f4-89cb-d85b8f5cc583.png">
5V is passed into a voltage divider, in order to use the data pins on the USB output. This is required to charge Apple Devices.

## PCB Design
<img width="736" alt="Battery Phone Charger" src="https://user-images.githubusercontent.com/103593959/172690922-350a5b45-ab1b-46ce-9866-4cf9ffeabde6.png">
Shown above is the lastest PCB design. Of interest is the particularly wide track width, which is required because of our design specification of being able to handle at least 3A. Besides that parts, besides the voltage divider for the data pins, have been picked to handle no less than 3A.

## Simulations

## Results
