# EMX3500 To Stereo Conversion

A "replacement" PCB for the [EMX3500](https://de.yamaha.com/files/download/other_assets/1/324571/EMX3500G.pdf) to convert the L/R-amplification stages and Graphic Equalizer (GEQ) to simple stereo amp.

![](/assets/soldered.jpg)


## What is this project?
EMX3500 is an older analog powered mixer by Yamaha, see the below image.
This project separates the mixing part from the amp part of the original product.
To this end, a custom PCB was designed to enable the removal of all unnecessary parts (channels, tape board, various input boards...the massive chassis)

This was required as, looking at the original PCBs (>10 individual PCBs), we find that
* The original PCBs are designed using single layer PCBs with star-grounding (with some PCBs (or parts thereof) directly grounded to the chassis, others via other PCBs)
* Many of mixers PCBs have multiple sub-circuits of different functionalities and its near impossible to remove any part without breaking the complete system

Hence, my conclusion was to refactor the needed circuit paths from a plethora of individual PCBS onto new single purpose PCBs.
This creates a creates a stand-alone stereo amp and, in the future, I can restore the mixer into its own device that can be connected to any stereo amp.

This repository currently contains the KiCad project for the stereo amp related PCB, that can be connected to the original GEQ and amp stages.
The circuit is more or less the original circuit, reduced to its minimal subset required to achieve the desired functionality.
At the same time, the star-grounding is changed in favor for simple 2-layer PCB design with a ground-plane.
I know, I know, hardcore-music aficionados with their bee-wax filled capacitors will cry themselves to sleep hearing this, but I can promise you...I sleep quite comfortably despite this alteration...

Further upgrades also include a small bluetooth module.


> **Note**:
> I am anything but a professional circuit designer. In fact, this was my first complete PCB design with manufacturing...

> **Warning**:
> The headphone related part of the PCB does not what you might think, and will be completely removed/changed in a future revision of this project.


## Why did you destroy a mixer? Why thou!?
By chance I got my hands on a fully-working EMX-3500 for 20EUR at an auction.
I did ***not expect*** this mixer to work at all, but to my surprise all 16-channels, GEQ, DSP board, etc all worked without a hiccup (except maybe slowly deteriorated pots...)
However, I bought it with the intention for salvaging parts for synth-related projects, but clearly this would have been a crime to destroy down to individual parts.

Nevertheless the housing wasn't in the most prestine condition: screws were rusted in (previous owner seemed to have stored it in a garage for an extended time period), one channel's XLR connector was broken in.
Also, and that was the major issue: I didn't have a space for nearly a gigantic and very heavy mixer in my apartment. I didn't plan for it... I was, however, in need for a new stereo amp :).
And the mixer part still exists as is and will be rebuilt into a smaller, independent unit.

## Before and after

![](/assets/pcb.png)

![](/assets/open_combined.jpg)

![](/assets/finished.jpg)
