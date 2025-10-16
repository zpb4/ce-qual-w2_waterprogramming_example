# CE-QUAL-W2 practical example for Shasta Reservoir
This repository houses the executables and data required to run the CE-QUAL-W2 hydrodynamics model (version 4.5) for a Shasta Reservoir test case. This README file provides a high-level overview of the contents of the repository, setting up the CE-QUAL-W2 model, 
running the model, and analyzing the output via raw output data and the W2 post-processor tool. This repository supports the conceptual discussion of the CE-QUAL-W2 model on the Waterprogramming Blog Post [here](https://waterprogramming.wpcomstaging.com/wp-admin/edit.php?post_type=post&author=247677274)

## Input data description
The code below supports the data processing, model fitting, generation, and plotting routines to support the aforementioned manuscript.
## Getting started
1) temp_precip_data-process.R: Processes raw GEFS forecast and observed MAT/MAP data for model fitting (30 min)
2) temp_precip_model-fit.R: Fits synthetic forecast model to meteorological data from step 1 (1 hour)
3) temp_precip_synthetic-gen.R: Generates specified number of syn-GEFS samples to be input into HEFS (FEWS) (1 hour per 100 samples)
4) temp_precip_fews_process.R: Arranges syn-GEFS samples to be processed by external CNRFC HEFS architecture
5) ens-process_syn-gefs.R: Processes syn-GEFS .csv files from CNRFC to be R compatible for analysis

#### Plotting routines

- main_plot.R: Main plotting script for manuscript figures
- plot_supp-inf.R: Plotting script for supporting information figures
- calc_ensemble_stats_top-10.R: Calculates cumulative ensemble statistics for top-10 inflow events
- calc_ensemble_stats_top-100.R: Calculates cumulative ensemble statistics for top-10 inflow events
- forecast_verification_functions.R: Helper functions for ensemble forecast verification and plotting
- EFO-results_process.R: Process and plot EFO results for SI
- EFO-results_process_pre-hc.R: Process and plot EFO pre-hindcast results
- plot_cumul_ensembles_hopper.R: Processing and plotting functions for cumulative ensemble forecast plots
- plot_ensembles_hopper.R: Processing and plotting function for ensemble forecast plots
- plot_rank_hist.R: Processing and plotting function for rank histogram verification
- plot_cumul_rank_hist.R: Processing and plotting function for cumulative rank histogram plot
- plot_spread-skill_hopper.R: Processing and plotting function for binned spread error diagrams
- plot_ecrps_hopper.R: Processing and plotting function for ensemble CRPS (eCRPS) verification plots
- plot_top-10-events_hopper.R: Processing and plotting script for 'Top-10' cumulative ensemble statistics
- plot-top-100-events_hopper.R: Processing and plotting script for 'Top-100' cumulative ensemble statistics

#### Contact
Zach Brodeur, zpb4@cornell.edu
