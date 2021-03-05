This folder contains code that solves models from the paper of Bayer and Luetikke, "Solving heterogeneous agent models in discrete time with many idiosyncratic states by perturbation methods" found at:

https://cepr.org/active/publications/discussion_papers/dp.php?dpno=13071#

The paper solves three models, represented here in three places:

A Krusell-Smith model with a single asset:
	* [OneAsset-KS]
		* in Assets/One execute SteadyStateOneAssetIOUs.py then FluctuationsOneAssetIOUs.py

A HANK model with a single asset:
    * [OneAsset-HANK]
	    * in Assets/One execute SteadyStateOneAssetIOUsBond.py then FluctuationsOneAssetIOUs.py

A HANK model with a liquid and an illiquid asset, [TwoAsset-HANK]
    * [TwoAsset-HANK]
	    * in Assets/Two execute SteadyStateTwoAsset.py then FluctuationsTwoAsset.py
	
Other content:

1) BayerLuetticke_wrapper.py creates a wrapper to the one asset version of BayerLuettike's code. 

This file:
   * Creates BayerLuettickeAgent and BayerLuettickeEconomy which are simple wrappers to BayerLuetikke's code, presently only the steady state part of this.
   * Simulates a BayerLuettickeEconomy with 10,000 agents in steady state

2) ConsIndShockModel_extension.py extends ConsIndShockModel to calculate and store a histogram of the distribution of agents.

The BayerLuettike code can also be run directly to recover impulse response functions to aggregate shocks.

The direct (non-notebook) code for which is found in the folder BayerLuetticke_code/TwoAssetCode

To run this code run the two files in order:

1) SteadyStateTwoAsset.py - solves the steady state
2) FluctuationsTwoAsset.py - solves the aggregate shocks and plots impulse response functions


