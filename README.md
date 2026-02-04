# COVID-19 Viral Spread & Epidemiological Visualization

This project implements a biological simulation that visualizes how a virus propagates through a population, utilizing mathematical distribution models and statistical disease progression logic.

---

## 💡 Motivation & Inspiration
This project was inspired by the visualization techniques often seen in viral growth simulations. I have adapted these concepts to include:

* **Inspired by Kite:** Foundational spread logic adapted for advanced visualization.
* **Vogel’s Phyllotaxis:** Implementing a sunflower-inspired spiral distribution for uniform population density.
* **Dual-Layer Animation:** A custom animation engine that handles both daily status updates and "one-by-one" infection wave rendering.
* **Granular Disease Logic:** Moving beyond a basic SIR model to include incubation periods and divergent recovery/fatality paths.



---

## 🔍 Why This Visualization?
By using a polar coordinate system and a phyllotaxis distribution, this simulation provides a unique look at "herd" dynamics:

1.  **Uniform Density:** 4,500 individuals are packed into a circular "petri dish," ensuring that the spread isn't skewed by random clustering.
2.  **Visual Clarity:** You can clearly see the "wave" of red (infected) moving through the grey (healthy) before leaving behind green (recovered) or black (deceased) markers.
3.  **Real-Time HUD:** A dynamic heads-up display tracks the day, current active cases, total recoveries, and total deaths.

---

## 🧠 Model & Logic
The system employs a **Probabilistic SIR (Susceptible-Infectious-Recovered)** architecture. The movement of the virus is governed by mathematical constants.



* **Transmission ($R_0$):** Set to 2.28, meaning every infected person statistically generates 2.28 new cases.
* **Spatial Distribution:** Dots are positioned using the Golden Angle formula:
    $$\theta = n \times 137.508^\circ$$
    $$r = c\sqrt{n}$$
* **Incubation & Recovery:** The model calculates a "serial interval" of 7 days between infection generations, with recovery windows ranging from 7 to 56 days depending on case severity.

---

## 📊 Visualizing Outcomes
Unlike a static graph, this simulation allows you to observe the **lag effect** in epidemiology:

* **The Infection Peak:** Watch how the number of active cases spikes after the first few serial intervals.
* **The Recovery Lag:** Notice how the green "recovered" dots only begin to appear significantly 12-14 days after the first red dots.
* **Mortality Rate:** A calibrated 3.4% fatality rate creates a sparse but visible scattering of black dots.

---

**Developed by:** Kiet Truong  
**Academic Affiliation:** University of Wisconsin–Madison
