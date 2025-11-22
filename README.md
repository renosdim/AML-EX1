# Social Shortfall and Ecological Overshoot

This notebook explores **social shortfall** and **ecological overshoot** across different groups and years.  
It is structured into several key code cells, each with a distinct purpose.

---

## **Code Cell 1**

- Defines **indices** that are used throughout the notebook for mapping values to labels or linking indicators to files.  

- Provides **data filtering and gathering functions**, ensuring that all indicator values are properly processed even if presented in inconsistent formats.  

- Includes a **function for rounding float-type variables** for consistent presentation.  

- Contains a **core function** that, based on the `domain` parameter (ecological or social), builds the relevant data table for analysis.

---

## **Code Cell 2**

- Implements a **function to acquire country cluster data**, dividing countries into **bottom-40**, **middle-40**, and **top-20** groups.  

- Builds a **Trellis Plot**, computing ecological overshoot for each group for the only available year (2017) using the formula:  

$$
O = \frac{Y_t - Y_g}{Y_g}
$$

where:  

- $Y_t$ = overshoot value for the group  
- $Y_g = g \cdot Y_w$, with $g$ as the group weight (0.4 for middle and bottom groups, 0.2 for top group) and $Y_w$ as the world value for that indicator  

- For social shortfall, a **helper function** acquires the years where data is available accross all indicators.The first year in that list is used. Values for each group represent the respective shortfall, with **inversion and normalization adjustments** applied.

---

## **Code Cell 3**

- Contains a **function to acquire social shortfall or ecological overshoot** for the start and end years.  

- Builds the **Sandwich Plot**, where:  

  - **Light red bars** indicate overshoot or shortfall at the start year  
  - **Dark red bars** indicate overshoot or shortfall at the end year  

This visual clearly shows changes over time for each indicator.

---

## **Code Cell 4**

- Defines a **function to build a doughnut plot**, utilizing the same processed data from the Sandwich Plot.  

- Provides a **compact, intuitive visualization** of overshoot or shortfall distribution across indicators.

---

