# FC-28-Soil-Moisture-Sensor-Interfacing

#The soil moisture sensor consists of two probes that are used to measure the volumetric content of water. The two probes allow the current to pass through the soil, which gives the resistance value to measure the moisture value.

#When there is water, the soil will conduct more electricity, which means that there will be less resistance. Dry soil conducts electricity poorly, so when there is less water, then the soil will conduct less electricity, which means that there will be more resistance. 

#This sensor can be connected in analog and digital modes.

#**Analogue Mode**

#To connect the sensor in the analog mode, we will need to use the analog output of the sensor. When taking the analog output from the soil moisture sensor FC-28, the sensor gives us a value from 0 to 1023. The moisture is measured in percentages, so we will map these values from 0 to 100, and then show them on the serial monitor. You can set different ranges of the moisture values and turn the water pump on or off according to it.

#Connect the FC-28 soil moisture sensor to the Arduino as follows:
- VCC of the FC-28 to 5V of the Arduino
- GND of the FC-28 to GND of the Arduino
- A0 of the FC-28 to A0 of the Arduino

![Soil-Moisture-Sensor-FC-28](https://user-images.githubusercontent.com/97503786/187653432-b434fc4c-1d90-47b4-9058-d15d6d255129.png)

#The module also contains a potentiometer, which will set the threshold value. This threshold value will be compared by the LM393 comparator. The output LED will light up and down according to this threshold value.

#**Circuit diagram**

![right](https://user-images.githubusercontent.com/97503786/187658352-f7145154-4e5f-4bd1-ba57-d6f62fb63bd3.jpeg)

#**Digital Mode**

#To connect the soil moisture sensor FC-28 in the digital mode, we will connect the digital output of the sensor to the digital pin of the Arduino. The sensor module contains a potentiometer, which is used to set the threshold value. The threshold value is then compared with the sensor output value using the LM393 comparator, which is placed on the sensor module. The LM393 comparator compares the sensor output value and the threshold value, and then gives us the output through the digital pin. When the sensor value is greater than the threshold value, the digital pin will give us 5V, and the LED on the sensor will light up. When the sensor value will be less than this threshold value, the digital pin will give us 0V and the light will go down.

**Circuit diagram**

#The connections for the FC-28 soil moisture sensor and the Arduino in digital mode are as follows:
- VCC of FC-28 to 5V of Arduino
- GND of FC-28 to GND of Arduino
- D0 of FC-28 to pin 12 of Arduino
- LED positive to pin 13 of Arduino
- LED negative to GND of Arduino


