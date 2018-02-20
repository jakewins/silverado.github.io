---
layout: post
title: What are the ECM units in a 2009 Silverado?
date: 2018-02-20
type: post
published: true
status: publish
comments: true
categories:
- Electrical
tags:
- electronics
- ecu
author:
  display_name: Davis-Hansson
---

If you read about the various embedded computers, "ECM"s or "ECU"s, in your vehicle, you'll quickly find there are several separate modules, not a single central computer.
What are the ECUs inside a 2009 GM truck?

<!--more-->

## Networks

The 2009 Silverado has two CAN networks - a slower, cheaper, one for not-so-important things, like your radio, and a faster more expensive one for key components.

Attached to these two networks are electronic control units, ECUs.
By splitting the control into multiple separate computers, the vehicle may be able to handle partial failures.
For instance, if your VCIM ECU fails, you'll lose OnStar - but your engine will keep running as if nothing had happened.

One thing to watch out for is that some refer to a specific ECU - the one in charge of controlling the actual engine - an "Engine Control Unit"; this is then unhelpfully abbreviated "ECU".
As such, you may find that when people say "ECU", they either mean the *specific* ECU that controls your engine - normally called the ECM ("Engine Control Module") or PCM ("Powertrain Control Module") - or they mean "ECU" as in "Electronic Control Unit", referring to any of the many control units in your car.

Here, I'll refer to the general idea of a computer connected to the CAN network as an "ECU", and to the specific computer that controls your engine "ECM".

## The High Speed Bus, "HS-CAN"/"GMLAN"

The HS-CAN network contains the critical system components, and this post will exclusively talk about the components connected to this network.
HS-CAN is a two-wire protocol wired into pin 6 and 14 on a GM truck; GM refers to it as "GMLAN".

### VCIM - "Vehicle Communications Interface Module"

![Standard non-bluetooth VCIM]({{ site.baseurl }}/public/assets/2018-02/vcim.jpeg)

This is the OnStar system.
It'll either be a simple onstar-only module, or a mode advanced one that also serves to connect your phone to the audio system via bluetooth.

This module is located under the dash, above the radio.

### TCCM - "Transfer Case Control Module"

![TCCM location]({{ site.baseurl }}/public/assets/2018-02/tccm.gif)

The TCCM is the component responsible for switching between 2WD and 4WD.
It picks up signals from the 4WD controls and converts them into mechanical action in your [transfer case](https://en.wikipedia.org/wiki/Transfer_case).

### EBCM - "Electronic Brake Control Module"

![2009 GM EBCM]({{ site.baseurl }}/public/assets/2018-02/ebcm.jpg)

Also called "ABS Pump Module" or "Brake Pump Control Module", this computer is in charge of the [ABS brakes](https://en.wikipedia.org/wiki/Anti-lock_braking_system#Components).

### FSCM - "Fuel Pump Control Module"

![After market FSCM]({{ site.baseurl }}/public/assets/2018-02/fscm.jpg)

As the name makes rather clear, this is a dedicated ECU for the vehicles fuel pump.
Its job is to monitor the fuel pressure sensor, and react to changes in pressure by increasing or reducing the fuel pump speed.

### BCM - "Body Control Module"

![Body Control Module]({{ site.baseurl }}/public/assets/2018-02/fscm.jpg)

This ECU is kind of a dumping ground for a large slew of features; it's the closest you might get to the idea of a "central" computer.
By combining a large series of features into one ECU, cost is reduced.

The BCM on a Silverado is, for instance, the component that deals with security functions like the anti-theft systems.
It also controls things on your dashboard, headlights, A/C and your horn, to name a few things.

### TCM - "Transmission Control Module"

![TCM]({{ site.baseurl }}/public/assets/2018-02/tcm.png)

Also called the TCU, "Transmission Control Unit", this is the ECU managing the the automatic transmission.
The TCM is where a large series of the vehicles sensors are connected - wheel speed sensors, vehicle speed sensor, and throttle suspension sensor, to name a few.
Using the input from those sensors, the TCM then drives solenoids to control the gear box.

Wikipedia has a [rather large article on this particlar ECU](https://en.wikipedia.org/wiki/Transmission_control_unit).

### ECM - "Engine Control Module"

![After-market Engine Control Module]({{ site.baseurl }}/public/assets/2018-02/ecm.png)

Also called PCM, "Powertrain Control Module", or, confusingly, ECU, "Engine Control Unit".

This is the party wagon - this ECU is the one that [directly controls the engine](https://en.wikipedia.org/wiki/Powertrain_control_module).
It's got a wide array of sensors and a wide array of control outputs for managing the firing of your cylinders, tracking malfunctions, tuning the fuel/air mix and much more.
