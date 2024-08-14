# AAC codec plugin for Raspberry Pi OS 64bit

As we all know Debian 12 switched to pipewire as audio backend, and the crew haven't decided to move [fdk-aac](https://packages.debian.org/source/stable/fdk-aac) out of `non-free` repo.

So by default install, there is no AAC codec for bluetooth, but it can be manually build from source.

Then there is the aac code plugin, install steps:

1. Make sure you are using PipeWire audio backend in `raspi-config`
2. Install libfdk-aac2: `sudo apt install libfdk-aac2`
3. Download the [`libspa-codec-bluez5-aac.so`](https://github.com/steve3d/raspberry-pipewire-aac-codec/raw/main/libspa-codec-bluez5-aac.so)
4. Move it into `/usr/lib/aarch64-linux-gnu/spa-0.2/bluez5`
5. Reboot
6. Connect your Apple AirPods (any)
7. Enjoy

This so is built in `libspa-0.2-bluetooth_0.3.65-3` and Debian 12 (bookworm)
