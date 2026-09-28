#  The Frog - Polycarbonate Strip-Based Jumping Robot

A mechanically actuated jumping robot designed and fabricated using **polycarbonate strips as energy-storage elements**. The project investigates how elastic energy stored in slender flexible strips can be converted into rapid jumping motion.

**Research Internship | Mechanics & Computation Lab, Indian Institute of Science**
**Guide:** Prof. Ramsharan Rangranjan
**Duration:** May 2026 – July 2026

---

## Overview

**The Frog** is a jumping robot that uses the elastic energy stored in pre-deformed **polycarbonate strips** to generate a rapid upward impulse.

The project combined:

* Mechanical design and fabrication
* Nonlinear mechanics of flexible strips
* Numerical solution of boundary value problems
* Experimental characterization of jumping performance
* Multi-strip scaling analysis

The robot achieved a **maximum jump height of approximately 1 m**.

---

## Key Results

| Parameter              | Result                                                       |
| ---------------------- | ------------------------------------------------------------ |
| Maximum jump height    | **~1 m**                                                     |
| Strip material         | **Polycarbonate**                                            |
| Mechanical model       | **Nonlinear elastica**                                       |
| Numerical solver       | **`scipy.solve_bvp`**                                        |
| Multi-strip efficiency | **96% → 52%** when doubling strip count                      |
| Model improvement      | **32% higher accuracy** than conventional sine approximation |

---

## Mechanical Design

The jumping mechanism uses **thin polycarbonate strips** as compliant energy-storage elements.

The strips are deformed and store elastic potential energy. Upon release, this stored energy is rapidly converted into kinetic energy, producing the jumping motion.

The overall process can be represented as:

**Strip deformation → Elastic energy storage → Release → Rapid energy transfer → Jump**

The design was iteratively developed and fabricated to experimentally study the relationship between strip deformation, stored energy, and jumping performance.

---

## Nonlinear Elastica Model

For large deformations, a polycarbonate strip cannot be accurately described using small-deflection beam theory. The project therefore modeled the strip using the **nonlinear elastica formulation**.

The governing equations were formulated as a **boundary value problem (BVP)** and solved numerically in Python using:

```python
scipy.integrate.solve_bvp
```

The nonlinear model captures the **large-deflection and post-buckling behaviour** of the strip.

### Numerical Workflow

```text
Strip geometry & material properties
              ↓
      Nonlinear elastica
              ↓
       Boundary conditions
              ↓
       BVP formulation
              ↓
       scipy.solve_bvp
              ↓
     Strip deformation shape
              ↓
      Energy estimation
              ↓
       Jumping performance
```

---

## Large-Deflection Behaviour

A conventional sine-based approximation was compared against the nonlinear elastica solution.

For the large-deflection regime relevant to the jumping mechanism, the nonlinear model captured the post-buckling behaviour with **32% higher accuracy** than the conventional sine approximation.

This highlighted the importance of accounting for geometric nonlinearities when modeling the energy storage mechanism.

---

## Multi-Strip Scaling

The project also investigated how the jumping mechanism behaves when multiple strips are used.

While increasing the number of strips increases the available energy-storage capacity, the resulting system does **not scale linearly**.

Experiments showed an efficiency reduction from approximately:

**96% → 52%**

when the strip count was doubled.

This efficiency collapse provided insight into the mechanical losses and scaling limitations associated with combining multiple flexible energy-storage elements.

---

## Experimental Setup

The project involved:

* Fabrication of polycarbonate strip-based mechanisms
* Characterization of strip deformation
* Measurement of jumping height
* Comparison of experimental and numerical behaviour
* Investigation of different strip configurations

The experimental results were used to validate the nonlinear mechanical model and study the scaling behaviour of the jumping mechanism.

---

## Tools & Technologies

**Programming & Numerical Analysis**

* Python
* NumPy
* SciPy
* `scipy.solve_bvp`

**Mechanics**

* Nonlinear elastica
* Large-deflection beam mechanics
* Post-buckling analysis
* Elastic energy storage
* Energy conversion

**Hardware / Fabrication**

* Polycarbonate strips
* Mechanical prototyping
* Robot fabrication
* Experimental characterization

---

## Project Highlights

*  Designed and fabricated a **1 m jumping robot**
*  Modeled flexible-strip deformation using **nonlinear elastica**
*  Solved the resulting BVP numerically using **Python & SciPy**
*  Quantified the limitations of conventional sine-based approximations
*  Investigated the **scaling behaviour of multiple energy-storage strips**
*  Connected numerical modeling with experimental robot performance

---

## Project Context

This project was completed as part of a research internship at the **Mechanics & Computation Lab, Indian Institute of Science**, under the guidance of **Prof. Ramsharan Rangranjan**.

The work explored the intersection of **robotics, compliant mechanisms, nonlinear mechanics, and computational modeling**, with a focus on using mechanical energy storage to generate rapid locomotion.
