**Title: Machine Learning-Based Power Prediction for RTL-Level MIPS Processor Design.**

**Project Overview**
This project presents a machine learning–based framework to predict power consumption at the RTL level for a MIPS processor. The approach leverages switching activity extracted from VCD files generated during RTL simulation and applies an ensemble ML model to achieve accurate early-stage power estimation without gate-level simulation.

**Motivation**
RTL is the earliest stage where architectural decisions strongly impact power.
Traditional power estimation methods are time-consuming and resource-intensive.
Early, accurate power prediction helps designers optimize power–performance–area trade-offs.

**Methodology**
**1.RTL Simulation & Data Generation**
A 32-bit MIPS processor was designed and simulated.
40 different instructions were applied.
VCD (Value Change Dump) files were generated from RTL simulations.
Switching activity was extracted for input and output signals using a VCD parser.

**2.Feature Generation**
Switching activity (number of signal transitions per cycle) was used as the main feature.
A dataset of 1880 samples was generated.
Each sample includes:
Switching activity of signals.

**3️.Automatic Signal Selection**
Signals with zero or negligible variance were removed.
Feature importance was evaluated using:
Gradient Boosting
Random Forest–based importance
Only power-dominant signals were retained to reduce redundancy.

**4.Machine Learning Model**
An ensemble model combining:
Gradient Boosting Regression (GBR)
Ridge Regression.

**Tools & Technologies**
RTL Design: Verilog
Simulation: Xilinx ISE
Power Data: VCD-based switching activity
Machine Learning: Python, Scikit-learn
Models: Gradient Boosting, Ridge Regression
Visualization: Matplotlib
