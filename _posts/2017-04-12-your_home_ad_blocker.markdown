---
title:  "Build an Adblocker using pi-hole for home network"
date:   2017-03-16 15:04:23
categories: [diy]
tags: [learnt, raspberrypi]
---

So it's Ads everywhere and it's annoying..

![Ads Everywhere](https://media.giphy.com/media/d2YZzTQvyoNYf9YI/giphy.gif)

So I came across  **PI-HOLE™** which was a fun learning way to get ads out of home. It's simple and easy way with Raspberry Pi, learn more about it [here](https://pi-hole.net/) .Here's an outline on the how part ?

What we need,
 - Raspberry Pi 2/3 or even PiZero [You need to set up wireless network]
 - 8GB/16GB SDCard 
 
So Let's get started. I started off with the basic OS for Raspberry Pi - [Raspbian Jessie Lite](https://www.raspberrypi.org/downloads/raspbian/)

3 Steps to get pi up and running. 
1. Download the OS and Unzip it.
2. Flash the image to SDCard . Try [etcher](https://etcher.io/) it's super easy and cool :) 
3. Insert SD Card, connect LAN Cable and Power supply . 

``` 
_Create a file named ssh without extension and place it in the memory card. It's to enable ssh by default when OS boots up. or you need to go through extra steps. _
```

Turn on the power and TAAADAAAA..!! now the Pi is up. ssh into it with default password [pi/raspberry] and install our magician by running one command:

```
curl -sSL https://install.pi-hole.net | bash

```

Go through the installation process, stuff you should care about are DNS option, I selected OpenDNS for the upstream DNS and left the network setting to default since I connected through LAN. To have a feel for the pi-hole enabled the web-admin and log queries options.

The installer will do bunch of stuffs and at last will tell you the web interface login with success message. Take a note of it. 

Are we done. 

![close](https://media.giphy.com/media/l2Je9zHYveK012EVi/giphy.gif)

Finnaly, place the pi's ip address as primary DNS in DHCP settings of the Router [more info](https://discourse.pi-hole.net/t/how-do-i-configure-my-devices-to-use-pi-hole-as-their-dns-server/245). Then reboot the router and navigate to pi web interface address that we noted.

That's it home ad blocker is configured and it already started blocking ads for us. 

It's a simple idea to serve a blank page for ad links it discovered and it's gonna make browsing Ads-free atleast in home :P . 


![FREEDOM](https://media.giphy.com/media/6901DbEbbm4o0/giphy.gif)
