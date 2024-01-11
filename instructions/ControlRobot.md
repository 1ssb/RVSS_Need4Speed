## Connect your robot to the wifi:
1. Turn the robot on with the switch on it's side.
2. Your robot will then connect to the wifi, and advertise a wlan address on its OLED screen -- take note of this number (xxx.xxx.xx.x).

## Check the connection!
Navigate to the RVSS repository on your local machine and get ready to test the camera and motors on the PiBot. You will run a script that will check that the camera can take an image (validate by looking for reasonable, non-zero image width and height), and will turn on each motor, one at a time. Make sure you're holding your robot so it doesn't drive off a table. Make sure to enter the wlan address.

``` python PenguinPi-robot/software/python/client/test_camera_motors.py --ip xxx.xxx.xx.x```

If your motor doesn't spin or no image shape prints, let one of the workshop organisers know as your robot may be faulty.

**Note: if you want to get some initial insight into how control the robot camera and motors, read through this script to see how it works.**

## How to turn off the robot:
1. On the back of the robot, there is a 'SDN' button. Press this button for 3 seconds.
2. On the front of the robot, there is a little green light, next to a red light. After you press the 'SDN' button, wait for the message 'Turn Raspberry Pi off safely' to show on the OLED screen **AND** for this green light to be off. Note: after pressing the button, the LED will flash, then turn solid, then finally turn off after this pattern. It is now safe to turn off the robot with the side switch.

## FAQ
**I want to ssh onto the robot!**
You should not need to do this at any point. Please check with one of the workshop organisers before changing code directly on the PiBot. If they give you the go ahead, you can:
1. Check the robot's OLED screen to see its wlan address (xxx.xxx.xx.x).
2. In a terminal window, SSH to the robot with the command below. Note: the -X command is important, please make sure you use this!
```ssh -X pi@xxx.xxx.xx.x```
3. When prompted, enter password: PenguinPi 
