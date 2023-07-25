# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:

import robot and camera from robomaster library and import time library in the python code

### Step2:

Initiallize the robo and create a chasis object

 ### Step3:

Create a camera object

### Step4:

Mention x distance, y distance, z as the angle you want it to move and the speed inside the <"chasisobject'>.move() 

### Step5:

Close the initialiized robo

## Program
```
from robomaster import robot
import time
from robomaster import camera

if _name=='main_':
    ep_robot=robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=2.8,y=0,z=0,xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0,y=0,z=45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")


    ep_chassis.move(x=0.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=204,b=255,effect="on")

    ep_chassis.move(x=0.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=192,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0.9,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0,y=0,z=-35,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=1.9,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0,y=0,z=35,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=192,b=0,effect="on")

    ep_chassis.move(x=1.44,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0,y=0,z=10,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0,y=-2.1,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=192,b=0,effect="on")

    ep_chassis.move(x=0,y=0,z=-10,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")


    ep_chassis.move(x=-0.55,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")


    ep_chassis.move(x=0,y=0,z=180,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=204,b=255,effect="on")


    time.sleep(4)
    
    
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")


    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![robo](/robot.jpg)

1[robo](/robot_side.jpg)

## MobileRobot Movement Video:


[![video](https://youtu.be/7Jd60ljt67c)](https://youtu.be/7Jd60ljt67c)
 

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.
