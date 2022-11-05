# Pinout

## Water sensor (ultrasonic sensor)

* ECHO PIN - 17
* TRIG PIN - 16

## System sensor (system temperature)

* SYS TEMP - ADC(4)

> _ADC represents the internal analog pin_

## LED Indicator (system on  light and alarm light)

* SYS ON - 25
* ALARM (Water level) - 15

# Required libraries

* from machine import Pin, I2C, SPI
* import time
* import os
* from pico_i2c_lcd import I2cLcd
* from lcd_api import LcdApi

# Variables

This outlines the variables utilized for the calculations internally.

## Water level

* MIN_WATER_HEIGHT = 138 # CM 
* MAX_WATER_HEIGHT = 10 # CM 
* WATER_ALARM = 117.3 # CM - 85 empty

## System Temp

* MAX_TEMP = 45 # degreesC 

## 16x2 LCD Display
* I2C_ADDR = 39 # Pin 0 - SDA, Pin 1 - SCL
* I2C_NUM_ROWS = 2
* I2C_NUM_COLS = 16
* lcd_i2c = I2C(0, sda=machine.Pin(0), scl=machine.Pin(1), freq=400000)
* LCD_DIS = I2cLcd(lcd_i2c, I2C_ADDR, I2C_NUM_ROWS, I2C_NUM_COLS)