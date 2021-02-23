# wallisandgill
Wallis and Gill Digital Yacht Firmware and Tools

## Linux instructions
 1. Install arduino-cli with the linux install script first. ```https://arduino.github.io/arduino-cli/latest/installation/```

### Upload latest firmware
 1. First you need to copy this repository to your Linux workstation or server: ```$ git clone https://github.com/unxs0/wallisandgill.git```
 2. Then change dir: ```$ cd Arduino/AK3SignalKOnMast```
 3. Then you need to identify which esp32 board you are using. Most likely ```nodemcu-32s```, but it also could be the ```esp32doit-devkit-v1```, if you have trouble identifying just go ahead and try both. Only one will be able to be uploaded.
 4. You also need to know which ```/dev/``` device you have connected your esp32 board to. Most likely /dev/ttyUSB0 or similar.
 5. Finally you can upload running (e.g. doit board on /dev/ttyUSB0): ```$ arduino-cli upload --port /dev/ttyUSB0 --fqbn esp32:esp32:esp32doit-devkit-v1:FlashFreq=80,UploadSpeed=921600 --input-file ./build/esp32.esp32.esp32doit-devkit-v1/AK3SignalKOnMast.ino.bin```
 6. You may have to press the boot or reset button and hold for 4 secs. But you can also just try to flash again until it works.

### Additional help
Please email support@wallisandgill.com if you encounter any issues.
