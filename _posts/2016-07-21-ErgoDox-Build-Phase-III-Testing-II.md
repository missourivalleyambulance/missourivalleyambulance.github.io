---
layout: post
title: ErgoDox Phase III
subtitle: Testing, Part 2
---

<a class="embedly-card" href="https://gfycat.com/RedVainIberianemeraldlizard">RGB Underglow</a>
<script async src="//cdn.embedly.com/widgets/platform.js" charset="UTF-8"></script>

Basic RGB LED strip functionality has been implemented. I spent 3 days bashing my head against my desk trying to figure out how to implement this _and_ get the firmware to compile successfully. It turns out I'm not the first person to implement RGB LEDs on an ErgoDox; [u/wootpatoot](https://www.reddit.com/user/wootpatoot) on Reddit already built such a board. With a basic working firmware up and running, I can now begin work on trying to implement the strip on the left hand. 

Presently I've got the RGB strip wired to the Teensy's D5 pin, typically an unused port on ErgoDox. The next goal is to get the strip up and running on B6, and hopefully be able to control a strip on the left-hand without making any modifications to the PCB. B6 normally controls a standard LED on the right hand. Assuming my understanding of the PCB design is correct, signals sent on B6 are also sent (but not used) to the left hand as well. I'm hoping to get power from the left hand's unused USB pinout, and that the B6 signals just automatically carry over to the left hand. 

Worst case scenario, I can do like u/wootpatoot did, and run an additional wire over to the left hand - but I'm hoping to avoid that. 

### Update (7/29)

After many more days of pounding my head against my desk, I've been unable to find a way to drive the LED strip from the I/O expander. I've resigned myself to the fact that I'll need to run a 5th wire over to the left hand to drive the strip. 

The problem: ErgoDox is designed to use a 4 pin TRRS port & cable to connect the two hands. 

![](https://i.imgur.com/f3rsgax.jpg)

Solution: I'll use a mini-USB port instead, and run a cable with mini-USB on either end to connect the two hands. 

I ordered and received a breakout board from [Sparkfun](https://www.sparkfun.com/products/9966). I'll wire the board to the pinouts normally used for TRRS. 

![](https://i.imgur.com/NyplYT5.jpg)


Fortunately, the mini-USB port & breakout board will fit perfectly in the case. I'm hoping mounting the board to the case with hot glue will be sufficient. If all else, when I order the final carbon fiber plate for the production build I will add screw holes to mount the board to the plate. 

---
<p align="right">Typed on AEKII</p>