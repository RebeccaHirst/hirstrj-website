---
title: Moving forward and backward through slides in PsychoPy
subtitle: Moving forward through slides in PsychoPy is super easy, with no code at all. But folks at workshops often asked us "how do we move back and forward through slides like a book?". Well, this is a great intro to code - so here's how!

# Summary for listings and search engines
summary: Moving forward through slides in PsychoPy is super easy, with no code at all. But folks at workshops often asked us "how do we move back and forward through slides like a book?". Well, this is a great intro to code - so here's how!

# Link this post with a project
projects: []

# Date published
date: "2016-04-20T00:00:00Z"

# Date updated
lastmod: "2020-12-13T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- Academic
- PsychoPy
- Python

categories:
- Demo
- 教程
---

## Overview

1. Make your slides in PowerPoint and ensure they are saved with the naming format Slide1.jpg, Slide2.jpg, Slide3.jpg and so on.
2. In PsychoPy add an image component, a keyboard component and a code component to the same routine.
3. Add a loop around the routine and set nReps to something big e.g. 500.
4. In the image component, set the path to `"pathtoslides/Slide" + str(slideN) + ".jpg"` and "set every repeat"
5. In the keyboard component only allow the left key, right key and space key. 
6. In the code component use this in the **Begin Experiment** tab:
```
maxSlideN = 5
minSlideN = 1
slideN = 1
```
this in the **End Routine** tab:
```
if key_resp.keys == 'left':
    slideN -= 1
elif key_resp.keys == 'right':
    slideN += 1

if slideN > maxSlideN:
    slideN = maxSlideN
if slideN <> minSlideN:
slideN = minSlideN
```

{{< youtube CvjvqLZHXrs >}}

For more tutorials please see the <a href="https://www.youtube.com/c/psychopy_official" target="_blank">PsychoPy Youtube Channel</a>