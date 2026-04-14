# SGP-Mapping-Navigation

A hierarchical cross-domain aware navigation framework for amphibious robots in unstructured littoral environments.

This repository contains the implementation of our amphibious navigation framework that combines:

- **Sparse Gaussian Process (SGP)-based terrain mapping**
- **Uncertainty-aware local path planning**
- **Explicit cross-domain transition management** for answering:
  - **whether to cross**
  - **where to cross**

The framework is designed for local-online navigation at representative littoral land-water interfaces, where robots must operate under heterogeneous terrain conditions, degraded boundary perception, and uncertain transition risks.

---

## Overview

Autonomous navigation for amphibious robots is particularly challenging in unstructured littoral environments, where the robot must move across both land and water while handling terrain discontinuities, shallow-water perception degradation, and unstable water-land transitions.

To address these issues, this project implements a **hierarchical perception-mapping-planning framework** with three main components:

1. **Perception and Mapping**
   - LiDAR-based local terrain observation
   - Continuous terrain reconstruction using **Sparse Gaussian Processes (SGP)**
   - Estimation of:
     - elevation
     - terrain gradient
     - predictive variance (uncertainty)

2. **High-Level Cross-Domain Decision Layer**
   - Local-online structural transition triggering
   - Candidate crossing-point extraction and filtering
   - Risk-aware crossing-point selection

3. **Low-Level Motion Planning Layer**
   - **Uncertainty-Aware Traversability-Constrained D* Lite (UATC-D* Lite)**
   - Jointly considers:
     - terrain traversability
     - SGP-derived uncertainty
   - Generates adaptive and safer short-horizon paths in mixed land-water terrain

This repository includes both **simulation** and **real-world deployment** components.

---

## Key Features

- Continuous terrain mapping from sparse LiDAR point clouds
- Elevation and uncertainty estimation via Sparse Gaussian Processes
- Traversability and semantic map construction
- Explicit management of land-water transitions
- Risk-aware crossing-point selection
- Uncertainty-aware D* Lite path planning
- Support for both simulation and real-world robotic deployment
- Deployment-oriented implementation for embedded platforms

---

## Repository Structure
README.md
Simulation.zip
Real-World.zip
simulation point cloud.zip
