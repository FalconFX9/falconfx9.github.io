---
layout: post
title:  "Introducing the robot dog project!"
date:   2023-06-22 19:58 -0500
categories: robot-dog
published: true
---

# Overview

The goal of this project is to design and build an ultra-low-cost, highly capable, mostly 3D-printed robot dog, similar to the [Dingo][dingo-link].

[dingo-link]: https://www.youtube.com/watch?v=8KntOIgzUjY

# Objectives

Our initial goal is to construct the robot dog, and have a functioning platform we can use to build further functionality into, such as autonomous navigation.

## Design Goals

To accomplish this, we have several design goals we would like the mechanical platform to accomplish, including:

-statically and dynamically stable walking/running

-ability to walk over small obstacles

-perform a small jump

-recover from falls

# Constraints

While building something similar to the ever-so-famous [Spot][spot-link] platform would be great, our design is centered around the omnipresent constraint of cost.

This has several implications for our design. Chief of which is the scale of our design, and what motors we choose to use. All larger scale robots (industrial like [Spot][spot-link], or home-brew like [OpenDog][opendog-link]) tend to use some form of large brushless motor, be it direct-drive or through some form of gearbox. These are prohibitively expensive on their own, and require even more expensive controllers (such as the [ODrive][odrive-link]) to run. Given that we require 12 motors (3 for each leg due to the dual-axis hip joint), we would have to spend several hundreds of dollars on just motors, too much for a hobby project.
This leaves us with two other options: geared brushed DC motors with encoders, or hobby-grade servos. While geared DC motors offer a middle-ground (lower cost than brushless systems, very accurate with a decent encoder...) the fact that they still require drivers, and their relatively poor performance-to-weight make them difficult to justify when compared to RC Servos with similar performance, at much lower cost (such as the [DS3230-Pro][ds3230-link]), which also don't require any drivers, and given that we are not building a pick-and-place system, the relatively poor accuracy of such hobby-grade servos is acceptable.


[spot-link]: https://www.bostondynamics.com/products/spot
[opendog-link]: https://github.com/XRobots/openDogV3
[odrive-link]: https://odriverobotics.com/
[ds3230-link]: https://www.aliexpress.com/item/1943129663.html