# Optimization of Coffee Extraction Parameters Sequentially Using Optuna

This code implements a sequential process for optimizing coffee extraction parameters using [Optuna](https://www.preferred.jp/ja/projects/optuna/).

The parameters being optimized include the dose of coffee (DOSE), grind size (Grinder Size), water temperature (Water Temperature), and pouring water amount (Pouring Water Amount).Each parameter is defined using `FloatDistribution` or `IntDistribution`, and Optuna's `ask()` function is used to generate parameters sequentially.

After testing the generated parameters, the resulting score (objective value) is passed to Optuna using the `tell()` function, which then influences the next parameter search. Manually selected parameters can also be added to the optimization process using `add_trial()`.

Finally, `plot_optimization_history()` and `plot_parallel_coordinate()` are used to visually represent the optimization progress and the relationships between the parameters.
