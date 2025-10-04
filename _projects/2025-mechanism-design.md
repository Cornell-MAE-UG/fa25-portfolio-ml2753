---
layout: project
title: Mechanism Design
description: Mechanism for Maximum Lift
technologies: [Rhino 7]
image: /assets/images/mech-drawing.png
---

The problem asked to design a frame/mechanism to lift the maximum possible weight to the highest possible height in a 150cm long by 50cm tall bounding box. The components given include 3 pins supports (2 of which are mounted to the ground), a rigid bar, and a linear actuator chosen from [this catalog](https://www.tolomatic.com/wp-content/uploads/2022/05/2700-4000_29_IMA_cat.pdf), using the maximum force values only. The support and bar/actuator are assumed to be rigid.

![Image of the linear actuator]({{ "/assets/images/tolomatic_ima_series.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

The actuator chosen for the design is the IMA 44 Series with the BN10 Screw, with 11.03 kN peak thrust. The stroke is 457mm. See the catalog link above for more specifications.

The plan was to draw the free body diagram of the entire mechanism first at 50cm, with the stroke fully extended and exerting the maximum peak thrust force. The unknown force load is applied at the top to be solved for, which gives the maximum possible weight that can be held. Below are the calculations leading up to the design.

![Images of design process]({{ "/assets/images/mech.png" | relative_url }}){: style="width: 100%; height: auto;"}

The extended length of the actuator and rigid bar were calculated based on the specifications, then the exploded parts of the mechanisms were drawn as separate free body diagrams. Using the free body diagrams, the reaction forces were computed using force and moment balance equations. Using the moment balance about the pin connected to the rigid bar at the ground, the maximum force that can be held is 11.70 kN at 50 cm above ground level.

![Images of final design]({{ "/assets/images/mech-drawing.png" | relative_url }}){: style="width: 100%; height: auto;"}