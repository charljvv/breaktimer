# breaktimer
A python script to remind you to take regular breaks by way of a SENSE HAT board on an RaspberryPI

# Demo
[https://youtu.be/QQferyn7KB8](https://youtu.be/QQferyn7KB8)
# Pre-requirements
## Hardware
- An installed sense HAT board on the pi. More info on that here: [https://www.raspberrypi.org/products/sense-hat/](https://www.raspberrypi.org/products/sense-hat/)
- The official guide is also useful for getting started and exploring other projects: [https://www.raspberrypi.org/documentation/hardware/sense-hat/](https://www.raspberrypi.org/documentation/hardware/sense-hat/)
<img src="https://github.com/charljvv/breaktimer/blob/master/assets/sense-hat-pic.jpg" width="300" height="200">

## Software
- A RaspberryPi with a version of linux.
- Install Python on your pi. Python2.7 is usually installed with most debian distributions. This code should be compatible with v3.6 as well.
- Clone this repo
- Run `pip install -r requirements.txt` or `pip install -r requirements.txt` (for python3 assuming pip3 is bound correctly to PATH)
- Run `python breakmeupscotty.py` or `python3 breakmeupscotty.py` (for python 3)
- This will run an endless loop. This script is created to be run in the background or on system startup.

## Launching this script on pi startup
Assuming you have a runnig shell with the requirements setup correctly.
run `crontab -e`
and add the following line at the bottom of this file:
`@reboot /usr/bin/python ~/breakmeupscotty.py`

Replace `/usr/bin/python` with your path to python
and `~/breaktimer/breakmupscotty.py` with the path to the repo/breakmeupscotty.py

This will run the script on startup of the pi. Have a look at [http://www.cronmaker.com/](cron maker) if you want to customize the frequency of the script running.
Cron setup is out of scope for this project.
