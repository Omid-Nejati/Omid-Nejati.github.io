---
layout: page
title: Line Detection
description: Fast Drivable Area for Autonomous Driving
img: assets/img/line_det.gif
importance: 3
category: work
---

In Autonomous cars use images of the road to detect drivable areas, identify lanes, objects near the car, and necessary information. This information achieved from the road images are used to make suitable driving decisions for self-driving cars. Drivable area detection is a technique that segments the drivable parts of roads in the image. Modern methods often consider road detection as a pixel by pixel classification task, which is struggling to solve the problem of computational cost and speed. So to increase the speed of performance, we consider the process of drivable area recognition as a row-selection task. In this paper, special rows in the image are selected. Then, the boundaries of the drivable area are detected in these rows.
