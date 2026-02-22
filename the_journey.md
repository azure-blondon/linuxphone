# the journey

From installing arch linux on an sd card to a working phone


## Installing Arch

### Preping the sd card

I wanted to use the Raspberry pi Imager on windows, but the ARM Arch linux tar is not compatible.

So, I switched to following [the instructions on the wiki](https://archlinuxarm.org/platforms/armv8/broadcom/raspberry-pi-4) for AArch64. I used ubuntu for the process.

> Working with ports on WSL is a pain for me, but I am sure it should be manageable


### Booting and connecting to the internet

I had some troubles booting, so I had to change the /etc/fstab file (change the filesystem to /dev/mmcblk1p1).
(this was due to the fact that I tried something I shouldn't have)

I changed the keyboard layout to french (this command is temporary)
```bash
loadkeys fr
```

Then, I needed to initialize pacman keys and update the system, which needed the internet.
However, I needed `iwd` to use the wifi module in the pi. So I had to connect through ethernet.

The problem was that I don't have a router here, I only have my phone's hotspot. After trying many things, I connected my pc to my phone hotspot, then plugged an ethernet cable between my pc and the pi. Changed some parameters to allow sharing wifi to other devices. Then I had to start `dhcpcd` and I quickly downloaded `iwd`.


## Initial setup

### Syncing time

> I am here!

```bash
sudo ln -sf /run/systemd/resolve/stub-resolv.conf /etc/resolv.conf
```

### Creating my user

### Naming the pi

### Installing important programs

- `man`
- `sudo`
