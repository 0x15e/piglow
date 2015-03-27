#PiGlow sample code and instructions

Available from Pimoroni: http://shop.pimoroni.com/products/piglow

PiGlow is a small add on board for the Raspberry Pi that provides 18 individually controllable LEDs. You can use it for all sorts of things! And of course, it fits inside a Pibow!

##Setting up your Raspberry Pi

###Pre-Requisites

PiGlow is based on an IC that communicates via i2c protocol. We need to enable i2c communication on your Raspberry Pi for it to work.

####The easy way:

```bash
curl get.pimoroni.com/i2c | bash
```

####Using raspi-config

```bash
sudo raspi-config
```

Then navigate to **Advanced Options**, then **I2C** and answer Yes to both questions.

###SMBUS Python Library

Then we install the i2c libraries and Python support:

    sudo apt-get install python-smbus

Then reboot your Pi!

##Running the example Python code

Either clone this git repository or download piglow-example.py. You can then run the sample by entering:

    sudo python piglow-example.py

The Python code is designed to show you how to talk to the IC on the PiGlow board so that you can extend it to do other more exciting things!

Want a specific example of how to do something? Get in touch! We should be able to knock up an example or at least point you in the right direction. Just e-mail support@pimoroni.com

##Other support for PiGlow

**Gordon Henderson** (@drogon on Twitter) has very kindly added support for PiGlow into his very popular wiringPi library and even includes a basic command line tool that you can use to control your PiGlow! http://wiringpi.com/dev-lib/piglow/

**Simon Walters** (@cymplecy) has added awesome PiGlow support to his Raspberry Pi GPIO Scratch library: http://cymplecy.wordpress.com/2013/08/12/scratch-gpio-piglow-support/

**Jason Barnett** has put together a great Python class and a load of samples: https://github.com/Boeeerb/PiGlow

**Ben Lebherz** has forked Jasons project and tidied up the code a bit while adding gamma correction: https://github.com/benleb/PyGlow

**Manuel Ernst** has created a Node.js library: https://github.com/zaphod1984/node-piglow

##More information

For more information the datasheet for the SN3218 IC is included in this repository which outlines the complete communication protocol for the chip.

For those wanting to wire up their PiGlow in other ways these are the GPIO pins used by the module:

- P1 & P17 (3V3)
- P2 (5V)
- P14 (GND)
- P3 (SDA)
- P5 (SCL)
