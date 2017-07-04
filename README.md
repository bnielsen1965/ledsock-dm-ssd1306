# ledsock-dm-ssd1306

A ledsock display module driver for SSD1306 i2c based OLED displays.

## install

This module should be installed as a dependency in a ledsock server installation.

> cd ledsock
> npm install --production --save git+https://github.com/bnielsen1965/ledsock-dm-ssd1306.git

Be sure to edit the config.js for ledsock and specify the displayModule.module as "ledsock-dm-ssd1306".

### Raspberry Pi Notes
Assuming the display module will be running on a Raspbery Pi with the Raspbian OS, the raspberry pi i2c hardware must be configured before it can be used with this display module.

Edit the /boot/config.txt and add the following lines to enable the i2c hardware...

```text
dtparam=i2c1=on
dtparam=i2c1_baudrate=400000
```

Create a new file /etc/modules-load.d/i2c.conf and add the following lines so the device node will load...

```text
i2c-dev
```
