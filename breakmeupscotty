#!/usr/bin/python

# Import all the necessary packages
from sense_hat import ACTION_HELD, ACTION_PRESSED, ACTION_RELEASED, SenseHat
from datetime import datetime, timedelta
from random import choice, randint
from time import sleep

# Communicatation with the SENSE HAT board
sense = SenseHat()

# Clear the board - defaults to blank . ie. Off
sense.clear()

# Colours are any combination of R, G, B : (0->255, 0->255, 0->255)
black = (0, 0, 0)
white = (255, 255, 255)
red = (255, 0, 0)
blue = (0, 0, 255)
green = (0, 255, 0)
purple = (128, 0, 128)
yellow = (255, 255, 0) 

sleepTime = 3600 # an hour in sleep time :D 60*60 =36000
workingHours = (7,17) # start work at 7 and stop at 17, denoted as start time (inclusive), end time (exclusive)
workWeek = (0,4) # Monday is 0 and Sunday is 6. ie. Monday -> Friday 0,4; Monday -> Saturday 0,5

breakTimeMessage = "BREAK" # Customisable message displayed when the time passes

def randomRGBValue():
	return randint(0,255)

while True:
	if(datetime.today().weekday() in range(workWeek[0], workWeek[1]+1) and datetime.now().hour in range(workingHours[0],workingHours[1]))

		# Flash all LEDs with random colours
		sense.clear(randomRGBValue(), randomRGBValue(), randomRGBValue())
		sleep(1)
		sense.clear(randomRGBValue(), randomRGBValue(), randomRGBValue())
		
		# Print the message on the LEDs
		sense.show_message(breakTimeMessage,text_colour=red)

		# Flash all LEDs with random colours
		sense.clear(randomRGBValue(), randomRGBValue(), randomRGBValue())
		sleep(1)
		sense.clear(randomRGBValue(), randomRGBValue(), randomRGBValue())

		# Wait for a button press before restarting the timer
		event = sense.stick.wait_for_event()
		if(event.action == ACTION_PRESSED):
        		sense.clear()
        		sleep(sleepTime)
