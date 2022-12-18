# DualMCU-RP2040 Arduino Package
RP2040 Arduino Package Index JSON

DualMCU Arduino core is a ported version of the [Raspberry Pi Pico Arduino Core](https://github.com/earlephilhower/arduino-pico) based on the great work of earlephilhower Earle F. Philhower, III. This port of the RP2040 uses the Raspberry Pi Pico SDK and a custom GCC 10.3/Newlib 4.0 toolchain, the same as earlephilhower [version 2.6.4](https://github.com/earlephilhower/arduino-pico/releases/tag/2.6.4).

# Documentation
See https://github.com/UNIT-Electronics/DualMCU along with the examples for more detailed usage information.

# Supported Boards
* DualMCU RP2040
* Raspberry Pi Pico
* Raspberry Pi Pico W
* Generic (configurable flash, I/O pins)

# Installing via Arduino Boards Manager

Open up the Arduino IDE and go to File->Preferences.

In the dialog that pops up, enter the following URL in the "Additional Boards Manager URLs" field:

https://github.com/Rabadan-uelectronics/DualMCU-RP2040-Arduino-Package/releases/download/v1.0.0/package_DualMCU_rp2040_index.json

![image](https://github.com/Rabadan-uelectronics/DualMCU-RP2040/blob/main/releases/download/0.0.0/Preferences-AditionalBoardsManagerURL.png)

Hit OK to close the dialog.

Go to Tools->Boards->Board Manager in the IDE

Type "DualMCU" in the search box and select "Add":

![image](https://github.com/Rabadan-uelectronics/DualMCU-RP2040/blob/main/releases/download/0.0.0/BoardsManager.png)

# Uploading Sketches

To upload your first sketch, you will need to plug the USB-C cable into the DualMCU, move the mechanical USB selector to the “A” position (see section: 3.11 Mechanical selector for the USB Communication of https://github.com/UNIT-Electronics/DualMCU/blob/main/DualMCU(Product%20Reference%20Manual).pdf) and press and hold the RP2040 reset button (PB1), you can find it onboard with the label  “RST”

![image](https://github.com/UNIT-Electronics/DualMCU/blob/main/Docs/RP2040-Reset_BUTTON.jpg)

Without release the RESET, with the other hand, press and hold the RP2040 boot button (PB2) labeled “BOOT” 

![image](https://github.com/UNIT-Electronics/DualMCU/blob/main/Docs/RP2040-Enter_Bootloader_mode.jpg)

Then hit the RST and BOOT buttons and the sketch should be transferred and start to run.

![image](https://github.com/UNIT-Electronics/DualMCU/blob/main/Docs/RP2040-Boot_button.jpg)


After the first upload, this should not be necessary as the `arduino-pico` core has auto-reset support.
Select the appropriate serial port shown in the Arduino Tools->Port->Serial Port menu once (this setting will stick and does not need to be
touched for multiple uploads).   This selection allows the auto-reset tool to identify the proper device to reset.
Them hit the upload button and your sketch should upload and run.

**Windows Users**: Please do not use the Windows Store version of the actual Arduino application
because it has issues detecting attached Pico boards.  Use the "Windows ZIP" or plain "Windows"
executable (EXE)  download direct from https://arduino.cc. and allow it to install any device
drivers it suggests.  Otherwise the Pico board may not be detected.  Also, if trying out the
2.0 beta Arduino please install the release 1.8 version beforehand to ensure needed device drivers
are present.  (See #20 for more details.)


# Contributing
If you want to contribute or have bugfixes open an issue/PR here.

# Licensing and Credits
* The [Arduino IDE and ArduinoCore-API](https://arduino.cc) are developed and maintained by the Arduino team. The IDE is licensed under GPL.
* The [RP2040 GCC-based toolchain](https://github.com/earlephilhower/pico-quick-toolchain) is licensed under under the GPL.
* The [Pico-SDK](https://github.com/raspberrypi/pico-sdk) is by Raspberry Pi (Trading) Ltd and licensed under the BSD 3-Clause license.
* [Arduino-Pico](https://github.com/earlephilhower/arduino-pico) core files are licensed under the LGPL.
* [LittleFS](https://github.com/ARMmbed/littlefs) library written by ARM Limited and released under the [BSD 3-clause license](https://github.com/ARMmbed/littlefs/blob/master/LICENSE.md).
* [UF2CONV.PY](https://github.com/microsoft/uf2) is by Microsoft Corporation and licensed under the MIT license.
* Networking and filesystem code taken from the [ESP8266 Arduino Core](https://github.com/esp8266/Arduino) and licensed under the LGPL.
* DHCP server for AP host mode from the [Micropython Project](https://micropython.org), distributed under the MIT License.
* [FreeRTOS](https://freertos.org) is Copyright Amazon.com, Inc. or its affiliates, and distributed under the MIT license.
* [lwIP](https://savannah.nongnu.org/projects/lwip/) is (c) the Swedish Institute of Computer Science and licenced under the BSD license.
* [BearSSL](https://bearssl.org) library written by Thomas Pornin, is distributed under the [MIT License](https://bearssl.org/#legal-details).
* [UZLib](https://github.com/pfalcon/uzlib) is copyright (c) 2003 Joergen Ibsen and distributed under the zlib license.
* [LEAmDNS](https://github.com/LaborEtArs/ESP8266mDNS) is copyright multiple authors and distributed under the MIT license.
* [http-parser](https://github.com/nodejs/http-parser) is copyright Joyent, Inc. and other Node contributors.
* WebServer code modified from the [ESP32 WebServer](https://github.com/espressif/arduino-esp32/tree/master/libraries/WebServer) and is copyright (c) 2015 Ivan Grokhotkov and others
* The [Raspberry Pi Pico Arduino Core](https://github.com/earlephilhower/arduino-pico) of Earle F. Philhower, III (earlephilhower).


