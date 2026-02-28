# SENSE-UAV: Energy-Efficient Anomaly Detection and Information Fusion in Constrained UAVs via Spiking Neural Network Ensembles

## Overview
**SENSE-UAV** is a developing framework aimed at providing robust, energy-efficient anomaly and attack detection for highly constrained autonomous systems (micro, nano, and pico-quadrotors). 

Traditional Artificial Neural Networks are often too computationally heavy for the strict power budgets (~0.1 W to 10 W) of miniaturized drones. SENSE-UAV addresses this by utilizing the neuromorphic paradigm of Spiking Neural Networks (SNNs). The framework leverages PyTorch and snnTorch to build multi-sensor SNN ensembles capable of processing heterogeneous, high-frequency spatial-temporal data streams, specifically targeting Event-based vision, RGB cameras, and IMU data.

## Current Status
This repository is currently in the initial architectural phase. Active development, scaling, and hyper-parameter optimization of the SNN ensembles are planned to be conducted utilizing High-Performance Computing (HPC) resources. 

The core representation learning architecture draws scientific inspiration from recent state-of-the-art Visual-Inertial Odometry (VIO) paradigms, specifically:
* **DEIO (Deep Event Inertial Odometry):** Guan et al., ICCV 2025.
* **SuperEIO (Self-Supervised Event Feature Learning for Event Inertial Odometry):** Chen et al., arXiv 2025.

Unlike the baselines, SENSE-UAV translates these representation mechanisms into fully asynchronous, spike-based paradigms for optimal edge-deployment.

## Features (In Development)
* Multimodal SNN ensemble architectures (Event, RGB, IMU).
* Highly parallelized spatial-temporal dataloaders for continuous event-stream decoding (HDF5/ROS 2).
* Information fusion algorithms for detecting sensor spoofing, data poisoning, and hardware anomalies.
* Multi-GPU Distributed Data Parallel (DDP) training pipelines.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
