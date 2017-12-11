# My Conky Config
I know ... it's basic ... but I prefer minimal which is why I use Bunsen and it comes with Conky installed and preconfigured by default. If you want to try out Bunsen, check it out [here](https://github.com/BunsenLabs). This is a must have for those that like a nice minimal system or prefere a non resource hog.

## What is Conky?
Conky is a free, light-weight system monitor for X, that displays any information on your desktop. Conky is licensed under the GPL and runs on Linux and BSD.

Conky is highly configurable and is able to monitor many system variables including the status of the CPU, memory, swap space, disk storage, temperatures, processes, network interfaces, battery power, system messages, e-mail inboxes, Arch Linux updates, many popular music players (MPD, XMMS2, BMPx, Audacious, etc.), weather updates, breaking news, and much more.

Conky can display your info as text, progress bars or graphs with different fonts and colors. With additional scripts you can add new functionality to Conky.

Get more info and download Conky [here](http://conky.sourceforge.net/). You can get pre-built configs at [deviantART](http://www.deviantart.com/?q=conky).

### Do I need to do anything before I use this?
There are a few tings you will need or may need to do:

* Make sure `lm-sensors` is installed to get the Temp readings.
* In the `CPU` areas, make sure to adjust for the amount of cores you actually have.
* Change the interfaces to whatever yours are named, run `ifconfig` to get yours.
* If you separated your `/home`, `/var`, etc partitions, adjust the **Disk Usage** section to reflect those.

#### lm-sensors
`lm-sensors` is a hardware health monitoring package for Linux. It allows you to access information from temperature, voltage, and fan speed sensors. It works with most newer systems.

This may already be on your computer but to install it run:

```
sudo apt install lm-sensors
```

One the install is complete run an initial scan of your hardware

```
sensors
```

You'll see information like:

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
* `font = 'Monospace:Light:size=9'` <- Should only need to adjust the size.

## What's it look like?
![ScreenShot](https://raw.github.com/Computero/conky_config/master/Conky.png)

