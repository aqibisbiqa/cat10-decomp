To reproduce minproject results, first build the `quizx` library via running the following from the root of the git repo:

    cd quizx
    cargo build --release

The data itself is generated using the `hidden_shift_stabrank_cat10` binary. This takes several parameters as input, including a random seed, and produces a single row of CSV data (in its own file) as output. The easiest way to run these is by using the shell scripts found in the [scripts](scripts) folder. You can do so by running these commands from the root:

    cd scripts
    ./hidden_shift_data_cat10.sh
    
These take a long time to run, and benefit from having many cores available.

Once the data is generated, open the `visualize.ipynb` notebook to produce visualizations and data summaries.

For more details on the $\left|\text{cat}_{10}\right\rangle$ decomposition implementation, see `quizx/src/decompose.rs`.