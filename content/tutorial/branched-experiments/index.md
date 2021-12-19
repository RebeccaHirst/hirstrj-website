---
title: Branched Experiments in PsychoPy
subtitle: Make an experiment that can take one of several routes depending on how your participants respond.

# Summary for listings and search engines
summary: Make an experiment that can take one of several routes depending on how your participants respond.

# Link this post with a project
projects: []

# Date published
date: "2016-04-20T00:00:00Z"

# Date updated
lastmod: "2020-12-13T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ""
  placement: 2
  preview_only: true

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

1. Make a consent routine, a trials routine and an end routine. 
2. In the consent routine add a keyboard component that allows either the Y or N key to be pressed. 
3. Add a code component to your consent routine.
4. In the code component use this in the **End Routine** tab:
```
if key_resp.keys == 'Y':
    trialLoopReps = 1
elif key_resp.keys == 'N':
    trialLoopReps = 0
```
5. Add a loop around the trials routine (and trials loop) and set nReps to `trialLoopReps`. if the participant does not consent, this part of the experiment will be skipped!

{{< youtube 45NRWjFiYK0 >}}

For more tutorials please see the <a href="https://www.youtube.com/c/psychopy_official" target="_blank">PsychoPy Youtube Channel</a>