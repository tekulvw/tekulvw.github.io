---
layout: post
title: "BVH Converter"
category: Projects
tags:
 - python
 - code
 - mocap
---

In the fall of 2015 I began working for the University of Cincinnati's Simulation Lab as a contractor working for P&G.
The project was pretty simple; we needed to find a way to recreate a real space, virtually, with high precision on critical objects in a given scene.
We eventually settled on using a standard passive IR motion capture system with custom marker mounts for our critical objects.

The mocap system definitely had the precision we wanted and was capable of capturing the markers on all of our critical objects but we still had no way to take the mocap data and view it in design software (like Autodesk Maya).
Text based exports from the mocap software could only be done in a format named BVH (Biovision Hierarchy).
BVH is an interesting mathematical concept that keeps track of location data of connected points on a skeleton by actually storing an orientation of each point relative to it's parent.

For our use case, we couldn't use BVH directly (as Maya couldn't interpret it) and had to convert the orientation data back to true location data in a 3D space.
Surprisingly, there weren't a ton of open source converters available, and I ended up creating one based on an open source BVH viewer I'd found.

Github: [https://github.com/tekulvw/bvh-converter](https://github.com/tekulvw/bvh-converter "Github Repo")

PyPi: [https://pypi.org/project/bvh-converter/](https://pypi.org/project/bvh-converter/)
