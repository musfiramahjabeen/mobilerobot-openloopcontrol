# MobileRobot-Openloopcontrol

## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:

1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:

Initiate the MobileRobot.

### Step2:

Connect your PC with the MobileRobot through Wi-Fi.

### Step3:

Open batter_level.py file and check the battery.

### Step4:

Open the other Python files and Program the movements of the robot using python.

### Step5:

Execute the python program and record the movements.

## Program

```python
# Developed by : MUSFIRA MAHJABEEN M
# Register Number : 212223230130
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_720P)

    ep_chassis.move(x=2.25, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=75, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=102,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=93, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=153,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=-35, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=147,b=254,effect="on")

    ep_chassis.move(x=1.45, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=254,g=147,b=168,effect="on")

    ep_chassis.move(x=0, y=0, z=52, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=83,g=82,b=162,effect="on")

    ep_chassis.move(x=1.7, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=98,g=183,b=82,effect="on")

    ep_chassis.move(x=0, y=-2, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=75,g=196,b=52,effect="on")

    ep_chassis.move(x=0, y=0, z=160, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=176,b=56,effect="on")

    ep_chassis.move(x=1, y=0, z=15, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=198,g=177,b=156,effect="on")

    ep_chassis.move(x=0, y=0, z=360, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=190,g=177,b=156,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

### Start Point :

![start](https://github.com/musfiramahjabeen/mobilerobot-openloopcontrol/assets/138971008/94e364c2-bf71-446b-bbff-4be1b46a0575)


### End Point :

![end](https://github.com/musfiramahjabeen/mobilerobot-openloopcontrol/assets/138971008/8945c0b5-1efc-421e-9474-f2178946a38e)


## MobileRobot Movement Video:

Check out my youtube video:

    https://youtu.be/ALWE5VsxhOg

## Result:

Thus the python program code is developed to move the mobilerobot in the predefined path.

<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
