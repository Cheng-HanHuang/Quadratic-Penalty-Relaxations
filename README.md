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


## 2. ReduMIS preliminary time-to-first-solution results

| (n, p)         | avg_init_time_sec |
|----------------|------------------:|
| (2000, 0.3)    |        309.008750 |
| (2000, 0.5)    |        327.442750 |
| (2000, 0.7)    |        368.753375 |
| (4000, 0.3)    |        346.855500 |
| (4000, 0.5)    |        608.526875 |
| (4000, 0.7)    |        820.273750 |
| (6000, 0.3)    |        474.935250 |
| (6000, 0.5)    |        994.785375 |
| (6000, 0.7)    |       1258.280875 |
| (8000, 0.3)    |        830.066125 |
| (8000, 0.5)    |       1578.481000 |
| (8000, 0.7)    |       1302.883750 |
| (10000, 0.3)   |        783.218250 |
| (10000, 0.5)   |       1625.062625 |
| (10000, 0.7)   |       1384.237625 |
| (20000, 0.3)   |       2510.655000 |
| (20000, 0.5)   |       2407.158750 |
| (20000, 0.7)   |       2905.550000 |
| (30000, 0.3)   |       3533.131250 |
| (30000, 0.5)   |       4333.006667 |


## 3. Open-pit mining: ancestor vs parent formulation

- Instances: newman1 and kd

- Each mode was run 200 times per instance.

- Full result table:

| instance | mode | mean_steps | median_steps | min_steps | max_steps | mean_time_sec | median_time_sec | min_time_sec | max_time_sec |
| ---      | ---  |  ---         | ---          | ---       | ---       | ---           | ---             | ---          | ---          |
| newman1 | ancestor | 1092.165 | 1091 | 693 | 1557 | 0.988636 | 0.97643 | 0.560832 | 1.884777 |
| newman1 | parent | 1018.605 | 967 | 477 | 1846 | 0.747483 | 0.712712 | 0.340681 | 2.177611 |
| kd | ancestor | 537.72 | 534 | 498 | 632 | 0.968356 | 0.959496 | 0.879048 | 1.833711 |
| kd | parent | 517.77 | 516 | 462 | 644 | 0.443613 | 0.434604 | 0.377893 | 0.797381 |

- `redumis_time_to_first_solution_preliminary.csv`

- `openpit_parent_vs_ancestor_full_results.csv`

- `openpit_runtime_summary.csv`
