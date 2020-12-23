## 555ADSR PCB/Panel set

This module is the spiritual successor to my old Kirschmann ADSR module which, whilst being very useful and an interesting use of CMOS ICs, required a fairly hefty trigger signal in order to work.

This is an updated envelope generator which uses a 555 timer configured as a Schmitt trigger (see: [https://www.nutsvolts.com/magazine/article/555-monostable-circuits](https://www.nutsvolts.com/magazine/article/555-monostable-circuits) - figure 15 in particular) from which the envelope is generated. The net result is something that not only triggers at around 1V but also has far fewer parts, particularly ICs, than the Kirschmann design.

I'm going to call that a win, and it isn't dissimilar to the design that Doepfer use in their EG modules, albeit without the bells and whistles.

In addition, I've 'borrowed' a couple of features from a Rene Schmitz design, specifically: the resistor R13 is optional, but adding it will give the input a bit of hysteresis (the degree of which is governed by the values of R13 - 1MΩ is what I use) which is handy if you're using a slowly changing waveform as a trigger.

Secondly, there's a buffer between the sustain and decay pots which removes any interdependence between the two. It also uses up an otherwise uncommitted op-amp.This is a PCB/panel set - it is up to you to source components for the build and actually build it. There are a few points to note, however:

-   Attack, decay and release tapers should be log taper - I recommend 1M audio. If you use smaller values, you should scale the decay/release capacitor, C4, accordingly (eg. if you use 100k pots for attack/decay then you should multiply the required capacitor value by 10)    
-   Pretty much anything goes for the value of C4 - 470nF is a good, general value. Use larger values if you're planning to use the module for pads, or smaller for percussive patches. Anything above around 4.7uF will yield ridiculously long attack/decay times.
-   For best results, use the CMOS version of the 555 - Renesas 7555 or TI SA555 are good choices; I've had mixed results with non-CMOS 555s. For the op-amp, a TL072 will work just fine.
-   The build also requires 4 surface-mount transistors but these are pre-soldered for you.  

**CURRENT DRAW (approx.):**

-   _20mA (+12)_
-   _5mA (-12)_

