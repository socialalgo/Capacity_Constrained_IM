# Capacity Constrained IM

Environment: Windows/Linux with `c++17`, `cmake` and `OpenMP`.

## Compile and Run

#### Compile [using Linux bash]

```bash
cd exp
mkdir build && cd build
cmake ..
make
```

#### Run

```bash
./exp [dataset_name] k eps greedy_option
```

**dataset_name**: Name of the graph file in `/data/`;

**k**: Set the constant $k$.

**eps**: Set the parameter $\epsilon$ of solutions extending *OPIM-C*.

**greedy_option**: Specify the type of MC simulation-based solutions to execute. Possible values:

+ **0**: Do not execute these solutions.
+ **1** (default): Execute these solutions with CELF trick.
+ **2**: Execute these solutions with vanilla version.

#### Example

```bash
dnc-corecipient 10 0.05 1
```

Run the experiments on *DNC* dataset, with $k=10,\epsilon=0.05$, with the CELF greedy solutions.

## More Experiments

**exp_batch.cpp**: (default) Main experiment.

**exp_query_set.cpp**: Randomly generate one query set.

**exp_gamma.cpp**: Calculate the curvature for a graph and a query set.


#### Reference
```
@inproceedings{ccim,
  author       = {Shiqi Zhang and
                  Yiqian Huang and
                  Jiachen Sun and
                  Wenqing Lin and
                  Xiaokui Xiao and
                  Bo Tang},
  title        = {Capacity Constrained Influence Maximization in Social Networks},
  booktitle    = {Proceedings of the 29th {ACM} {SIGKDD} Conference on Knowledge Discovery
                  and Data Mining, {KDD} 2023, Long Beach, CA, USA, August 6-10, 2023},
  pages        = {3376--3385},
  publisher    = {{ACM}},
  year         = {2023}
}
```

