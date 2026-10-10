# GFM Reconnection Transient Stability

MATLAB/Simulink models accompanying the research on transient stability of virtual synchronous generator (VSG)-based **single-loop voltage-magnitude (SLVM) controlled grid-forming (GFM) inverters** during islanded-to-grid reconnection.

## Research context

The study examines the reconnection transient associated with removing the auxiliary pre-synchronization frequency correction after the inverter has been synchronized and connected to the grid. Of particular interest are the internal VSG frequency-deviation state, active-power and current transients, and the role of voltage-magnitude dynamics in an SLVM-controlled inverter.

These files are provided to facilitate inspection of the Simulink implementation and independent reproduction of the modeled scenarios.

## Available Simulink models

| File | MATLAB/Simulink version indicated by the model |
| --- | --- |
| [VSG_SLVM_Reconnection_R2024a.mdl](VSG_SLVM_Reconnection_R2024a.mdl) | R2024a |
| [VSG_SLVM_Reconnection_R2018a.mdl](VSG_SLVM_Reconnection_R2018a.mdl) | R2018a |

Both files use the Simulink `.mdl` model format. The release labels identify the corresponding model versions; they do **not** imply compatibility with every other MATLAB release.

## How to open and run

1. Select **Code → Download ZIP** on GitHub and extract the repository, or clone it with Git.
2. Open MATLAB with the release corresponding to the model you intend to inspect.
3. Set the MATLAB current folder to the downloaded repository directory.
4. Open the relevant model, for example:

   ```matlab
   open_system('VSG_SLVM_Reconnection_R2024a.mdl')
   ```

   For the earlier model, use:

   ```matlab
   open_system('VSG_SLVM_Reconnection_R2018a.mdl')
   ```

5. Review the model configuration, initialization requirements, solver settings, and reconnection event settings before running the simulation. Resolve any missing toolbox, library, or workspace-variable dependencies reported by Simulink.
6. Run the model from the **Simulink Run** button and inspect the available scopes or logged signals.

To reproduce a particular case discussed in the manuscript, the power references, local load, network parameters, synchronization/withdrawal sequence, and controller settings must match that case.

## Reproducibility and compatibility notes

- The **switch-closing event** and the **withdrawal of the auxiliary synchronization correction** are distinct steps in the reconnection sequence. Their configuration should be checked separately.
- MATLAB/Simulink behavior can depend on the software release, installed toolboxes, solver settings, and model initialization.
- The presence of two model files does not by itself establish numerical equivalence between their outputs. Verify the results in the intended MATLAB release before making a cross-version comparison.
- Numerical results and claimed performance improvements should be interpreted together with the assumptions and parameter settings reported in the associated manuscript.

## Questions

For questions about opening the models, missing dependencies, or reproducing a specific simulation case, please use the repository's **Issues** section and include the MATLAB release, the model filename, and the relevant error message or simulation settings.
