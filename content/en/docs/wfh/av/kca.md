---
title: "KCA's Home office setup"
---

# TL;dr

## Audio

Rode podmic going into a focusrite 2i2 interface to USB Switch. Audio out goes through the 2i2 to speakers or headphones depending on volume set.

## Video

IPhone mounted to monitor arm with hdmi out to a camlink to usb switch

The usb switch allows me to run the work laptop and my personal devices through the same set up with minimal cable unplugging.

it mostly works.


# Future plans

webcams almost universally suck quality wise. and my current webcam is dying. It feels morally wrong to buy effectively the same webcam for twice the price.

## Constraints:

needs to work on MacOS, Windows and Linux
Needs to be able to be moved between systems.

## Options:

- Capture card and canon m50:
Unfortunately manual focus and needs the canon app running all the time to keep it from shutting down.

- Capture card and go pro:
Gets me auto focus and a wide lens but no DOF, long term works but not shiny.

- Avermedia pw315
This is a brand new webcam that is 500+ dollars and pretty much the only one that doesn’t epically fail for image quality and control options but it’s $500+, fixed focus and the same price as the go pro option

- Capture card and camera upgrade:
money++ 😞

## Systems

I have 2 work laptops one locked down windows one MacOS. Both will not work with software options due to fun reasons (library signing on MacOS and locked down on the other) on top of this I have, One or more desktops and One personal laptop

I’d rather not have the fun job of unplugging and replugging usb and dealing with that. I also want to take audio from all of the devices and centralise it. So I can output a mix of multiple systems as required.

And this is where the Raspberry Pis are used.

Raspberry Pis support running in device mode allowing them to pretend to be certain devices including UVC webcams. If i connect the camera and microphone to desktop i can then have OBS capture both at all times and output a set of RTMP streams to the local network going to the Raspberry pis when required.

The pi receives RTMP stream turn into an audio and video UVC connection and provide to the work device. For Audio output from each system the PI pretends to be a sound device and takes that output and sends it over the network to the desktop.


This all ignores the personal laptop but that's ok. it's used to being ignored.
