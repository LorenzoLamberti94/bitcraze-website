---
layout: page
title: Positioning Systems Overview
page_id: overview_positioning
redirects:
  - /docs/overview_positioning/
---
{%row%}
{%column 12%}
The Crazyflie 2.X (as most other quadcopters and robots) has no real notion of
its position in space. The on board sensors (accelerometers and gyros) can be
used to give a rough idea of its movements but lacks the accuracy for long term
position awareness. The solution is to use an external system that can provide
information of the current position.

## Lighthouse positioning System
{%endcolumn%}
{%endrow%}

{%row%}
{%column 3%}
![The Lighthouse system](/images/documentation/overview/lighthouse.png)
{%endcolumn%}

{%column 6%}
The lighthouse positioning system is our latest method of positioning on the Crazyflie 2.X. The [Lighthouse Base Stations](https://www.vive.com/eu/accessory/base-station2/) are used here, and they emit infrared laser scans that are detected by our [Lighthouse positioning deck](https://store.bitcraze.io/collections/positioning/products/lighthouse-positioning-deck). This enables the crazyflie to (like with the LPS) calculate its own position on board.
{%endcolumn%}

{%column 3%}
- [Lighthouse positioning documentation](/documentation/repository/crazyflie-firmware/master/functional-areas/lighthouse/).
{%endcolumn%}
{%endrow%}



{%row%}
{%column 12%}
## Loco Positioning System
{%endcolumn%}
{%endrow%}

{%row%}
{%column 3%}
![The LPS system](/images/documentation/overview/lpssystem.png)
{%endcolumn%}

{%column 6%}
The crazyflie can detect its position by means of our Loco Positioning System (LPS). Here we use UWB modules (Decawave's DWM1000), which can measure the distance between each other. With the ranges of at least 4, but rather 8, [Loco positioning nodes](https://store.bitcraze.io/collections/positioning/products/loco-positioning-node), and a [loco positioning deck](https://store.bitcraze.io/collections/positioning/products/loco-positioning-deck), the crazyflie can calculate its own position onboard. Our [roadrunner](https://store.bitcraze.io/collections/positioning/products/roadrunner) is a stand-alone tag which can also work with our LPS system, if you require another platform than the Crazyflie.
{%endcolumn%}

{%column 3%}
* {% id_link loco-pos-system-overview %}
{%endcolumn%}
{%endrow%}



{%row%}
{%column 12%}
## Motion Capture Positioning
{%endcolumn%}
{%endrow%}

{%row%}
{%column 3%}
![Motion capture system](/images/documentation/overview/motioncapture.png){:width="500px"}
{%endcolumn%}

{%column 6%}
The Crazyflie can be positioned using reflective markers and infrared motion capture cameras. We use [Qualysis](https://www.qualisys.com/) in our own office but researchers and hobbiest have used the Crazyflie with MCS cameras of [Vicon](https://www.vicon.com/) and [Optitrack](https://optitrack.com/) as well. The main principle of using the MCS for positioning is that the cameras emit infrared light, which are reflected back by special reflective markers. This will enable the IR-cameras to detect the location of the marker, which the MPC software on an external computer will calculate the actual position from. This information can then send to the Crazyflie through the Crazyradio PA. Also, check out our [motion capture marker deck](https://store.bitcraze.io/collections/decks/products/motion-capture-marker-deck).
{%endcolumn%}

{%column 3%}
 - [ USC's Crazyswarm documentation](https://crazyswarm.readthedocs.io/en/latest/).
{%endcolumn%}
{%endrow%}
