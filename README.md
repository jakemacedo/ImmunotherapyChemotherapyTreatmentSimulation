# Immunotherapy Chemotherapy Treatment Simulation
This script utilizes the chaotic cancer model presented in [Itik and Banks, 2010](https://doi.org/10.1142/S0218127410025417) and expanded upon in [Valle et al., 2018](https://doi.org/10.1155/2018/9787015) in order to simulate cancer dynamics and plot the system dynamics under different assumptions. This is done by altering the value of the variable a12 which is the fractional tumor cells killed by healthy cells and is affected by the competiton for nutrients between healthy cells and tumor cells: 
- When a12 = 1 a strange attractor appears which is related to the chaotic nature of cancer growth (Figure 1B). This chaotic nature is also demonstrated by plotting two trajectories with slightly different starting states which result in two very different outcomes (Figure 1A).
- When a12 < 1 the system exists as a limit cycle or periodic orbit (Figures 1C-D).
- When a12 > 1 the system collapses onto a single equilibrium point which is related to the complete eradication of tumor cells in a population(Figures 1E-F).

The main situations of concern would be in the cases where a12 >= 1 because it is in these states that the tumor cell population could potentially reach its carrying capacity, especially in the case where a12 = 1. If this were to occur, then the cancer would metastasize in search of more nutrients which would likely cause the death of the cancer patient. To prevent this, several different treatmennt options are available and the ones in the second half of this project examines the affects of immunotherapy and chemotherapy and their viability. To accomplish this simulation, modifications were made to the original ODEs present in the chaotic cancer model.

## Immunotherapy Simulation
There are several approaches to immune effector cell therapy, but regardless of the method used the goal of each is to cause an increase in the amount of effector cells present in the system. For this simulation, it is assumed that this change occurs instantaneously instead of as a gradual change. To accomplish this change a value q was added at time = 1000 to the differential equation associated with the population of immune effector cells, emulating a sudden influx of effector cells. This is repeated for both a12 = 1 as well as a12 < 1, but was not done with a12 > 1 since that patient would already be cured of cancer. It can be seen from Figures 2A-D that this treatment for a chaotic cancer system causes the system to collapse onto a single equilibrium point where any tumor cells present are eradicated. The same can not be said for the cancer system described by a limit cycle as through Figures 3A-D it can be seen that while the simulated immunotherapy treatment does collapse the system to a single equilibrium point, this point has a nonzero cancer cell value. Essentially, through this simulation it is demonstrated that immunotherapy in this situation would only put the cancer into remission, not eliminate it completely.

## Chemotherapy Simulation

## References

M. Itik and S. P. Banks, “Chaos in a three-dimensional cancer model,” International Journal of Bifurcation and Chaos, vol. 20, no. 1, pp. 71–79, 2010 https://doi.org/10.1142/S0218127410025417


Valle, Paul A., et al. “Bounding the Dynamics of a Chaotic-Cancer Mathematical Model.” Mathematical Problems in Engineering, vol. 2018, 2018, pp. 1–14., https://doi.org/10.1155/2018/9787015. 
