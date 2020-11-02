# Smart-Bin
A major environmental concern of our society today is proper management and disposal of solid waste, which is crucial to the cleanliness and overall health of our society. Traditional monitoring and disposal of waste is highly inefficient as it requires a lot of time and human effort. Using the power of Internet of Things (IoT), Smart Bin is designed for efficient and smart waste monitoring.


Components Used:

1) Arduino Mega 2500 board
2) Ultrasonic Sensor HC-SR04
3) ESP8266 (ESP-01) Wi-Fi Module
4) Breadboard
5) Jumper Wires
6) Dustbins


Working:

The Smart Bin uses ultrasonic sensors to monitor the height of garbage in any dustbin. Ultrasonic sensors are placed on the interior side of the lid of each dustbin. The HC-SR04 ultrasonic sensor is a 4-pin module, whose pin names are Vcc, Trigger, Echo and Ground respectively. The module has two eyes like projects in the front which forms the Ultrasonic transmitter and Receiver. The Ultrasonic transmitter transmits an ultrasonic wave which travels in air and when it strikes any material, it gets reflected back towards the sensor. This reflected wave is observed by the Ultrasonic receiver module as shown in the picture below.

![ultrasonic-sensor-working](https://user-images.githubusercontent.com/17234130/40727592-d07c9e80-6445-11e8-82fb-a636e6c5967a.png)

The circuitry inbuilt on the module calculates the time taken for the ultrasonic wave to come back. Now, the speed of sound in air is known. Using the simple formula Distance = Speed * Time, the amount of garbage in the dustbin is calculated.

As trash increases, the distance between the sensor and the dustbin decreases. This live data is sent to the microcontroller. The microcontroller then processes the data and using the ESP8266 WiFi module, it sends the data to the server. Once the amount of garbage in each dustbin is available to the server, the dustbin that requires attention is determined by considering the level of garbage. If the level of garbage in any dustbin exceeds a particular threshold (considered 75% here), it is alerted so that the dustbin can be cleaned.

Instructions for Use:

1) Download and install Arduino IDE
2) Make all the necessary connections
3) Compile and upload the code to the board

![img_20180318_173939](https://user-images.githubusercontent.com/17234130/40727614-dce7b506-6445-11e8-941e-d92ca7f9ccd3.jpg)

![img_20180318_181521_hdr](https://user-images.githubusercontent.com/17234130/40727661-fcbbe064-6445-11e8-9cec-24b56c02d584.jpg)

![40354931-b60e939c-5dd2-11e8-8747-171c0dddda23](https://user-images.githubusercontent.com/17234130/40727784-40df0168-6446-11e8-9f43-fc5609971da7.jpeg)

