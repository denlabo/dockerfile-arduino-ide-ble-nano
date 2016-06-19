# dockerfile-arduino-ide-ble-nano

Build a docker image of Arduino IDE with compiler for [RedBear BLE Nano](http://redbearlab.com/blenano/).

We tested on Docker v1.11 with Arch Linux 4.5.4-1.

## Quick Start

```
$ sudo xhost +
$ docker run -ti --rm -e DISPLAY=$DISPLAY --privileged \
    -v $HOME/project:/home/arduino/Arduino \
    -v /dev/bus/usb:/dev/bus/usb -v /tmp/.X11-unix:/tmp/.X11-unix \
    denlabo/arduino-ide-ble-nano
```

HINT: **$HOME/project** should be replaced to the path of your project directory.

## Notice

### Maintainer
This dockerfile is maintained by [denLabo LLC](https://github.com/denlabo/).

### Trademarks of Third Party
* "Arduino" is a trademark of Arduino LLC in the U.S. and other countries.
* "BLE Nano" is a trademark or registered trademark of Red Bear Company Limited in the U.S. and other countries.
