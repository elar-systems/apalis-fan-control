# at30-fan-control
Temperature-based control of Toradex Apalis T30 fan through GPIO port.

This package installs the **at30-fan-control** daemon that checks temperature of the Toradex Apalis T30 CPU and controls fan through one of the GPIO pins.

## Installation

You need to build and then install this package:

### Build .deb package
Dependencies:
* fakeroot
* lm-sensors

You can build .deb package using Makefile:
```
make deb
```
And then install it with ```dpkg```:
```
sudo dpkg -i at30-fan-control-*.deb
```

## Uninstall
You can uninstall this package with ```dpkg```:
sudo dpkg -r at30-fan-control

If package does not uninstall properly because of installation issue, try:

sudo mv /var/lib/dpkg/info/at30-fan-control* /tmp/ && sudo dpkg --remove --force-remove-reinstreq at30-fan-control


## Configuration

There is config file /etc/at30-fan-control/at30-fan-control.conf in which you can change
* GPIO pin which will contol the fan
* Upper and lower temperature triggers
* Temperature refresh delay

Please refer to Toradex Apalis T30 documentation to see available GPIO pin numbers.







# aimx6-fan-control
Temperature-based control of Toradex Apalis iMX6 fan through GPIO port.

This package installs the **aimx6-fan-control** daemon that checks temperature of the Toradex Apalis iMX6 CPU and controls fan through one of the GPIO pins.

## Installation

You need to build and then install this package:

### Build .deb package
Dependencies:
* fakeroot
* lm-sensors

You can build .deb package using Makefile:
```
make deb
```
And then install it with ```dpkg```:
```
sudo dpkg -i aimx6-fan-control-*.deb
```

## Uninstall
You can uninstall this package with ```dpkg```:
sudo dpkg -r aimx6-fan-control

If package does not uninstall properly because of installation issue, try:

sudo mv /var/lib/dpkg/info/aimx6-fan-control* /tmp/ && sudo dpkg --remove --force-remove-reinstreq aimx6-fan-control


## Configuration

There is config file /etc/aimx6-fan-control/aimx6-fan-control.conf in which you can change
* GPIO pin which will contol the fan
* Upper and lower temperature triggers
* Temperature refresh delay

Please refer to Toradex Apalis iMX6 documentation to see available GPIO pin numbers.

