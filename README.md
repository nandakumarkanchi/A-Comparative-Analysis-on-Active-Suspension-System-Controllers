# 🚗 Comparative Analysis of Active Suspension System Controllers

> **PID · LQR · Fuzzy Logic Control for Quarter-Car Active Suspension Systems**
> *MATLAB/Simulink · Vehicle Dynamics · Control Systems · Research Repository*

---

## 📌 Overview

This repository accompanies the research paper:

> **“A Comparative Analysis and Evaluating Active Suspension System Controllers with CoppeliaSim”**
> Published in **IEEE**
> 🔗 [https://ieeexplore.ieee.org/abstract/document/10668918](https://ieeexplore.ieee.org/abstract/document/10668918)

The work presents a **comparative evaluation of active suspension (AS) controllers**—namely **PID**, **Linear Quadratic Regulator (LQR)**, and **Fuzzy Logic Controller (FLC)**—using a **quarter-car suspension model** developed in **MATLAB Simulink** and visualized through **CoppeliaSim**.

The study focuses on two key performance metrics:

* **Car Body Displacement (CBD)**
* **Stabilization Time (st)**

and benchmarks them against a **Passive Suspension (PS)** system.

---

## 🎯 Key Contributions

* Mathematical modelling of **passive and active quarter-car suspension systems**
* Implementation of **multiple PID control strategies** for active suspension
* Design and evaluation of an **optimal LQR controller**
* Rule-based **Fuzzy Logic Controller (Mamdani type)** for suspension control
* Comparative analysis using **CBD and suspension travel** as performance indices
* Integration with **CoppeliaSim** for dynamic visualization and validation

---

## 📂 Repository Structure

```
├── Models/
│   ├── Passive_suspension_model.slx
│   │
│   ├── PID_Controller_Based/
│   │   ├── Active_Suspension_PID_method_1.slx
│   │   ├── Active_Suspension_PID_method_2.slx
│   │   └── Active_Suspension_PID_method_3.slx
│   │
│   ├── LOR_Controller_Based/
│   │   └── Active_Suspension_LQR.slx
│   │
│   └── Fuzzy_Logic_Controller_Based/
│       ├── Active suspension fuzzy rule.fis
│       └── Active_suspension_Fuzzy_logic.slx
│
├── figures/
│   ├── figure_1.png   # Suspension system methodology
│   └── figure_7.png   # Comparative simulation results
│
└── README.md
```

---

## 🏗️ Methodology

The suspension system is modelled using a **Single Degree of Freedom (SDOF) quarter-car model**, representing both **sprung and unsprung masses**, springs, dampers, and road excitation inputs.

### 📐 Suspension System Methodology

![Figure 1](figures/figure_1.png)

*Figure 1: Schematic representation of (a) Passive Suspension System and (b) Active Suspension System used for modelling and simulation.*

* **Passive Suspension (PS):** Fixed spring–damper parameters, open-loop behavior
* **Active Suspension (AS):** Closed-loop control using external actuator force

The controllers generate actuator force based on system states to improve ride comfort and handling.

---

## ⚙️ Controller Implementations

### 🔹 PID Controller-Based Models

Three different PID implementations are explored:

* **Method 1:** Real-time car body displacement feedback
* **Method 2:** Real-time suspension travel feedback
* **Method 3:** Dual PID controller configuration

These approaches highlight how tuning and structural variations influence system response.

---

### 🔹 LQR Controller-Based Model

The **Linear Quadratic Regulator (LQR)** is designed using a state-space formulation and optimal control theory. Weighting matrices **Q** and **R** are selected to balance ride comfort and control effort.

This method achieves **faster stabilization**, making it suitable for performance-critical scenarios.

---

### 🔹 Fuzzy Logic Controller-Based Model

The **Fuzzy Logic Controller (FLC)** uses:

* Two inputs: displacement error and rate of change of displacement error
* One output: actuator force
* **Mamdani rule base with 25 rules**, defined in the `.fis` file

This approach mimics human decision-making and offers strong robustness against nonlinearities.

---

## 📊 Results and Discussion

### 📈 Comparative Performance Analysis

![Figure 7](figures/figure_7.png)

*Figure 2: Resultant car body displacement (CBD) and suspension travel of (a) Passive Suspension, and Active Suspension systems using (b) LQR, (c) Fuzzy Logic, and (d) PID controllers.*

### Key Observations

* **LQR Controller:** Fastest stabilization time
* **PID Controller:** Lowest maximum CBD (~0.08 m), best for ride comfort
* **Fuzzy Logic Controller:** Balanced performance with reduced peak displacement

The results highlight a **trade-off between stabilization time and displacement minimization**, emphasizing that controller selection depends on application priorities.

---

## 📜 Authors

* **Nandakumar R.**
  Symbiosis Institute of Technology, SIU, Pune
  📧 [nandakumarkanchi@gmail.com](mailto:nandakumarkanchi@gmail.com)

* **Ramesh B. T.**
  Symbiosis Institute of Technology, SIU, Pune
  📧 [rameshbt049@gmail.com](mailto:rameshbt049@gmail.com)

* **Javed K. Sayyad**
  Symbiosis Institute of Technology, SIU, Pune
  📧 [jksayyad23@gmail.com](mailto:jksayyad23@gmail.com)

* **Shubhadeep Biswas**
  Symbiosis Institute of Technology, SIU, Pune
  📧 [shubhadeep.biswas.btech2022@sitpune.edu.in](mailto:shubhadeep.biswas.btech2022@sitpune.edu.in)

---

## 📚 Citation

If you use this repository in your research, please cite the paper:

> N. R. Nandakumar, R. B. T. Ramesh, J. Sayyad, and S. Biswas,
> *A Comparative Analysis and Evaluating Active Suspension System Controllers with CoppeliaSim*, IEEE, 2024.
> [https://ieeexplore.ieee.org/abstract/document/10668918](https://ieeexplore.ieee.org/abstract/document/10668918)

---

## ⚠️ Notes

* This repository focuses on **modeling and simulation**, not embedded implementation
* Simulink models are intended for **academic and research use**
* Figures are reproduced from the published paper for explanatory purposes

---

## 🤝 Collaboration

Researchers and students interested in **vehicle dynamics, control systems, and simulation-based validation** are welcome to explore, fork, and extend this work.
