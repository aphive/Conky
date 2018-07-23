# My Conky Config
I know ... it's basic ... but I prefer minimal which is why I use Bunsen and it comes with Conky already installed and preconfigured by default. If you want to try out Bunsen, check it out [here](https://www.bunsenlabs.org/). This is a must have for those that like a nice minimal system or prefer a non resource hog. The configs here can be used on other systems as well, you may need to do some minor tweaks but they should be minimal if any.

## What is Conky?
* Conky is a free, light-weight system monitor for X, that displays any information on your desktop. Conky is licensed under the GPL and runs on Linux and BSD.
* It is highly configurable and is able to monitor many system variables including the status of the CPU, memory, swap space, disk storage, temperatures, processes, network interfaces, battery power, system messages, e-mail inboxes, Arch Linux updates, many popular music players (MPD, XMMS2, BMPx, Audacious, etc.), weather updates, breaking news, and much more.
* It can display your info as text, progress bars or graphs with different fonts and colors. With additional scripts you can add new functionality to Conky.
* Get more info and download Conky [here](http://conky.sourceforge.net/). You can get pre-built configs at [deviantART](http://www.deviantart.com/?q=conky).

### Considerations
There are a few tings you will need or may need to do:

* Make sure `lm-sensors` is installed to get the Temp readings.
* In the `CPU` areas, make sure to adjust for the amount of cores you actually have.
* Change the interfaces to whatever yours are named, in a terminal run `ifconfig` to get yours.
* In the `Disk Usage` area, make sure to add entries for the different mount points if you separated them during install.
* Show your Distribution:
    * `Distribution: $alignr ${execi 1200 lsb_release -ds | awk '{print $1}'} ${execi 1200 lsb_release -ds | awk '{print $3}'}`

### Note
There are two config files, which you use, depends on which version of conky you are running. If you look at the default conky config on your machine you can compare both files and see which one matches the format on your system.

#### lm-sensors
`lm-sensors` is a hardware health monitoring package for Linux. It allows you to access information from temperature, voltage, and fan speed sensors. It works with most newer systems.

This may already be on your computer but to install it run:

```
sudo apt install lm-sensors
```

Once the install is complete, run `sensors` to initiate an initial scan of your hardware. You'll see information like:

```
Adapter: ISA adapter
Core 0:       +53.0°C  (high = +105.0°C, crit = +105.0°C)
Core 1:       +52.0°C  (high = +105.0°C, crit = +105.0°C)
Core 2:       +52.0°C  (high = +105.0°C, crit = +105.0°C)
Core 3:       +55.0°C  (high = +105.0°C, crit = +105.0°C)
```

### Other things to do
Depending on your screen size, resolution and content, make sure to adjust the following lines.
* `maximum_width = 260,`
* `font = 'Liberation Mono:Light:size=9'`

## What's it look like?
![Screenshot](https://github.com/Computero/Conky/blob/master/Conky.png "ScreenShot")
