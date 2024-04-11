# Commands in TACC

## `maze`

### evaluating `bc`

```
sbatch -J eval_maze_bc -o eval_maze_bc.o -e eval_maze_bc.e -p gpu-a100-small -N 1 -t 24:00:00 --wrap "python llm_rl_scripts/maze/bc/eval_bc.py PARAMS /work/09720/yhpark/rl-llm-bench-dataset/maze/checkpoints/fully_observed/bc --outputs_path ."
```

You can evaluate `partially observed` setting through changing `fully_observed` in the command to `partially_observed`.

### evaluating `mc return`

```
sbatch -J eval_maze_mc -o eval_maze_mc.o -e eval_maze_mc.e -p gpu-a100 -N 1 -t 24:00:00 --wrap "python llm_rl_scripts/maze/mc_returns/eval_mc.py PARAMS /work/09720/yhpark/rl-llm-bench-dataset/maze/checkpoints/fully_observed/mc --outputs_path ."
```

