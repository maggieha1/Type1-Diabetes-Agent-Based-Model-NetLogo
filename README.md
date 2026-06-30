# NetLogo Type 1 Diabetes (T1D) Simulation

This project is an extension of the standard blood glucose regulation model in NetLogo. It differentiates the pancreatic cells into Alpha and Beta cell populations to simulate the autoimmune pathophysiology of Type 1 Diabetes and provides tools for manual insulin management.

## Model Overview
The model simulates blood glucose homeostasis regulated by the liver and pancreas. The core extension adds:
- **Cell Differentiation:** Pancreatic cells are split into insulin-producing Beta cells (yellow) and glucagon-producing Alpha cells (red).
- **Autoimmune Destruction:** A progressive destruction of Beta cells (turning them black/inactive) based on a user-defined rate.
- **Manual Intervention:** A manual insulin injection system to counteract the loss of insulin regulation.

## How to Set Up the Interface
To ensure the simulation works correctly, please configure your NetLogo Interface tab with the following elements:

### 1. Sliders
* `beta-cell-destruction-rate`: Range 0 to 100. Controls the probability that an active Beta cell is destroyed during each tick.
* `insulin-injection-dose`: Range 10 to 500. Determines the amount of insulin added to the bloodstream when the "Inject Insulin" button is pressed.

### 2. Buttons
* **Inject Insulin**: Command `inject-insulin`. Spawns insulin molecules into the bloodstream to help sequester glucose.

## Key Procedures
The following procedures have been integrated into the code to manage the T1D logic:
* **`make-pancreas`**: Initializes the pancreas with a mix of Alpha and Beta cell breeds.
* **`autoimmune-attack`**: Simulates disease progression by turning active Beta cells black.
* **`adjust-hormones`**: Specialized logic where Alpha cells handle glucagon and surviving Beta cells handle insulin.
* **`inject-insulin`**: A manual user tool to spawn insulin molecules.

## Troubleshooting
If you encounter errors when checking the code:
1.  **Duplicate Procedures**: Ensure you have removed any older versions of `make-pancreas` or `adjust-hormones`.
2.  **Breed Definitions**: Ensure the `pancreatic-cells` breed is removed and replaced by `alpha-cells` and `beta-cells` definitions.
3.  **Variable Names**: Ensure slider names in the Interface tab exactly match `beta-cell-destruction-rate` and `insulin-injection-dose`.

## Credits
This simulation is based on the original blood glucose model by Uri Wilensky (2017).
