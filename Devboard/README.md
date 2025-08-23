# Devboard

This devboard was a quick perfboard design to get WLED running and driving my ARGB fans. The design has a handful of problems listed below.

  1. The ["BOB-12009" Level Shifter is not recommended](https://kno.wled.ge/basics/compatible-hardware/#:~:text=I2C%20shifters%20are%20generally%20too%20slow%20for%20addressable%20LEDs%2C%20so%20don%27t%20use%20them.) due to the slow pull up nature of the design. Using a SN74AHCT125 bus buffer is a better approach.
  2. A 62-100Ohm resistor should be used on the outputs to the data pins of the 3-pin ARGB connectors.
  3. Each 3-pin ARGB connector could benefit from a ~100nF decoupling cap near its terminals. 
  4. No reverse polarity protection. Not a huge deal, but for a DIY device, would be nice.

![Example Image](https://github.com/jwidess/ARGB-WLED-PC-Controller/blob/main/Devboard/Devboard-Sample.jpg?raw=true)

![Schematic](https://github.com/jwidess/ARGB-WLED-PC-Controller/blob/main/Devboard/Devboard-Schematic.png?raw=true)