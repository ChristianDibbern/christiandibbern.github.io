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
In late 2017 an engineering buddy of mine, Phil and I started building a programmable LED light wall. We had just gotten an Ikea Kallax, a shelf that's made up of open cubes to store items. Optionally you can put doors on some of the cubes. But the doors that Ikea sells, while not unattractive, are quite plain. We took these doors as our canvas and put lights on them. We wired up the lights to a micro controller, enclosed everything with a sheet of plexiglass for a frosted look and coded a few animations for the device.

<div class='pics_in_a_row'>
<div style="flex: 1.0;">
<img src='https://www.ikea.com/PIAimages/0644182_PE702466_S5.JPG'>
</div>
<div style="flex: 0.75018;">
<img src='https://i.ibb.co/7KnNZj8/Groovegrid-Door-edit-compressed.jpg'>
</div>
</div>

Guided by our first prototype Phil designed multiple generations of custom circuit boards over the course of the project. Below is the first generation with our initial logo.

![](/assets/images/Groovegrid-Board_edit.jpg#half)
![](/assets/images/Groovegrid-Board-Back_edit.jpg#half) We had included 4 mechanical buttons onto the initial test board, which were meant to select different animations, but of course they could also be used for other applications. It occured to us that [2048](https://en.wikipedia.org/wiki/2048_(video_game)), the open source game that was very popular a few years prior, would be perfect for Groovegrid. It‘s actually simple enough that it can be adapted to works on 4x4 pixel display. Developing this game for Groovegrid was the spark we needed to take our project to the next level.

<video autoplay="autoplay" loop="loop" muted playsinline style="width: 100%; height: auto; margin-bottom: 30px;">
<source src="/assets/images/Groovegrid2048_trim_compressed.mp4" type="video/mp4" />
</video>

## Groovegrid V2

Because the buttons on the board were more of a hack than a convenient interface, the first thing we did was add a wireless module, so we could move controls off the board. The most readily available controllers were the smartphones in our pockets, so we decided to go with them as our primary means of interaction.  
This was probably the most important step in the development process, because we suddenly had infinite possibilities of interaction. But with 

### Brand Design

To get a better feeling for what the Groovegrid brand could be I started out by thinking of possible target audiences. Groovegrid has three main use cases:

* Retro Gaming
* Mood Lighting
* Party Lighting

For the brand I wanted to create a retro feeling of 80s dance, Tron, Neon Lights. I was especially inspired by the Miami Heat basketball team. They created a [Vice special edition jersey collection](https://www.adsoftheworld.com/media/design/miami_heat_nike_uniform "Miami Heat Vice Jersey Behind the Scenes") that was going in a similar direction.

![](https://i.ibb.co/SvJTYJD/Groove-Grid-Moodboard-Export-compressed.jpg#full)

Next, I wanted to tackle the logo. My original design (center of the image below) was a juxtaposition of Grid set in a blocky pixel typeface and Groove set in Futura, which feels very rounded due to its geometric nature. With this style I meant to convey both a sense of fun and "grooviness" and a sense of retro digital. The design was not without problems, though. The main issue was the pixel G. It's drawn on a solid rectangle that is meant to symbolize a Groovegrid display. But this causes too much emphasis on the letter, its background overshoots the cap height by a significant amount. I experimented with a few variations, some of which are depicted below, but nothing felt quite right.

![](https://i.ibb.co/KLC31gn/Groovegrid-Logo-Tweaking-Process.png#full)

I eventually came to the conclusion that the pixel typeface I used just didn't fit, I needed custom letterforms. So I took a step back and suddenly it hit me. The pixel type would only feel right if it could work on Groovegrid. Which meant each letter would have to be reproducible on 4x4 pixels. I was surprised by the amount of different glyphs I could come up with for a single character.

![](https://i.ibb.co/LvqxBkB/Groovegrid-G-Entwuerfe-edit.jpg)

Above you can see a few different ideas for the letter G, some of which don't feel like a G at all. I was trying to see how far I could push the character before it would become unrecognizable. I was delighted when I realized that one of my concepts for an uppercase G would become a lowercase g when rotated 90°. From this coincidence I prototyped an animated logo on paper:

<video autoplay="autoplay" loop="loop" muted playsinline style="width: 100%; height: auto;">
<source src="/assets/images/Groovegrid-Logo-Prototype.mp4" type="video/mp4" />
</video>

At first I only meant to insert my custom type into the old logo design, but I was very intrigued with the new animated design. Around this time, Phil and I were also talking about manufacturing more Groovegrid devices with vastly different form factors, so the square around the G in the old design, meant to signify a Groovegrid display, was losing relevance. The meaning the new design loses by dropping Futura and going full pixel type, to me it makes up for in quirkiness. It also regains the feeling of grooviness when printed in color. Additionally, the new logo feels more cohesive.

![](https://i.ibb.co/H4W8jD3/Groovegrid-Logo.png)

### Groovegrid Devices

Our first Groovegrid device was a 4x4 pixel Kallax shelf door and while we have plans to build a higher resolution version that can stand on its own or be hung on the wall, for our second prototype, we wanted to go bigger, much bigger. In fact, we built a 2x0.5m table that houses almost 600 individual LEDs.

![](https://i.ibb.co/dgSykyc/Table-Making-Of-edit.jpg#half)
![](https://i.ibb.co/pP9n647/Table-Making-Of-2-edit.jpg#half)

The table form factor with its higher resolution allows for more possibilities in app design. We've already developed versions of Snake and Flappy Bird for the table and are in the process of implementing a multiplayer system. Upcoming multiplayer games are: an adaptation of the board game [Battleship](https://en.wikipedia.org/wiki/Battleship_(game)) and [Pong](https://en.wikipedia.org/wiki/Pong). In the case of pong we're about to experiment with using actual physical paddles on the table to control the game.

<video autoplay="autoplay" loop="loop" muted playsinline style="width: 100%; height: auto; margin-bottom: 30px;">
<source src="/assets/images/Groovegrid-Table-Animation_trim_compressed.mp4" type="video/mp4" />
</video>

### Mobile App Design

The Groovegrid remote mobile app has two main tasks to accomplish. Launching Groovegrid applications and providing individual controls for them. The mobile app's home screen displays two tabs that contain a list of the available animations and games, respectively. When an application is running, a button is docked to the tab bar, that provides access to the application's control screen. Because there's nothing the mobile app can do while disconnected, the whole UI is grayed out to signify the state to the user.

![](https://i.ibb.co/L90XBSw/App-Homescreen-Disconnected.png#half)
![](https://i.ibb.co/Rgw6qcw/App-Homescreen.png#half)

Most games we have in mind require only simple controls, such as "Tap to Jump" or "Swipe to Move". Since the smartphone as an input device provides a great amount of freedom, we want to make use of this. For a clone of the boardgame [Battleship](https://en.wikipedia.org/wiki/Battleship_(game)) we use the phone as a second screen, so the players can place their ships privately, while the main action takes place on the Groovegrid. Maybe we can find some interesting uses for augmented reality, to use a high resolution display in conjunction with an ultra low resolution display.

<div>
<video autoplay="autoplay" loop="loop" muted playsinline class="half center" style="margin-bottom: 30px;">
<source src="/assets/images/Battleship_collision-highlighting_trim_compressed.mp4" type="video/mp4" />
</video>
</div>

### Mobile App Development

A while back, I had heard about Google's efforts to create a cross-platform mobile app development framework called [Flutter](https://flutter.dev "Flutter"). In Flutter, most code is only written once in Google's own Dart language, which can run in a virtual machine for fast development cycles, or be ahead of time compiled for a final release. Developers can also access native device APIs to interface with hardware components like bluetooth using Java and Kotlin or Objective-C and Swift, respectively. I remember thinking it was very interesting, but I didn't have time to delve into it. When I wanted to start working on the Groovegrid mobile app, Google had just released version 1.0 of Flutter, so I was excited to use the new technology for our app.

I structured the mobile app into layers and embedded the BLoC (Business Logic Components) pattern that Google presented at their I/O conference in 2018. It takes advantage of Dart Streams to provide a clean, reactive way to manage state and works really well with Flutter. All communication between layers is handled via Streams to avoid static circular dependencies. I chose to follow this pattern because at its core the app is just a bluetooth remote. That means basically everything in the app happens asynchronously, which is why reactive programming lends itself very well to this project.

{% comment %}

Flutter uses Google's own Dart language for development. The Dart code can either run in a virtual machine or be compiled to native code. This enables a great development workflow with sub second hot reload, while also making releases fast and buttery smooth with AOT compilation. This is especially advantageous for UI development, I can make a change, hit save and my changes immediately show up on my connected device. What I like most about Flutter is UI-as-code. In contrast to native device frameworks, Flutter doesn't have a separate UI markup language or a UI Builder. Instead the Dart language features allow it to be used in a declarative manner to specify UIs. The upside here is that you can always rely on the power of code when declaring UIs.

I was able to write all UI and business logic in Dart, but Flutter doesn't expose all device hardware directly to Dart.  
The core of the mobile app is bluetooth communication between the phone and Groovegrid, so I needed a way to use the bluetooth module. Flutter enables this via platform channels, that allow access to native device APIs. Platform channels are written in the target device's native language. On Android you can use Java or Kotlin, on iOS it's Objective-C or Swift.

{% endcomment %}

{% comment %}

### Microcontroller Development

The micro controller on our board runs all Groovegrid applications and drives the LED grid. Code is written in C++ on the Arduino platform. The codebase is mostly maintained by Phil, because it tightly integrates with the hardware, which is his area of expertise. Since he doesn't have much experience with object oriented programming, I try to give some guidance on best practices and architecture. This is also a challenge for me, because I haven't really worked with C++ before and it can be quite different than more modern high level languages at times.

{% endcomment %}