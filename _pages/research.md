---
title: "Research"
permalink: /research/
layout: single
author_profile: false
classes:
  - wide
  - nosidebar
---

I work on the reliability of machine learning systems that control physical
things &mdash; vehicles and robots. Broadly: hardware and software faults will
happen in deployed systems, and I want to know which ones actually matter for
safety, and how to spend a protection budget on those and not the rest.

## Fault Tolerance for Closed-Loop Autonomous Systems

Most work on protecting neural networks from hardware faults asks a single
question: does a fault corrupt the output of one inference? For an image
classifier that is the right question. For a vehicle running a policy inside a
feedback loop, it is not. The system produces many decisions per second, and the
vehicle and its controller correct as they go, so a large fraction of corrupted
outputs never reach the outcome at all.

I study the gap between those two views &mdash; how a fault behaves in a single
inference versus what it does to the closed loop over time &mdash; and what that
implies for where protection is worth paying for.

*Ongoing work.*

## Fault Injection for Vision-Language-Action Models

Vision-language-action (VLA) models are moving from research demos toward
deployment on embedded accelerators, where memory is not always ECC-protected
and a single upset can corrupt a weight that is then re-read for the rest of the
task. Existing robustness studies of these models perturb the *inputs* &mdash;
sensor noise, adversarial patches, physical degradation &mdash; but not the
computation itself.

I am building an evaluation platform that injects hardware faults into a VLA
policy and measures the effect end to end, comparing open-loop and closed-loop
behavior on the same faults.

*Ongoing work.*

## Safety Interventions for Driver Assistance Systems

Adversarial patches placed in the physical world can cause an open-source driver
assistance system to make unsafe decisions. This work characterizes those
failures and evaluates runtime interventions that keep the vehicle safe when the
perception stack is compromised.

C. Chen, G. Xiao, **D. Lee**, L. Yang, E. Smirni, H. Alemzadeh, and X. Zhou.
"Safety Interventions Against Adversarial Patches in an Open-Source Driver
Assistance System." *IEEE/IFIP International Conference on Dependable Systems
and Networks (DSN)*, 2025.

## Earlier Work

Before moving to systems reliability I worked on ultra-low-power mixed-signal
hardware &mdash; reconfigurable capacitance-to-digital converters and integrated
PPG sensing for wearable health devices &mdash; and on audio processing hardware
in industry. See [Publications](/publications/).
