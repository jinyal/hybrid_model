# Interpretable hybrid deep learning model for reservoir inflow simulation
## Overview
This repository contains codes to build the hybrid model which decomposes inflow into precipitation-runoff and routing processes to simulate the reservoir inflow in the Missouri River Basin - Mainstem System Reservoirs, as described in the papers

Li, J., Dao, V., Hsu, K., Analui, B., Knofczynski, J. D., & Sorooshian, S. (2024). Improving cascade reservoir inflow forecasting and extracting insights by decomposing the physical process using a hybrid model. Journal of Hydrology, 630, 130623. https://doi.org/10.1016/j.jhydrol.2024.130623

If you have any questions or ideas regards to the code, feel free to contact Jinyang Li through email at: jinyal4@uci.edu

## Key designs
The meteorological information undergoes preprocessing via an LSTM (Long Short-Term Memory) network, wherein hidden states capture historical water information. Different lengths of hidden states are subsequently connected to a Routing and Precipitation-routing module to represent separate physical processes. The total inflow is the sum of these two parts.

![workflow](https://github.com/jinyal/hybrid_model/assets/59593913/dabb238f-e3ed-41b2-8efc-2eed41747a56)
