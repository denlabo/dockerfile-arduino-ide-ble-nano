# dockerfile-arduino-ide-ble-nano

Build a docker image of Arduino IDE with compiler for [RedBear BLE Nano](http://redbearlab.com/blenano/).

We tested on Docker v1.11 with Arch Linux 4.5.4-1.


## Quick Start

Run the commands as follows.
NOTE: **$HOME/project** should be replaced to the path of your project directory on the host.

```
$ sudo xhost +
$ docker run -ti --rm -e DISPLAY=$DISPLAY --privileged \
    -v $HOME/project:/home/arduino/Arduino \
    -v /dev/bus/usb:/dev/bus/usb -v /tmp/.X11-unix:/tmp/.X11-unix \
    denlabo/arduino-ide-ble-nano
```

If you want to keep the preferences of IDE, please remove the ``--rm`` option.


## How to Manually Build

```
$ git clone https://github.com/denlabo/dockerfile-arduino-ide-ble-nano.git
$ cd dockerfile-arduino-ide-ble-nano/
$ docker build -t denlabo/arduino-ide-ble-nano .
```


## Notice

### Maintainer
This dockerfile is maintained by [denLabo LLC](https://github.com/denlabo/).

### Trademarks of Third Party
* "Arduino" is a trademark of Arduino LLC in the U.S. and other countries.
* "BLE Nano" is a trademark or registered trademark of Red Bear Company Limited in the U.S. and other countries.
