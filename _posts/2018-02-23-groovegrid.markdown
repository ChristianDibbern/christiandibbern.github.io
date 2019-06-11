---
layout: post
title: Groovegrid
date: 2018-02-23
description: Groovegrid is a line of LED devices that can be controlled via smartphone.
  They display cool animations and users can play retro style games.
image: "/assets/images/Groovegrid.png"
tags:
- Dummy Text
- Moon Drinking
- Kale

---
In late 2017 an engineering buddy of mine, Phil and I started building a programmable LED light wall. We had just gotten an Ikea Kallax, a shelf that's made up of open cubes to store items. Optionally you can put doors on some of the cubes. But the doors that Ikea sells, while not unattractive, are quite plain. We took these doors as our canvas and put lights on it. We wired up the lights to a micro controller, enclosed everything with a sheet of plexiglass for a frosted look and coded a few animations for the device.

![](https://www.ikea.com/PIAimages/0644182_PE702466_S5.JPG#half "Ikea Kallax Shelf")

<div class='pics_in_a_row'>
<div style="flex: 1.3344;">
<img src='http://blimpage.com/pants/codepen/mm1.jpg'>
</div>
<div style="flex: 0.7505;">
<img src='http://blimpage.com/pants/codepen/mm3.jpg'>
</div>
</div>

Phil even designed a custom board for the project, which was eye opening to me. I didn't know you could have a low quantity of custom boards manufactured for so cheap. The manufacturer didn't charge extra to print on the board, so if I could think of a name for our project and create a logo while Phil worked on the circuit design, our board would be custom branded. That was enough motivation for me to get it done quickly.

![](/assets/images/Groovegrid-Board_edit.jpg#half)
![](/assets/images/Groovegrid-Board-Back_edit.jpg#half)
We had included 4 mechanical buttons onto the board, which were meant to select different animations, but of course they could also be used for other applications.
It occured to us that [2048](https://en.wikipedia.org/wiki/2048_(video_game)), the open source game that was very popular a few years prior, would be perfect for Groovegrid. The game takes place on a 4x4 grid, where the player can move around number tiles that add up to higher numbers and the goal is to go as high as possible. To make different number tiles easier to distinguish, in the original they have unique colors for each number. We just had to strip away the numbers and everything else could work. Developing this game for Groovegrid was the spark that we needed to take our project to the next level.

## Groovegrid V2

Because the buttons on the board were more of a hack than a convenient interface, the first thing we did was add a wireless module, so we could move controls off the board. The most readily available and easy to use controllers were the smartphones in our pockets, so we decided to go with them as our primary means of interaction.  
This was probably the most important step in the development process, because we suddenly had infinite possibilities of interaction. But with great possibility comes great responsibility to design a system that is cohesive and usable. The major tasks to accomplish were:

* Brand Design
* New Groovegrid devices
* Mobile App Design and Development
* Microcontroller Software Development

#### Brand Design

To get a better feeling 

![](https://i.ibb.co/SvJTYJD/Groove-Grid-Moodboard-Export-compressed.jpg#full)

<video autoplay="autoplay" loop="loop" muted playsinline style="width: 100%; height: auto;">
<source src="/assets/images/Groovegrid-Logo-Prototype.mp4" type="video/mp4" />
</video>

#### Groovegrid Devices

#### Mobile App Design

#### Mobile App Development

A while back, I had heard about Google's efforts to create a cross-platform app development framework called Flutter. I remember thinking it was very interesting, but I didn't have time to delve into it. When I wanted to start working on the mobile app, Google had just released version 1.0 of Flutter, so I was excited to use the new technology for our app.

#### Microcontroller Development