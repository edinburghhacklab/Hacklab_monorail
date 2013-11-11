# Edinburgh Hacklab monorail project

## 
## how to control the monorail
You can control it from Python over Bluetooth as follows:

1. Install python-nxt (http://code.google.com/p/nxt-python/)

2. Turn it on by pressing the orange button.

3. Start python and run the following setup commands:

from nxt.bluesock import Bluesock
from nxt.motor import Motor
ID = '00:16:53:02:9B:DE'
sock =  BlueSock(ID)
brick = sock.connect()
motor_a = Motor(brick, nxt.motor.PORT_A)
motor_b = Motor(brick, nxt.motor.PORT_B)
motor_c = Motor(brick, nxt.motor.PORT_C)

You can then control the motors by calling motor.turn(power, degrees)
e.g. motor_a.turn(127, 360).

Motor A moves it along the rail, Motor B pans the sensor head and Motor
C tilts the sensor head.

See the python-nxt documentation for more, you should be able to set up
and use the sensors too.

## license for the
This work is licensed under a [http://creativecommons.org/licenses/by-sa/3.0/]{Creative Commons Attribution-ShareAlike 3.0)

## people involved
Martin created out of a lego mindstorms kid a monorail. Marcel designed the hooks to hang
the metal bars on to the ceiling and the original connector to link the metal bars. 
The connector above the white board and above the solidering iron required further adjustments
to the design. A task that Jane conducted. Rob made a movie from the  
[http://www.youtube.com/watch?v=eIcEL06_T70](first run)

## roadmap
* charging station
* junctions

## other software to create new lego arrangements
free for personal use [http://mlcad.lm-software.com](Mike's LEGO CAD)