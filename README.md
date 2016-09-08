Hook up Connections:
This module can host up to 8 buttons and store a passcode of up to 18 button presses.

All buttons/switches use a common ground, 
Connect the other side of the buttons/switches to the following pins.

[Button, Digital Pin]
1,D2  	2,D3
3,D4  	4,D5
5,D6  	6,D7
7,D8           9,D9

This controller can drive an SSR (solid state relay) to control a range of devices such as solenoids, mag switches, or linear actuators.
NOTE: pins are limited to 20mA and typically cannot sink or source enough current to directly power these devices.
You must use an SSR or an arduino signal level compatible relay to control the devices external power supply.

There are 2 digital pins that change state when a correct passcode is entered.

D12 (normally low until the correct passcode is entered)
D13 (normally high until the correct passcode is entered)
When the correct passcode is entered these two pins switch state from Low/High and High/Low for 5 seconds and then return to theier normal state.

When an incorrect passcode is attempted the unit has the ability to play a (although at a low levlel) wrong answer buzz sound. 
Pin 11 is the audio output pin and can be connected to a small speaker + side. 
The - side of the speaker would be connected to the common ground of the controller.


First Run:

When the controller is turned on for the first time it does a small test to se if it has been programmed with a passcode.
If not, it will program itself with the default passcode (1-2-3-4).

You can then use the device as it is and when you press buttons 1-2-3-4 you will see the LED at D13 turn off for 5 seconds and then turn back on.
A correct passcode has been entered!


Setting a Passcode:
Some people may wish to change the passcode to something else, or utilize more than 4 buttons.
You may enter up to 18 total button presses from any of the 8 buttons. (i.e. 162853644212531687)

To do this press and hold buttons 1,2,& 4 at power up. 
The LED at D13 will turn off and then in 3 seconds it will flash rapidly(20x) indicating that the controller is switching into programming mode.
Once the LED stays solid you can now begin to enter the sequence of button presses you desire.
When you have finished entering your sequence simply leave the unit alone for 5 seconds. 
The LED at D13 will flash rapidly(20x) to indicate that the controller is leaving programmiong mode and returning to normal operation mode.

NOTE: If you are entering a new passcode be sure to not take any longer than 5 seconds between button presses as the unit exits programming mode when 5 seconds pass after the last button press. 

TIP: If you accidently enter programming mode and do not wish to enter a new passcode simply do not enter one and wait 5 seconds for the unit to automatically leave programming mode. 


Resetting to default:

This controller module has the ability to be reset back to a factory default passcode ( 1-2-3-4 )
To reset the module Pull pins 2,3, 4, & 5 to ground while powering up.
The LED at D13 will flash rapidly on and off (20x) once the default passcode has been set.
At this time remove the pins from ground
After the LED stops flashing there is a 3 second delay before the unit resumes normal operation.
