# Hierarchical Morphospace Simulator

[![GitHub Pages](https://img.shields.io/badge/Live_Demo-GitHub_Pages-blue?logo=github&logoColor=white)](https://albertogonzalezcasarrubios.github.io/hierarchical-morphospace-simulator/)
[![Zenodo DOI](https://img.shields.io/badge/Zenodo-10.5281/zenodo.20693984-blue.svg)](https://doi.org/10.5281/zenodo.20693984)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

This repository constitutes the **Online Supplementary Material** for the paper:  
> *"How much diversity is lost in classification? Morphospaces as a metric of taxonomic impact"* > **Journal:** *Biological Theory* (2026) | **Author:** Alberto González-Casarrubios | **DOI:** https://doi.org/10.1007/s13752-026-XXXXX-X

---

### Project Links
* **Interactive Live Simulation:** [GitHub Pages](https://albertogonzalezcasarrubios.github.io/hierarchical-morphospace-simulator/)
* **Permanent Code Archive:** [Repository on Zenodo](https://doi.org/10.5281/zenodo.20693984)
* **Research Paper:** [Biological Theory (DOI)](https://doi.org/10.1007/s13752-026-XXXXX-X)

---

### Application Summary
The **Hierarchical Morphospace Simulator** is an open-source web application that models the mathematical framework presented in the paper. It provides a visual interface to analyze the taxonomic impact in biological diversity. The application runs directly in the browser without installation and calculates all metrics in real-time.

---

### Theoretical Summary
The simulator models biological diversity across three nested hierarchical levels, based on a shared set of discrete morphological characters:

1. **Theoretical Morphospace ($\Omega$):** The complete set of all mathematically possible combinations of characters. Its total size is the product of the domain sizes of its variables:
   $$|\Omega| = \prod_{i=1}^n |D_i|$$
2. **Ontological Morphospace ($\Omega_O$):** The sub-space containing only the morphotypes that satisfy biological constraints ($C_O$), representing the limits of physical or developmental viability:
   $$\Omega_O = \{x \in \Omega \mid \forall c \in C_O, c(x) = \text{"True"}\}$$
3. **Epistemic Morphospace ($\Omega_E$):** The quotient space generated when taxonomic rules ($\sim_E$) are applied to the ontological space, grouping individual morphotypes into species categories:
   $$\Omega_E = \Omega_O / \sim_E$$

#### Metrics Tracked:
* **Lumping Factor ($L$):** Measures the average number of distinct biological morphotypes grouped under a single species category:
   $$L = \frac{|\Omega_O|}{|\Omega_E|}$$
* **Epistemic Gap ($I_E$):** Measures the informational cost of the classification in bits (using Hartley entropy), showing the volume of morphological variation that becomes hidden within the taxonomic categories:
   $$I_E = \log_2(L)$$

---

### How to Use the Application & Controls
The interface consists of a control panel and a visualization canvas:

* **Visualization:** Switch between 2D projections and 3D point clouds (using Three.js). You can rotate, pan, and zoom the 3D view using the mouse.
* **Biological Constraints:** Adjust the distribution of viable morphotypes ($\Omega_O$) by selecting *Uniform*, *Geometric*, or *Clumped* patterns to simulate different biological scenarios.
* **Taxonomic Slider:** Move the slider between *Lumper* and *Splitter* to change taxonomic rules. The interface updates in real-time to show how species numbers change and how the Epistemic Gap ($I_E$) grows.
* **Camera and Export:** Use the quick-camera buttons (ISO, TOP, FNT, SDE) to snap to standard views.
---

### Citations
If you use this simulation, its source code, or the theoretical framework in your research, please cite both the paper and the repository:

#### Research Paper:
González-Casarrubios, A. (2026). How much diversity is lost in classification? Morphospaces as a metric of taxonomic impact. Biological Theory. [[https://doi.org/10.1007/s13752-026-00549-4](https://doi.org/10.1007/s13752-026-00549-4)]

#### Software Repository (Zenodo):
González-Casarrubios, A. (2026). Hierarchical Morphospace Simulator (v1.0). In Biological Theory. Zenodo. [https://doi.org/10.5281/zenodo.20693984]

---

### License
This project, including its software code and visual assets, is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0) License.

You are free to share, copy, redistribute, remix, transform, and build upon this material for any purpose (even commercially), provided that you give appropriate credit to the original author, provide a link to the license, and indicate if changes were made.
