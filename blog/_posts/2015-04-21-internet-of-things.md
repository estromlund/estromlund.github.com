---
layout: post
title: Internet of Things
---
I've been wanting to get back into hardware for a while now. After building a self-balancing mini-robot in my last semester at Berkeley, I have really only done software development. Lately I've had some time on my hands, and decided to check out the **Internet of Things**.

The "Internet of Things" -- I've been hearing this phrase for a while now, but never really stopped to consider what it is. Of course there are the obvious applications, and most people can probably quickly refer to the Apple Watch, Google Glass (RIP), Pebble, Fitbit, etc.

The thing is, those are all one category of applications -- wearables. Wearables to me are interesting, but I feel like this is a very specific category, and that this Internet of Things goes much further than a Fitbit, a heart rate monitor, and a fancy watch, all hooked up to the smartphone in your pocket.

## A little bit of research

So I decided to do a little research on the internet of things, and was pleasantly surprised to see that there are a lot of extremely interesting applications outside of wearables, and a lot of opportunities across the board.

### Home tech

One of the devices available today is Amazon's [Dash Button] (https://www.amazon.com/oc/dash-button).

Basically, the way these buttons work are that you stick them to something (say, your washing machine), then press it when you need more detergent. Amazon automatically deals with everything else, and that detergent arrives on your doorstep a day or so later. No need to go on Amazon itself, no need to do anything but press the button.

The problem to me was that it wasn't automatic, it required a manual step.

But then, as I was clicking around Amazon's website, I came across the developer section and the [Dash Replenishment Service](https://www.amazon.com/oc/dash-replenishment-service). Bingo.

The Dash Replenishment Service is basically an API that allows device makers to cut the manual button press out of the process. Refrigerator's water filter about to expire? It orders a new filter on it's own. Printer ink low? Your printer orders a new cartridge. This is part of the magic promised by the internet of things, and I can't wait until more devices are connected like this.

### Retail

Retail, I suppose, is another "obvious" application of the internet of things. It seems to be what Apple is focusing on with the iBeacon.

Just think about the Apple Store experience -- you can walk in, get information pushed to your phone automatically, grab a product, and pay. All that without speaking to anyone. Imagine if every store had this experience.

It wouldn't be too hard, and I'm sure there are many startups chasing this right now. With the prevalence of iBeacon (or similar Bluetooth LE device) manufacturers such as [Estimote](http://estimote.com/), [Gelo](http://www.gelosite.com/), [Gimbal](https://www.gimbal.com/), and [Sensorberg](http://www.sensorberg.com/), prices are going down. Right now, Gimbal (Qualcomm's offering) seems to be the cheapest at $5 per tag, and I can only imagine that prices will continue to sink due to competition and growing manufacturing competence.

With the availability of low cost Bluetooth LE beacons, why not just throw one in every package? or even embed them in products themselves?

## Opportunities for Makers

I think the most exciting thing about the **Internet of Things** is the opportunity for people define their own needs, and to build solutions without too much effort.

Many would probably say the same thing about software ("just learn to code!"), but I think the cost of entrance here is much lower. There are platforms out there like [littleBits](http://littlebits.cc/) and [Smart Living](http://www.smartliving.io/) which significantly lower the barrier to entry.

littleBits, for example, consists of several modules that you simply snap together like Legos. Want a temperature sensor to activate an mp3 player? Plug those two modules together, turn a dial, and it's done. Smart Living is a bit more complex, but comes with an internet platform and mobile application that allow easy customization based on IFTTT-like integrations with your calendar and other data sources.

For those with some more experience, or a willingness to learn, there are platforms like [Arduino](https://www.arduino.cc) and [Raspberry Pi](https://www.raspberrypi.org), and [tons](https://www.hackaday.com) of [resources](https://learn.adafruit.com) to [learn](http://startingelectronics.org/).

### Ideas

I, for one, thought it would be cool to check out some devices and see what I could make. I kinda just went for it and splurged on a Raspberry Pi, Arduino Starter Kit, and a [TI Sensortag](http://www.ti.com/sensortag-bt). Despite "splurging", this all came out to just around $100.

A quick note about the Sensortag -- this little guy is $29, has 10 sensors (temperature, light, magnet, sound, etc.), and displays all the data in an iPhone or Android app (you can also access the tag's Bluetooth services in a custom implementation). It's pretty awesome.

So what am I going to do with these components? I'm not sure yet, but I have some ideas:

- Use the Raspberry Pi + my external hard drive to run a [low cost Time Machine server](http://lifehacker.com/build-a-time-machine-backup-server-with-a-raspberry-pi-1629629222). I rarely back up my computer because I am never where the hard drive is plugged in, but if it happens automatically over WiFi, then great!

- Bedroom clapper light. Let's end some debates over who has to walk to the other side of the room to turn of the light when we go to sleep.

- Apartment buzzer -> iPhone. If the door to our entry is closed then we can't hear the buzzer. I'm sure there's some way to hook this up into an app that will notify me when someone is buzzing, and then let me allow entry without walking to the phone. This should even work when we're not home, and hopefully let us not miss as many deliveries.

- I'm probably going to throw the TI Sensortag in the refrigerator and use its temperature sensor to see what is going on in there. Our salads always come out frozen, no matter what temperature setting we choose.

- I really want to automate the heating in our apartment using temperature sensors in the various rooms, but we have radiators and I'm not sure what hardware would be needed to manually twist the knobs, or if that is even feasible.

- An electronic lock would be cool, but I'm not sure it would work in our old apartment's door.

- We don't have a smoke detector, and after the basement fire I'm thinking we should really get one. I could make one for fun, but I might want the real deal to actually protect us.

- With a motion or sound detector, I could shoot a message to a phone when the dishwasher or washing machine is done.

I'm realizing these are all home projects, which I suppose makes sense, but I wonder what else I could do outside of here.

Have you done any cool projects, or have any ideas? If so, I'd love to hear, so shoot me an email at [erik@erikstromlund.com](mailto:erik@erikstromlund.com).
