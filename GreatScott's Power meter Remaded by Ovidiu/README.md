# Description # Copy Paste from [this source](https://hackaday.io/project/187504-esp32-3-channel-power-logger)

Were you ever working on a battery or solar powered project and wanted to know exactly how much current your prototype was using?

The easiest way to measure is to use one of the INA219 or INA3221 modules which can be found for cheap. Unfortunately the modules are flawed and often require modifications in order to work as intended.

This is why i have decided to design and create my own power logger which has way more features than any commercial product. On top of that it is fun and easy to build.

# Details #

Here are some of the hardware features:

- 3 channel monitoring, with one of the channels having a "USB C to USB A" power monitor (for monitoring a usb device charging for example)

- ESP32 C3 Mini powered, makes it easy to program and interface with

- USB C interface for programming and power

- Micro SD card support for saving logging data (useful for solar power monitoring projects for example)

- Battey support. Contains all necessary components for safe operation on 3.7V battery (overcurrent, over/under charge, LDO for 3.3V).

- TFT Display and buttons for programable interface. This allows the device to be used without needing a serial connection to a laptop in order to read values.

I am writing the software myself in ArduinoIDE and although the final version is not ready yet. here are some of the software features i'd like it to have:

- Easy to use menu to enable/disable channels, set sampling rates, etc.

- The possibility to use 2 channels together to monitor efficiency of devices (for example monitor the input and output of a 5v boost converter)

- Record accurate date/time and values to a microSD card for later review

- Monitor battery level of the power logger itself and alert when low (maybe send an email or MQTT notification)

- Monitor voltage and current levels on any of the 3 channels and send notifications

- Display a bar graph instead of instant values for the past 1/5/15 min

# Instructions #

## Download and install EasyEDA software ##

Use the provided schematic and PCB files and import them in EasyEDA

## Make any changes if needed ##

If you'd like to add your own features you could rewire the pins of the ESP32

## Order PCB and components ##

Now is the time to decide if you want to order the PCB with the components already soldered to it.

## Solder the components to the PCB ##

I have deliberately used 1206 SMD components to allow for hand soldering if you feel up for it. You don't need a microscope for those

## Optionally use a spare PCB and some standoffs for protecting the bottom of the PCB ##

Add some M3 standoffs and use one of the spare PCBs as a base for stability

## Add the display ##

I recommend using some M3 standoffs to secure the TFT display in place. You could just leave it hanging but i do not recommend it

## Program the ESP32 ##

You'll find my ArduinoIDE software in the files of this project. Please feel free to modify it to suit your needs

I wouldn't mind a mention if you use it in any public way ```:)```

## Test the software ##

Ensure that the display is working and that the INA3221 module is detected. 

Don't forget to solder one of the J pads, in order to set the Chip address
Optional Calibration

If you use 1% resistors calibration may not be necessary, however depending on the accuracy you need you may want to measure the exact value of the resistors. The INA3221 library supports software calibration
Enjoy monitoring the power consumption of your projects

If you are a beginner like me and don't want to spend too much money of measuring devices, this might be the best way for you to achieve that.


