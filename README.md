Master’s Thesis — Preparation of a LAMMPS-FrameworkforLarge-ScaleParallel Replica Dynamics Simulations of Ablative Thermal Protection Material

Overview

This repository focuses on the system architecture and methodological overview; implementation-specific source code is not included.

The work focuses on extending the LAMMPS molecular dynamics framework to enable large-scale, long-timescale simulations of ablative thermal protection materials using a 
hybrid Parallel Replica Dynamics (PRD) and domain-decomposed parallelization strategy.

The goal is to overcome the inherent timescale limitations of classical molecular dynamics and enable simulation of rare-event driven physical processes relevant to 
thermal protection systems in aerospace applications.

Key Objectives
1. Extend LAMMPS for custom simulation workflows relevant to ablative materials
2. Implement a bond-breaking event detector for Parallel Replica Dynamics (PRD) simulations.
3. Combine PRD with spatial domain decomposition for scalable HPC execution
4. Enable microsecond-scale effective simulation times for large atomic systems

Features
1. Custom LAMMPS modifications in C++
2. MPI-based parallel execution framework
3. Parallel Replica Dynamics implementation for rare-event sampling
4. HPC-ready simulation setup (SLURM-compatible workflows)
5. Post-processing tools for trajectory and state analysis
6. Scalable architecture for large atomic systems

Methodology
1. Molecular Dynamics Base - Simulations are built on the LAMMPS MD engine, modeling atomic interactions using appropriate interatomic potentials for ablative materials.

2. Parallel Replica Dynamics (PRD) - The PRD approach accelerates simulation time by running multiple statistically independent replicas of the system in parallel, effectively sampling rare transition events.

3. Hybrid Parallelization Strategy - A combined approach is used:

Replica-level parallelism (PRD)
Spatial domain decomposition (MPI in LAMMPS)

This enables:

1. Efficient HPC scaling
2. Reduced wall-clock time for long-timescale processes
3. Improved sampling of rare physical transitions


Research Context and Contribution

This work contributes to the development of multiscale modeling frameworks for ablative thermal protection materials, with a focus on bridging atomistic-scale dynamics and macroscopic thermal response in extreme aerospace environments.

In particular, the thesis advances computational capabilities for rare-event-driven processes in ablative flows by integrating Parallel Replica Dynamics with scalable high-performance computing strategies. This enables the study of physically relevant long-timescale mechanisms, such as bond breaking and material degradation, that are otherwise inaccessible through conventional molecular dynamics.

The resulting framework supports improved predictive modeling of thermal protection systems by enhancing both temporal reach and spatial scalability in atomistic simulations.






