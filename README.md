# Play_with_Lisa
Link to a video demo: https://www.youtube.com/watch?v=FFNgHaUpvmM
## Overview
This project is an automatic cat toy for my cat Lisa.

Implemented with a [remote control API](https://github.com/mbennett12/kinetic-sculpture-webapi), the sculpture will start once I click the “run sculpture” button on a phone. In a cycle, the needle on the panel will rotate. When the needle points to a dot, the servo motor sweep the cat teaser to attract the cat’s attention. In 30 seconds, the cat toy can run two cycles.

This project is inspired by my last project Schrodinger’s cat. I feel guilty in the last project for “torturing” the hypothetical cat and make it get Covid all the time, so this time I decided to do some animal welfare for a real cat. I am also using the idea of randomness in this project inspired by the Schrodinger’s cat project. The angle and number of sweeps are random each time, to prevent my cat from getting bored with this toy.

## To Reproduce
Hardware:
This project is completed with an ESP32, a stepper motor and a servo motor. The stepper motor is for moving the needle in panel, and the servo motor is for sweeping the cat toy. To set up the project, you will also need a computer with [Arduino IDE](https://www.arduino.cc) to program the ESP32. I also made an enclosure for the toy with a cardboard box.


Software:
In Arduino IDE, upload motors.ino to the ESP32. Change the Wifi name and password accordingly. This code will let the ESP32 connect to wifi in order to run the API. Every 0.5 seconds, it will do an HTTP GET request to the server endpoint to check if the “run sculpture for 30 seconds” button is pressed. If the button is pressed, it will move the motors for 30 seconds.

