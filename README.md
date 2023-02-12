# ArduinoNano-GyroscopicSteering
A DIY steering wheel controller with MPU6050 gyroscopes connected to Arduino Nano or other ATmega328 based device. This is just a personal project but hopefully can serve as a further example/reference to add potentiometer functionality for others in their projects.
Also, this project only works on Windows.

## Instructions
1. Install [VJoy](https://sourceforge.net/projects/vjoystick/)
2. Download [VJoySerialFeeder](https://github.com/Cleric-K/vJoySerialFeeder)
3. Upload the included sketch into your Arduino (Customize according to your need) e.g. add other inputs, keep in mind the number NUM_CHANNELS, and order of channels in which ibus.write() is called in the code.
4. Customize the inputs in VJoySerialFeeder. e.g. In the provided sketch, ibus.write(mpu6050.getAngleY()) is called, that will be channel one, since it's used as an axis, set it in VJoySerialFeeder.
5. Setup to change the minimum, center and maximum value, e.g. 90,180,270.
6. Make sure the port is set to the one connected to your Arduino and IBus is set as the protocol.
![VJoySerialFeederExample](https://user-images.githubusercontent.com/23694752/218307935-fcdff35a-5e29-4b64-b446-067b4ff6a9db.png)
7. That should be all.

## References
[MPU6050_tockn](https://github.com/tockn/MPU6050_tockn)
[VJoySerialFeeder](https://github.com/Cleric-K/vJoySerialFeeder)
[This tutorial](https://github.com/Juarezdoposto/Lightsaber_Game_Controller)
