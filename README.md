# tslibd - D-Bus interface for the [tslib](http://tslib.org) library libts

## design idea

### systemd service `org.tslib.conf`
Create a systemd service with methods for enabling / disabling filters and
getting / setting their parameters.
Create one property per filter like *Filtername*Active for the status.
This is done by reading / writing the config file and properly reconfiguring
the library.

Already running users like ts_uinput or xf86-input-tslib should instantly
read the new touchscreen values, without restarting themselves (?)

### build deps
* libconfig to edit /etc/ts.conf
* systemd/sd-bus.h as DBUS interface
