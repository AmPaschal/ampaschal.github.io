---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

## Introduction
Security vulnerabilities are the weaknesses in software that leads to many cyber attacks and security breaches.
Two kinds of vulnerabilities are especially prevalent today -- memory safety vulnerabilities and vulnerabilities introduced by software dependencies.

Common techniques for discovering these vulnerabilities, namely fuzzing (for memory safety vulnerabilities) and runtime isolation (for dependency vulnerabilities), have significant limitations -- fuzzing is non-deterministic and misses real vulnerabilities, and runtime isolation introduces high runtime overhead.

My PhD research explores new systematic and efficient techniques to discover these vulnerabilities, that overcomes these limitations.



## Theme 1: Discovering Memory Safety Vulnerabilities in Embedded Software

Embedded systems are critical infrastructure, yet their network stacks are notoriously difficult to secure due to hardware dependencies and complex state spaces. This leaves them vulnerable to memory safety exploits that traditional testing often misses.

My research addresses this through:
*   **Systematic Testing of Network Stacks**: I developed a targeted approach to detect packet validation vulnerabilities in embedded network stacks, identifying critical security flaws in widely used systems (ASE 2023).
*   **Verifying Memory Safety with Unit Proofs**: I led an empirical study on "Unit Proofs," a compositional bounded model checking technique. We demonstrated its effectiveness in mathematically verifying memory safety, offering a rigorous alternative to the non-determinism of fuzzing (ICSE 2026).

## Theme 2: Mitigating Vulnerabilities in Software Dependencies

Modern applications rely on thousands of third-party libraries, but this ecosystem is built on implicit trust, where a single compromised dependency can breach the entire system. Current defenses often lack the granularity needed to stop these attacks without breaking functionality.

My research addresses this through:
*   **Zero-Trust Dependencies (ZTD-Java)**: I proposed the Zero-Trust Dependencies paradigm to enforce the principle of least privilege within an application's dependencies. I implemented **ZTD_Java**, a tool that restricts software dependencies to only the permissions they strictly need, effectively mitigating supply chain attacks with minimal overhead (ICSE 2025).