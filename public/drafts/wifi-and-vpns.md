# WiFi and VPNs

This is going to be a fairly detailed post into my recent WiFi home broadband problems, how I solved it and then how I layered on a VPN and what I learnt from the process.

<!--more-->

## TL,DR

Buy a Netgear AC1900 R7000 (the router, not the router modem). This will kill competitor WiFi. At this point home WiFi went from a few meg around the house to a solid 100+mb is all rooms.

Get an AirVPN.org account. Tunnelblick is a nice mac client. When run directly on my Mac, I'll get ~60mb broadband at home (so a 3/5ths reduction).

Firmware patch the router with DD-WRT (which is relatively straightforward). Then enable the VPN service (detailed in this post). **The speeds with the VPN enabled on router are about 20mb**, which seems about as fast as the router can do the software encryption.

---

## Part 1: Home broadband problems

In recent months the internet at home has been pretty terrible given that our connection is supposed to be 100mb and upwards.

We'd been complaining for a long time over several support phone calls, but in the last call, the support technician decided to actually share some real knowledge with me. He seemed to pick up from my language that I was technical so it seemed to unlock his inner geek with me, and for it, I'm much more knowledgeable about how WiFi works.

### Bad WiFi != Bad connectivity

The problem is (generally) the WiFi radio bands are saturated. An easy way to rule out the internet connection and be sure that WiFi is the problem is: **plug into your home modem via (patch) cable and run a speed test.**

I found immediately that the speeds jumped from a couple of meg over WiFi to a good 80+mb over cable.

The technician then rattled off a list of other non-wifi devices that compete for the same radio airwaves:

- Bluetooth
- Microwaves
- Portable phones (extenuated when they're out of their cradles)
- The neighbours!

It also didn't help that I had a bag of 10 Bluetooth beacons between the WiFi modem and the area which I work from.

Using the Android tool, [Wifi Analzier](https://play.google.com/store/apps/details?id=com.farproc.wifi.analyzer&hl=en) (also on [Windows](https://www.microsoft.com/en-us/store/apps/wifi-analyzer/9nblggh33n0n), and similiar-ish for [Mac](https://itunes.apple.com/us/app/wifi-explorer/id494803304?mt=12)) I would check the status around the house. At the most, I counted 10 networks from one spot in the house  (note that this picture is *after* I fixed my wifi, so normally "sharp-wifi" would be at the same strength, if not lower, on the chart):

![wifi analysis of nearby connections](/images/wifi-at-home.jpg)

### Fixing the signal

There's a couple of solutions that I employed. Firstly I bought a pack of basic [powerline](https://www.amazon.co.uk/TP-LINK-AV500-Powerline-Adapter-Starter/dp/B0084Y9N3O/ref=sr_1_1?ie=UTF8&qid=1465158211&sr=8-1&keywords=TP-LINK+500Mbps) adapters (which also included two RJ45 cables) and I hardwired the TV to the modem. This fixed the problem of not being able to stream things like Netflix to the TV.







