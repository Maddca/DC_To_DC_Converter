# Portable Battery Phone Charger
This project was done in collaboration with [Taylor Smith](https://github.com/TaylorSmith28).
## Overview
This is a Portable Battery based Phone Charger Design for Walla Walla University's Power Electronics Course. The goal of this project was to create a 12-15V to 5V DC converter in order to be able to charge a phone from a voltage source ranging from 12-15V.
## Design Specifications
1. Takes a 12-15V input and outputs a 5V
2. Is able to charge both Android Devices as well as Iphones
3. Able to handle any 12-15V source that might be used. (Up to 3A)
4. Power efficiency of atleast 80%
5. Small Board Size (less than 10cm x 10cm)
6. Costs less than $25

## Schematic

### Buck Converter
<img width="940" alt="12-15V to 5V DC Buck Converter" src="https://user-images.githubusercontent.com/103593959/172689317-0575e362-160b-45d4-ad98-937e967e6ca4.png">
Shown above is the final schematic for our project. Our input is delived from a 12-15V source to the screw terminal. For our final version we used a set of 8 AA batteries to generate 12V into the screw terminal. The input then passes a ferrite bead in order to limit noise coming from the input. It then passes into a LM25765-5 Buck Converter. The LM25765 works as a simple switcher in conjuction with our inductor and schottky diode in order to create an average duty cyle resulting in 5V. From the USB 5V are generated with a current ranging from about 20-30mA. This is entirely dependent on what kind of battery you use. The converter itself is designed to handle up to 3A so you are able to charge your phone with a car battery.

### Data Pin Voltage Divider
<img width="629" alt="Data Pin Voltage Divider" src="https://user-images.githubusercontent.com/103593959/172690697-4c113191-cb47-44f4-89cb-d85b8f5cc583.png">
5V is passed into a voltage divider, in order to use the data pins on the USB output. This is required to charge Apple Devices. We got the required Data Pin Voltages from https://blog.voltaicsystems.com/choosing-usb-pin-voltages-for-iphones-and-ipads/.

## PCB Design
<img width="736" alt="Battery Phone Charger" src="https://user-images.githubusercontent.com/103593959/172690922-350a5b45-ab1b-46ce-9866-4cf9ffeabde6.png">
Shown above is the lastest PCB design. Of interest is the particularly wide track width, which is required because of our design specification of being able to handle at least 3A. Besides that parts, besides the voltage divider for the data pins, have been picked to handle no less than 3A.

## Simulations
![WEBENCHSIM](https://user-images.githubusercontent.com/103593959/172692226-310b16a1-f443-4a36-b901-8baf80800180.png)
![DCSIM](https://user-images.githubusercontent.com/103593959/172692238-541f87c7-a201-4690-8562-cc60e67feb2c.png)
Above is the DC simulation showing the duty cycle. This was done through Webenches internal simulator.
[WEBENCH](https://www.ti.com/design-resources/design-tools-simulation/webench-power-designer.html)
## Results
![RESULTS-3](https://user-images.githubusercontent.com/103593959/172694162-edb24509-7349-41c7-8c8f-bdfb72bc2300.jpg)
![RESULTSWCHARGE](https://user-images.githubusercontent.com/103593959/172694205-9e061ccc-a44e-487e-9e71-378bbb84c875.png)
![RESULTSWCURRENT](https://user-images.githubusercontent.com/103593959/172694233-da5c8616-0a7c-4280-bb87-21d141a1bf0d.png)
![RESULTSRESISTOR](https://user-images.githubusercontent.com/103593959/172694187-71a39f78-31a7-45ef-89d6-a325fd3f6429.png)
The final results were that as expected the device can charge any type of phone including iphones. It has a power efficiency of more than 80%. It can supply up to 3A, but the capacitors in particular get hot rather quickly so don't leave it plugged in for very long. The low current diplayed(20-30mA)in the previous image was likely due to the AA batteries being used to charge a phone for several hours of total charging times previous to the image being taken.
