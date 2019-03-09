---
layout: post
title: Optimization of highly excited matrix product states
date: 2019-03-08 13:15:00
tags: website
author: Author
author_profile: true
excerpt: We present an implementation of shift-and-invert techniques and folded operators to target high-lying excited states expressed as matrix product states.
header:
  overlay_image: /assets/images/post_headers/baiardi_vdmrg2.png
  overlay_filter: 0.5
classes: wide
---
The wave function of a density matrix renormalization group (DMRG) calculation is represented as a matrix product state (MPS). Because DMRG is a ground-state method, excited states have to be calculated by a ground-state search in the space orthogonal to the already optimized lower-lying states. This is very impractical, especially for vibrational wave functions, where for large molecules the modes with high intensity are high in energy.
In our current [paper](https://aip.scitation.org/doi/full/10.1063/1.5068747) we show how a combination of root-homing algorithms and shift-and-invert Hamiltonians or folded Hamiltonians allows us to efficiently optimize high-lying states directly. As the optimization is now independent from the optimzation of lower-lying states, these calculations are trivially parallelizable. Besides a thorough investigation of the performance of these methods, we apply them to the calculation of highly-excited vibrational states of ethylene and a dipeptide. We also demonstrate how a sampling reconstruction scheme for vibrational MPSs can aid the classification of a vibrational state as fundamental, overtone or combination band and how it allows us detect anharmonic couplings.
Many thanks go to [Alberto Baiardi](https://scholar.google.ch/citations?user=mg0WlTkAAAAJ&hl=en&oi=ao) who did by far the biggest part of the implementation as well as ourPIs  [Vincenzo Barone](http://dreams.sns.it) and [Markus Reiher](http://www.reiher.ethz.ch) for their great and encouraging supervision.

