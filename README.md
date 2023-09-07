# # TEMPERATURE_CONTROL_SYSTEM
Temperature control system using two ATMega32 microcontrollers
# Temperature Control System (Microprocessors Course Project)
This Project is to design temperature control system using two ATMega32 microcontrollers with the help of platformio and proteus.

- Uses SPI communication protocol
- Uses LM35 Temperature Sensor for measurement of temperature
- 16×2 LCD is used to display temperature set point
- choose the Optimum_Temperature by using keybad
- It controls temperature by turning on and off the heater or cooler
- Show warning if the temperature is in the bad state
- Analyze the waveform of motors signal using oscilloscope

# Master Chip
- Receives Optimum_Temperature from keybad
- Prints the digital value of Optimum_Temperature on a 16x2 alphanumeric LCD
- Receives the temperature value Actual_Temperature from LM35 sensors
- Prints the digital value of Actual_Temperature on a 16x2 alphanumeric LCD
- Sends the digital value of Optimum_Temperature and Actual_Temperature  to the slave

# Slave Chip
- Receives the Actual_Temperature and the Optimum_Temperature from the master
- Turn on the cooler motor for temperatures between Optimum_Temperature+5 and Optimum_Temperature+10 degrees (starting with a
duty cycle of 50% plus 10% for every additional 5 degrees)
- Turn on the heater when the temperature is lower than Optimum_Temperature-5 degrees
- Red warning LED blink when the temperature is higher than Optimum_Temperature+10 degrees
- when temperature is between Optimum_Temperature-5 and Optimum_Temperature+5 the two moter should be off
- When one motor is on, the other motor should be off

# Design

![GP1](https://github.com/waelmarwan7/TEMPERATURE_CONTROL_SYSTEM/assets/91396631/19d7ce7e-fc26-4e21-b32c-abdc22da5c37)
