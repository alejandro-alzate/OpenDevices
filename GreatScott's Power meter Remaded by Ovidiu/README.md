# Description #

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

Copy Paste from [this source](https://hackaday.io/project/187504-esp32-3-channel-power-logger)