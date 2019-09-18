# LarduinoISP
make arduino board to be an ISP of LGT8FX8P(modify from LGT8FX8D, just change SWDID) series MCU
- 1. Use Larduino as ISP(not orther Arduino), link as the image.
- 2. And 'Upload using programmer', upload LED Blink. 
- 3. Copy command line, and replace Blink.ino.hex as Blink.ino.with_bootloader.hex, then run it in Terminal or CMD.
----
## This is my command in macOS:
/Applications/Arduino.app/Contents/Java/hardware/tools/avr/bin/avrdude -C/Applications/Arduino.app/Contents/Java/hardware/tools/avr/etc/avrdude.conf -v -patmega328p -carduino -P/dev/cu.usbmodem00001 -b19200 -Uflash:w:/var/folders/yx/3455zd357xv1q5thmn8d6nfw0000gn/T/arduino_build_662222/Blink.ino.with_bootloader.hex:i 
