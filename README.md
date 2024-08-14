# AAC codec plugin for Raspberry Pi OS 64bit

As we all know Debian 12 switched to pipewire as audio backend, and the crew haven't decided to move [fdk-aac](https://packages.debian.org/source/stable/fdk-aac) out of `non-free` repo.

So by default install, there is no AAC codec for bluetooth, but it can be manually build from source.

Then there is the aac code plugin, install steps:

1. install libfdk-aac2: `sudo apt install libfdk-aac2`
2. Download the [`libspa-codec-bluez5-aac.so`](https://github.com/steve3d/raspberry-pipewire-aac-codec/raw/main/libspa-codec-bluez5-aac.so)
3. Move it into `/usr/lib/aarch64-linux-gnu/spa-0.2/bluez5`
4. Reboot
5. Connect your Apple AirPods (any)
6. Enjoy

This so is built in `libspa-0.2-bluetooth_0.3.65-3` and Debian 12 (bookworm)
