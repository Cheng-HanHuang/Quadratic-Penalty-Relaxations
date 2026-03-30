# Experiment tables for anonymous GitHub

This file collects the exact experiment results provided in the rebuttal draft, reformatted for direct inclusion in an anonymous GitHub repository.

## 1. Fixed-budget MIS: PGD vs Gurobi

- Problem: Maximum Independent Set (MIS)

- Graph family: Erdős–Rényi graphs

- Node sizes: n in {2000, 4000, 6000, 8000, 10000, 20000, 30000, 40000}

- Edge densities: p in {0.3, 0.5, 0.7}

- Number of instances per (n,p): 8

- Time budget per instance: 5 minutes

- Metric reported: average independent-set size returned within budget


| n | pgd_size_p0.3 | pgd_size_p0.5 | pgd_size_p0.7 | gurobi_size_p0.3 | gurobi_size_p0.5 | gurobi_size_p0.7 |
| --- | --- | --- | --- | --- | --- | --- |
| 2000 | 27 | 14.25 | 10 | 21.875 | 13.125 | 8.375 |
| 4000 | 28.5 | 16 | 10.5 | 20.5 | 11.625 | 7.375 |
| 6000 | 30.25 | 17.375 | 10.5 | 21.75 | 12.25 | 8 |
| 8000 | 30.875 | 17.375 | 10.75 | 23.25 | 13.25 | 7.75 |
| 10000 | 30.625 | 17 | 10.625 | 22.875 | 13.5 | 8.25 |
| 20000 | 32.5 | 17.875 | 11 | 24.5 | 14 | 8.625 |
| 30000 | 33.625 | 18.75 | 11.25 | 26.25 | 14.25 | 9.125 |
| 40000 | 34.125 | 18.875 | 11.625 | 26.75 | 15.125 | 9.625 |


### Long-form table

| n | p | time_budget_minutes | num_instances | pgd_avg_independent_set_size | gurobi_avg_independent_set_size | absolute_gap_pgd_minus_gurobi | relative_improvement_vs_gurobi_percent |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2000 | 0.3 | 5 | 8 | 27 | 21.875 | 5.125 | 23.428571 |
| 2000 | 0.5 | 5 | 8 | 14.25 | 13.125 | 1.125 | 8.571429 |
| 2000 | 0.7 | 5 | 8 | 10 | 8.375 | 1.625 | 19.402985 |
| 4000 | 0.3 | 5 | 8 | 28.5 | 20.5 | 8 | 39.02439 |
| 4000 | 0.5 | 5 | 8 | 16 | 11.625 | 4.375 | 37.634409 |
| 4000 | 0.7 | 5 | 8 | 10.5 | 7.375 | 3.125 | 42.372881 |
| 6000 | 0.3 | 5 | 8 | 30.25 | 21.75 | 8.5 | 39.08046 |
| 6000 | 0.5 | 5 | 8 | 17.375 | 12.25 | 5.125 | 41.836735 |
| 6000 | 0.7 | 5 | 8 | 10.5 | 8 | 2.5 | 31.25 |
| 8000 | 0.3 | 5 | 8 | 30.875 | 23.25 | 7.625 | 32.795699 |
| 8000 | 0.5 | 5 | 8 | 17.375 | 13.25 | 4.125 | 31.132075 |
| 8000 | 0.7 | 5 | 8 | 10.75 | 7.75 | 3 | 38.709677 |
| 10000 | 0.3 | 5 | 8 | 30.625 | 22.875 | 7.75 | 33.879781 |
| 10000 | 0.5 | 5 | 8 | 17 | 13.5 | 3.5 | 25.925926 |
| 10000 | 0.7 | 5 | 8 | 10.625 | 8.25 | 2.375 | 28.787879 |
| 20000 | 0.3 | 5 | 8 | 32.5 | 24.5 | 8 | 32.653061 |
| 20000 | 0.5 | 5 | 8 | 17.875 | 14 | 3.875 | 27.678571 |
| 20000 | 0.7 | 5 | 8 | 11 | 8.625 | 2.375 | 27.536232 |
| 30000 | 0.3 | 5 | 8 | 33.625 | 26.25 | 7.375 | 28.095238 |
| 30000 | 0.5 | 5 | 8 | 18.75 | 14.25 | 4.5 | 31.578947 |
| 30000 | 0.7 | 5 | 8 | 11.25 | 9.125 | 2.125 | 23.287671 |
| 40000 | 0.3 | 5 | 8 | 34.125 | 26.75 | 7.375 | 27.570093 |
| 40000 | 0.5 | 5 | 8 | 18.875 | 15.125 | 3.75 | 24.793388 |
| 40000 | 0.7 | 5 | 8 | 11.625 | 9.625 | 2 | 20.779221 |


## 2. ReduMIS preliminary time-to-first-solution results

- These runs are preliminary/incomplete.

- Metric reported: average time to first returned solution and average size of that first solution.


| graph_name | avg_init_time_sec | avg_init_size |
| --- | --- | --- |
| er_n10000_p0.30000 | 783.21825 | 32.25 |
| er_n10000_p0.50000 | 1625.062625 | 18.125 |
| er_n10000_p0.70000 | 1384.237625 | 11.125 |
| er_n20000_p0.30000 | 2510.655 | 34.125 |
| er_n20000_p0.50000 | 2407.15875 | 19 |
| er_n20000_p0.70000 | 2905.55 | 11.875 |
| er_n2000_p0.30000 | 309.00875 | 27.5 |
| er_n2000_p0.50000 | 327.44275 | 16.125 |
| er_n2000_p0.70000 | 368.753375 | 10.125 |
| er_n30000_p0.30000 | 3533.13125 | 35.125 |
| er_n30000_p0.50000 | 4333.006667 | 20 |
| er_n4000_p0.30000 | 346.8555 | 29.375 |
| er_n4000_p0.50000 | 608.526875 | 17 |
| er_n4000_p0.70000 | 820.27375 | 11 |
| er_n6000_p0.30000 | 474.93525 | 30.25 |
| er_n6000_p0.50000 | 994.785375 | 17.375 |
| er_n6000_p0.70000 | 1258.280875 | 11 |
| er_n8000_p0.30000 | 830.066125 | 31 |
| er_n8000_p0.50000 | 1578.481 | 18 |
| er_n8000_p0.70000 | 1302.88375 | 11.125 |


## 3. Open-pit mining: ancestor vs parent formulation

- Instances: newman1 and kd

- Each mode was run 200 times per instance.

- Full result table:


| instance | mode | runs | converged_kkt_rate | strict_binary_rate | strict_feasible_rate | strict_binary_feasible_rate | old_binary_rate | old_feasible_rate | old_binary_feasible_rate | mean_steps | median_steps | min_steps | max_steps | mean_time_sec | median_time_sec | min_time_sec | max_time_sec |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| newman1 | ancestor | 200 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1092.165 | 1091 | 693 | 1557 | 0.988636 | 0.97643 | 0.560832 | 1.884777 |
| newman1 | parent | 200 | 1 | 0.325 | 0 | 0 | 0.33 | 0 | 0 | 1018.605 | 967 | 477 | 1846 | 0.747483 | 0.712712 | 0.340681 | 2.177611 |
| kd | ancestor | 200 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 537.72 | 534 | 498 | 632 | 0.968356 | 0.959496 | 0.879048 | 1.833711 |
| kd | parent | 200 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 517.77 | 516 | 462 | 644 | 0.443613 | 0.434604 | 0.377893 | 0.797381 |


### Runtime-focused summary

| instance | ancestor_mean_time_sec | parent_mean_time_sec | absolute_overhead_sec | relative_slowdown_x | ancestor_strict_binary_feasible_rate | parent_strict_binary_feasible_rate |
| --- | --- | --- | --- | --- | --- | --- |
| newman1 | 0.988636 | 0.747483 | 0.241153 | 1.32262 | 1 | 0 |
| kd | 0.968356 | 0.443613 | 0.524743 | 2.182883 | 1 | 1 |


## Files included

- `mis_pgd_vs_gurobi_5min_wide.csv`

- `mis_pgd_vs_gurobi_5min_long.csv`

- `redumis_time_to_first_solution_preliminary.csv`

- `openpit_parent_vs_ancestor_full_results.csv`

- `openpit_runtime_summary.csv`
