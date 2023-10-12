# solar-tracker
A solar tracking tool powered by Arduino and K64 for solar.

## Project Info
This project was created to be the rough design of a solar tracker. The basis of the project is to allow solar panels to get full-sun coverage throughout the day.

## Parts
* Arduino UNO R3
* FRDM-64F Development Board
* 128x64 Arduino OLED
* 5v 200mA Solar Cell
* CD74HC4067 MUX
* 3 x 10k Potentiometer
* 4 x GL5506 Photoresistor
* 2 x GL5506 Servo
* 4 x 1k Resistor

## Software
The code implementation for this project was written in C/C++
* Arduino IDE - Used for the Arduino UNO R3 programming
* Kinetis Design Studio - Used for programming the K64 Development Board
* OrCAD Capture CIS - schematic software

## Schematic
![solar-tracker-schematic](https://github.com/jshabun/solar-tracker/assets/33816145/e398de7b-c7fa-4998-9e04-3049b586e1ce)


## Testing
The solar tracker was tested in many different lighting conditions.  Testing required different environments such as night, day, indoors and outdoor lighting conditions.  It was tested for its responsiveness and stability.  Different lighting conditions had an effect on the tracking system responsiveness.  When the lighting condition was dark, the system was very responsive compared to when the lighting intensity was higher.  The higher sensitivity during darker conditions caused unnecessary movements to the tracking system.  Our initial test concluded that it required a control for fine tuning its  responsiveness to light differences within the different quadrants of the four sensors (photoresistors).  We added a potentiometer to control a threshold value for the differences in the sensor readings.  This allowed us to reduce unnecessary movements caused by higher sensitivity during darker lighting conditions.  This resulted in a more stable movement.  
	
A second potentiometer was added to control the speed at which it tracked the light.  Initial tests proved rapid movement was unnecessary since the purpose was to track the sun's slow movement.  This allowed us to decrease the speed for tracking the sun, which would make for a more stable movement and reduce wear on parts.  This also allowed us to increase the speed for testing, and demonstration purposes. 

## Installation/Running
1. Connect everything based on the schematic
2. Upload the `.ino` file to the Arduino Uno R3 and the `.c` file to the FRDM-K64F
3. Run the code on both microcontrollers and adjust the 2 main potentiometers based on lightning conditions to ensure proper calibration of light and movement sensitivity.

 ## Demo
 https://www.youtube.com/watch?v=bKEWS9X5NZo
