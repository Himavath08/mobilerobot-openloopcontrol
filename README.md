# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

## Step1:

Use from robomaster import robot

## Step2:

Choose the x,y,z - axis movement distance(meters).

## Step3:

Give ep_chassis.move to move straight.

## Step4:

Give time.sleep() for a break.

## Step5:
Give ep_chassis.drive_speed to have a circular movement.


## Program
```python
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
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=2.8, y=0, z=0, xy_speed=1.3).wait_for_completed()

    ep_led.set_led(comp = "all",r=0,g=250,b=0,effect="on")
    ep_led.set_led(comp = "all",r=0,g=0,b=200,effect="on")

    ep_chassis.move(x=0, y=0, z=75, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=1.3).wait_for_completed()

    
    ep_chassis.move(x=0, y=-1.6, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-20, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=50,b=50,effect="on")

    ep_chassis.move(x=0, y=-1.4, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=252,b=50,effect="on")

    ep_chassis.move(x=0, y=0, z=37, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=128,effect="on")

    ep_chassis.move(x=0, y=-1.4, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=6, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")

    ep_chassis.move(x=-1.95, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-102, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=140,g=102,b=0,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=50,g=102,b=0,effect="on")

  time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:
![sdd](https://github.com/Himavath08/mobilerobot-openloopcontrol/assets/139110631/c97b7cec-21a9-42da-88f7-5ed78bb15d7d)
![sa](https://github.com/Himavath08/mobilerobot-openloopcontrol/assets/139110631/12a80d1f-3ca9-4cbe-b987-611bcdb080e8)
![as](https://github.com/Himavath08/mobilerobot-openloopcontrol/assets/139110631/07c52a09-3e89-4a29-bd95-ba071a7200c0)

## MobileRobot Movement Video:
https://youtu.be/2DhFFhd4c-E?feature=shared

## Result:
Thus the python program code is developed to move the mobilerobot in the 
```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
