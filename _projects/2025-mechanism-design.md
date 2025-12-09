---
layout: project
title: Mechanism Design
description: Mechanism for Maximum Lift
technologies: [Rhinoceros 3D]
image: /assets/images/mech-drawing.jpg
---


**STEP ONE.** The bar is treated as rigid, and a static analysis is performed to determine reactions and optimize the mechanism layout within the given constraints.

**Problem constraints, objectives, and degrees of freedom.** The design problem required creating a frame/mechanism capable of lifting the maximum possible weight to the highest point within a 150 cm × 50 cm bounding box. The components provided included three pin supports (two mounted to the ground), a rigid bar, and a linear actuator selected from [this catalog](https://www.tolomatic.com/wp-content/uploads/2022/05/2700-4000_29_IMA_cat.pdf), using only the maximum force values. The supports and bar/actuator were assumed rigid. With the two ground-mounted pins constraining translation and the actuator controlling linear motion, the bar had one primary degree of freedom: rotation about the pin axis as it lifted the load.

![Image of the linear actuator]({{ "/assets/images/tolomatic_ima_series.jpg" | relative_url }}){: .inline-image-r style="width: 200px"}

The actuator chosen for the design is the IMA 44 Series with the BN10 Screw, with 11.03 kN peak thrust. The stroke is 457 mm. See the catalog link above for more specifications.

**Static analysis.** The analysis began by drawing the free body diagram of the entire mechanism with the actuator fully extended to 50 cm, applying its maximum peak thrust force. An unknown load was applied at the top, representing the maximum weight the mechanism could support.

![Images of design process]({{ "/assets/images/mech.png" | relative_url }}){: style="width: 100%; height: auto;"}

The extended lengths of the actuator and rigid bar were determined from the specifications, and the mechanism was broken into individual components with separate free body diagrams. Reaction forces were then calculated using force and moment equilibrium equations. By taking the moment about the pin connecting the rigid bar to the ground, the maximum weight the mechanism could support was determined to be 11.70 kN at 50 cm above ground level.

**Final mechanism design.**

![Images of design process]({{ "/assets/images/mech-fbds.jpg" | relative_url }}){: style="width: 100%; height: auto;"}
![Images of final design]({{ "/assets/images/mech-drawing.jpg" | relative_url }}){: style="width: 100%; height: auto;"}

**STEP TWO.** The bar is treated as a flexible beam, with transverse deflection due to self-weight analyzed and a cross-section/material selected to keep vertical deflection below 2% of its length.

**Maximum deflection in beam.** Since the Step 1 mechanism applied forces only at the ends of the bar, the bar experienced primarily axial loads, analogous to a truss member. After consulting with Professor Royer and the TA, it was decided that bending analysis was therefore limited to its self-weight. The bar was modeled as a steel beam with a 10 mm × 10 mm cross-section, and the uniformly distributed load was calculated from its density. Because the bar was diagonal under loading, only the transverse components were considered, and axial forces were ignored for bending analysis, allowing it to be treated as a simply-supported beam. Using the maximum deflection formula for a uniformly distributed load (Appendix E), the maximum deflection of the bar was approximately 0.791 mm.

![Images of design process]({{ "/assets/images/mech2.JPG" | relative_url }}){: style="width: 100%; height: auto;"}
![Images of design process]({{ "/assets/images/mech3.JPG" | relative_url }}){: style="width: 100%; height: auto;"}

**Beam design.** Although the original 10 mm × 10 mm cross-section was sufficient for the design, experiencing only 0.791 mm of deflection, the design was further optimized by adopting a deeper rectangular cross-section with the same steel area, resulting in a 5 mm × 20 mm beam. The mechanism from Step 1 inherently resists bending, so deflection was negligible in the optimized section, measuring only 0.198 mm, or 0.018% of its length, far below the 2% limit. While this analysis did not consider it, buckling may be a more critical factor due to the axial compressive loads from the pinned supports combined with the maximum weight and linear actuator force at the bar ends.

**Final beam design.**
![Images of final design]({{ "/assets/images/mech-drawing2.jpg" | relative_url }}){: style="width: 100%; height: auto;"}