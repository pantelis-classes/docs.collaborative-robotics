---
title: Development Environment with AWS Robomaker
---

# Development Environment with AWS Robomaker


## Dev Guide

The single most important source of information on each AWS service is the developer guide. Robomaker's guide is [Here](https://docs.aws.amazon.com/robomaker/latest/dg/what-is-robomaker.html) 

## Cost Estimate and Management

The biggest [cost of the service](https://aws.amazon.com/robomaker/pricing/) is clearly associated with the simulation runs.  

With AWS RoboMaker simulation run, you only pay for the time your simulation job takes to run. There are no resources to manage, no upfront costs, and you are only charged when your simulation job is in “running” status. You are charged an hourly rate based on the number of Simulation Units (or SUs) required to run your simulation job. A single SU provides 1 vCPU and 2 GB of memory, and the number of SUs required to run your simulation job is determined by the maximum resource requirement between vCPU and memory. For example, if your simulation job requires 1 vCPU and 4 GB of memory to run, it will require 2 SUs. A simulation job requires a minimum of 1 SU. You are billed at an hourly SU rate in increments of 1 minute, rounded up to the nearest minute.

This is an example 

The number of SUs required by a simulation job scales with the complexity of your robot and simulation world. A typical ground mobility robot has one camera sensor, one Lidar sensor, and two actuators. A modestly complex simulation world like a warehouse or a retail store contains about 100 modeled objects. For reference, running a simulation job with a typical robot and a modestly complex simulation world as described above requires about 7 vCPUs and 14 GB of memory, or 7 SUs.

Let’s consider that your robotics application release cycle is once a month and during each release, you use RoboMaker simulation to run 100 hours of simulations for performance testing. Consider that your robot is like a typical ground mobility robot and your simulation world is like a typical warehouse as described above. Running your simulation job will require 7 SUs.

Monthly charges:

Total SU-hours used: 100 hours/month * 7 SUs = 700 SU-hours

RoboMaker simulation price per SU per hour: $0.40

Total charges: 700 SU-hours * $0.40/SU-hour = $280

