# CDI Process Modeling (RC Circuit Approach)

This repository contains a dynamic simulation toolkit for **Capacitive Deionization (CDI)** water treatment processes. It uses an equivalent **RC Circuit Model** to simulate the electrosorption of ions over time.

## Objectives
* **Dynamic Modeling:** Solving coupled Differential Equations (ODEs) for Charge ($Q$) and Concentration ($C$).
* **Parameter Estimation:** Fitting experimental conductivity data to find:
  * Effective Resistance ($R_{eff}$)
  * Charge Efficiency ($\Lambda$)
* **Visualization:** Publication-quality plotting of Concentration vs. Time.

## Mathematical Model
The process is modeled as a capacitor in series with a resistor. The governing equations derived from mass and charge balance are:

1.  **Charge Balance (Ohm's Law):**
    $$\frac{dQ}{dt} = I = \frac{V_{applied} - V_{cap}}{R_{res}}$$

2.  **Mass Balance (Faraday's Law):**
    $$\frac{dC}{dt} = - \frac{I \times \Lambda}{F \times V_{tank}}$$

## Files Description
* `CDI_Modeling.ipynb`: The main Jupyter Notebook containing the ODE solver and curve fitting algorithms.
* `requirements.txt`: List of required Python libraries.

## How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
