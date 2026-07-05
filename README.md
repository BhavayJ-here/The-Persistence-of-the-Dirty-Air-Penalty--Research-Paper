# The-Persistence-of-the-Dirty-Air-Penalty--Research-Paper
Causal Analysis of Formula 1's 2022 Ground Effect Regulations

# ABSTRACT
In the start of 2022, FIA mandated a redesign of Formula 1 cars around ground effect aerodynamics with the goal of reducing performance penalty that happens because of cars following closely behind each other, which is called “Dirty Air”.This claim shaped regulatory and competitive discourse in the sport but has not been directly tested against timing data at individual lap level, which could tell the real advantage over each other in the official race. We gathered over 100486 racing laps and constructed a dataset from season 2021 to 2025 (2026 race is ongoing) Using FastF1 API.We constructed a compound specific physics correction to isolate the Dirty Air from confounding effects of fuel load and tyre degradation.and tested for a change in dirty air penalty across 2022 regulation boundary using two independent methodologies, which are Ordinary Least Squares (OLS) regression with clustered standard errors and Causal Forest Double/Debiased Machine Learning (DML) to account for potential non linearity and effect heterogeneity. We also reestimated both models with season as categorical variable to find if there are any significant individual season effects differing from 2021 baseline OLS,applying a generalized circuit filter to ensure results were not skewed by calendar changes. Both methods came to the same result, which is when 2022 to 2025 period was treated as a single pooled block, we found no statistically significant reduction in Dirty Air lap time penalty (OLS interaction term β = −0.0025, p = 0.803; Causal Forest mean effects of 0.019 s and 0.018 s per second of following distance for 2021 and 2022–2025, respectively).We also tested a more specific alternative hypothesis inspired by externally reported aerodynamic simulation data suggesting that improvement was concentrated in 2022 and eroded in 2023 to 2025, Our reestimation of both models with season as categorical variable found no individual season effect differing significantly from 2021 baseline OLS, though Causal Forest estimates for several seasons are individually distinguishable from zero in a pattern that isn’t monotonic and does not match the erosion shape. We conclude that 2022 ground effect regulation did not produce a detectable reduction in Dirty Air lap time penalty in the observed racing data where we held both pooled and season level tests. By distinguishing between simulation based engineering claims and outcome based race data, we show that even if a theoretical aerodynamic benefit exists, it has not translated into a detectable performance gain in the real racetrack, where tyre strategy, driver behavior, and race context can swamp a genuine aerodynamic effect that exists in simulation.

# STUCTURE
phase4_data_collection.ipynb
master_dataset.csv
phase5_physics_corrections.ipynb
dirty_air_penalty_curves.ipynb
ols_regression_phase7.ipynb
causal_forest_phase8.ipynb
phase_8_5.ipynb

# DATA
master_dataset.csv - raw collected lap data from 2021–2025

physics_adjusted_dataset.csv - tyre/fuel-corrected lap times, used by all downstream analyses

# Required packages:
fastf1, pandas, numpy, scikit-learn, statsmodels, econml, matplotlib
