# tslibd - DBUS interface for the [tslib](http://tslib.org) library libts

## design idea

### systemd service `org.tslib.touchscreen`
Create a systemd service with methods for enabling / disabling filter and getting / setting parameters:

Layout TODO

### build deps
* libconfig to edit /etc/ts.conf
* systemd/sd-bus.h as DBUS interface
