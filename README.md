# Travelling Tournament Problem using MetaHeuristics 

This project shows an *Enhanced Heuristic approach* of **Grey Wolf Optimizer(GWO)** and **Enhanced Simulated Annealing(ESA)** in order to find optimum solution for **Travelling Tournament Problem(TTP)**. In this project, I tackle the mirrored version of TTP. I use Prey Proximity Model of Grey Wolf Algorithm to find the best permutation to feed to a Fast Modified Constructive Heuristic algorithm to generate tournament schedules. I integrate an Enhanced Heuristic approach of Simulated Annealing to obtain least Cost Tournament Schedule. I upgrade the population updating step of GWO by using Probabilistic methods and hybridize it with SA to solve TTP and avoid getting stuck in local minima. This proposed hybrid algorithm converges to an _optimum solution for TTP_.


## Code Organization

Within the download you'll find the following directories and files. You'll see something like this:

```
src/
├── enhanced_simulated_annealing/
│   ├── cost_objective_function.R
│   ├── enhance_schedule_using_SA.R
│   ├── partial_swap_rounds.R
│   ├── swap_homes.R
│   ├── swap_rounds.R
│   └── swap_teams.R
├── grey_wolf_optimizer/
│   ├── cost_of_tournament.R
│   ├── get_best_permutation.R
│   └── get_random_population.R
└── modified_constructive_heuristics/
    ├── assign_stadiums.R
    ├── assign_teams.R
    ├── assign_teams_in_schedule.R
    ├── construct_consecutive_matrix.R
    ├── construct_tournament_schedule.R
    ├── create_SRR.R
    └── number_of_violations.R
```

**data** module contains *Distance Matrix* for different tournaments and number of teams.


## Running the Project

```
$ git clone https://github.com/chandanand/travelling-tournament-problem.git
$ R
> setwd('project_directory/src')
> source('main.R')
> Main('data_file_name')
```

## Results Achieved

| Instances | GWO/ESA | MBBO/ESA | ACO | PSO | BBO/SA |
| :---: | :---: | :---: | :---: | :---: | :---: |
| NL8 | 39721 | 39721 | 44112 | 43805 | 42568 |
| NL10 | 58190 | 58769 | 67264 | 66331 | 66121 |
| NL12 | 110519 | 111064 | 121981 | 121070 | 120040 |
| NL14 | 182996 | 183631 | 208086 | 210132 | 207848 |
| NL16 | 253957 | 254242 | 290188 | 291394 | 281963 |

*Disclosure: Results may vary on every run and depending upon parameters*


## Creators

**Chand Anand**

* <https://twitter.com/chandanand>
* <https://github.com/chandanand>

## References

[Enhanced Heuristic Approach for Traveling Tournament Problem based on Grey Wolf Optimizer](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=7346685&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D7346685), 8th IEEE International Conference on Contemporary Computing, 2015. Daya Gupta, Chand Anand, Tejas Dewan.


## Copyright and license

Code released under [the MIT license](https://github.com/chandanand/ttp_with_gwo/blob/master/LICENSE).
