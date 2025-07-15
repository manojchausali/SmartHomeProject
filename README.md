# Smart Home Project
Smart Home Energy Management System Simulation and Weather Classification using ML Model

## Task 1 : Smart Home Energy Management System Simulation 
Below report outlines the development of a Smart Home Energy Management System using the 
Wokwi.com simulator, integrating temperature, PIR motion, and ultrasonic distance sensors with 
an Arduino Uno. We designed the system to monitor environmental conditions and occupancy, 
enabling intelligent control over heating, cooling, and lighting to improve energy efficiency and 
comfort. 
Link to our simulated project - https://wokwi.com/projects/422815933533467649 
Components Used 
1. Arduino Uno – Central microcontroller to process sensor data. 
2. Temperature Sensor (DHT22) – For real-time temperature monitoring. 
3. PIR Motion Sensor – To detect occupancy and motion. 
4. HC-SR04 Ultrasonic Distance Sensor – For measuring distances and simulating object 
proximity. 
5. LCD Display (16x2) – To display real-time sensor data. 
6. 3 LEDs – Indicating alerts and sensor triggers: 
a. LED 1 – High temperature alert. 
b. LED 2 – Motion detected. 
c. LED 3 – Distance threshold breach. 
Circuit Setup 
1. The Temperature Sensor (DHT22) is connected to digital pin 13 of the Arduino. 
2. The PIR Motion Sensor connected to digital pin 0. 
3. For HC-SR04 Ultrasonic Sensor: 
The trigger : Trig → Pin 4 
The echo : Echo → Pin 1 
4. LCD Display (16x2) is connected to pins 12, 11, 10, 9, 8, 7. 
5. LEDs: 
LED 1 → Pin 3 (Temperature alert) 
LED 2 → Pin 6 (Motion detection) 
LED 3 → Pin 2 (Distance alert) 
Sensor Logic and Functionality 
1. Temperature Monitoring: The DHT22 sensor reads temperature data using the 
DHT.read22() function. A threshold of 28°C was set for high-temperature alerts. When 
the temperature exceeds this limit - LED 1 glows. Current temperature is displayed on 
the LCD and Serial Monitor. 
2. Motion Detection: The PIR sensor detects motion by reading the digital input from pin 0. 
If motion is detected - LED 2 glows and Serial Monitor logs "Motion detected!". When 
motion stops, the Serial Monitor logs "Motion ended!". 
3. Distance Measuring: The HC-SR04 sensor measures distance using pulse timing. If an 
object is within 100 cm - LED 3 turns on. Distance is displayed on both the LCD and 
Serial Monitor. 
Code Overview 
We used the following libraries: 
LiquidCrystal.h – For controlling the LCD. 
dht.h – For interfacing with the DHT22 temperature sensor.
Conclusion 
The Smart Home Energy Management System simulation effectively demonstrated real-time 
environmental monitoring and occupancy detection using the Wokwi simulator. The setup 
provides a functional model for optimizing home energy consumption, enhancing comfort and 
efficiency. 
1. The system accurately displayed temperature, motion detection, and distance readings. 
2. LED indicators provided instant visual alerts for all sensor triggers. 
3. The LCD effectively displayed multi-sensor data in real-time.

## Task 2 : Weather Classifier: Temperature & Humidity Analysis 
Link to code - 
https://colab.research.google.com/drive/1stA1J1mV9Gkt7QgNFAs43tXLhg_uZHJp?usp=sharing 
Overview 
1. First, we just add a new column "CATEGORY" to the data which is based on the provided 
conditions. 
2. Then, we plot a bar chart showing "Weather Category Distribution Over Years". 
3. Then, we split the dataset into training and testing sets. Using the training set, we train a 
random forest classifier model. 
4. For the test data, we predict the target values. 
5. Finally, we get the accuracy score of the model and print the classification report. 
6. At the end, we print a graph showing feature importance.
