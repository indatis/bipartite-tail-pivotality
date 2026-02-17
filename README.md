# Quota-Based Pivotality in Random Bipartite Networks

This repository contains the simulation framework used in:

Quota-Based Centrality under Heavy-Tailed Weight Regimes Brian Daniel
Bernhardt (2026)

The notebook reproduces all simulation results for:

-   Single-node pivotality (P1)
-   Pair pivotality (P2)
-   Light-tailed vs heavy-tailed weight regimes
-   Exposure amplification across bipartite ratios

# 1. Installation

Clone the repository:

git clone
https://github.com/YOUR_USERNAME/quota-pivotality-simulations.git cd
quota-pivotality-simulations

Install requirements:

pip install -r requirements.txt

# 2. Running the Simulation

Open the notebook:

jupyter notebook pivotality_simulations.ipynb

All parameters are defined at the top of the notebook:

theta = 0.7 target_d = 20 R = 100 distributions = [“gaussian”,
“student_t”, “power_law”]

To run all simulations: - Execute all cells in order. - Output figures
and GIFs will be saved in:

simulation_outputs/

# 3. Simulation Structure

The framework evaluates:

-   Fixed expected degree d*
-   Varying bipartite dimensions (M, N)
-   Three weight regimes:
    -   Truncated Gaussian
    -   Student-t (df=3)
    -   Pareto (power-law)

Graph-level statistics computed:

-   max P1
-   frac(P1 = 0)
-   Gini(P1)
-   max P2
-   frac(P2 = 0)
-   Conditional concentration metrics

# 4. Reproducibility

All simulations use seeded randomness via:

numpy.random.SeedSequence

Changing the seed will generate different random realizations.

5. Notes

-   Results in the paper correspond to R = 100 replications.
-   GIFs show structural transition across bipartite ratios.
-   No empirical data is used; simulations are fully synthetic.
