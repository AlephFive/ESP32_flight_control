# ESP32_flight_control

There are two ESP32 microcontrollers on the plane. One controls the rear control surfaces, while the other controls the forward propellers. Hence, there are two files that need to be uploaded to each microcontroller individually. The ServoControl file should be uploaded to the read controls, while the DCMotorControl file should be uploaded to the ESP32 connected to the DC motors.

Additionally, you may need to modify the Wifi network settings in both code files in order for the ESP32s to connect to your own network. Once they connect to the network, you can activate the plane remotely by going to this address: http://134.122.113.13/bm3027 

![open](https://miro.medium.com/max/700/1*4DswH9LDBM2T4CO9fM4QPw.jpeg)

A 3D stl file for the propeller is also provided. The file is an edited version of the TinkerCad fidget spinner model.


## How to run ESP32 code:

We are using the Arduino IDE. To enable IDE support for the ESP32, first open up Preferences and under "Additional Boards Manager URLs", add the following URL:
```
https://dl.espressif.com/dl/package_esp32_index.json
```
![BoardsManagerURL](https://user-images.githubusercontent.com/6265129/153997561-184baff3-dad6-4699-b3ea-dfbc9214f8ea.jpg)

Then, go to "Tools/Board:/Board Manager" and install ESP32:

![BoardsManager](https://user-images.githubusercontent.com/6265129/153997769-d04a40cc-fc14-4832-a115-e32f032be1a6.jpg)

Then, go to "Tools/Manage Libraries" and search for tft_eSPI. Install it.

![ManageLibs](https://user-images.githubusercontent.com/6265129/153997596-e524be05-fd41-4741-9025-56ad5be9ab33.jpg)

You will also need to install ESP32Servo, HTTPClient, and various Wifi packages for the ESP32.

After that, go to "Tools/Board:" and select "TIGO T1".

![BoardSelect](https://user-images.githubusercontent.com/6265129/153997616-e5988c80-6d34-4566-b800-3d8c03f9ffd7.jpg)

Now, simply connect your board and click upload.
