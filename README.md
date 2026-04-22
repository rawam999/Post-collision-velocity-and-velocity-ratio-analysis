# Droplet Collision and Post-Separation Velocity Analysis

This computational script processes high-speed droplet collision image sequences to measure:

- **Pre-collision droplet velocities**
- **Relative collision velocity**
- **Weber number (We)**
- **Impact parameter (B)**
- **Droplet diameter**
- **Post-separation droplet velocities**
- **Velocity restitution ratio** (`V_rel_post / V_rel_pre`)

The workflow is designed for analyzing binary or thresholded `.tif` image sequences of two droplets approaching, colliding, separating, and then moving apart.

---

## Overview

The script reads image frames from a specified folder, detects droplets frame by frame, and identifies:

1. **Collision start**  
   When two droplets become one connected region.

2. **Separation frame**  
   When the merged droplet breaks again into two separate regions.

3. **Pre-collision motion**  
   Used to compute individual velocities, relative velocity, Weber number, and impact parameter.

4. **Post-separation motion**  
   Used to compute rebound/separation velocities and the restitution ratio.

Finally, the script exports all measured quantities into an Excel file.

---

## Features

- Automatic detection of collision start and separation frame
- Circle detection using `imfindcircles`
- Pre-collision velocity calculation
- Post-separation velocity calculation
- Weber number and impact parameter estimation
- Size mismatch estimation between droplets
- Excel export of all results

---
