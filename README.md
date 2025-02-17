# Stockast [![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FRajdeepKonwar%2Fstockast.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FRajdeepKonwar%2Fstockast?ref=badge_shield)
## Stock Market Forecasting using Monte-Carlo Simulations

### Compile Instructions

#### Linux
```
make
```
Type `make clean` to clean object file and executable.

### Run Instructions

#### Linux
Set the number of threads to be used for computation,
```
export OMP_NUM_THREADS=number_of_threads
```
For example, `export OMP_NUM_THREADS=8`.
Then run the program
```
./stockast
```

### General info
* The input file "ml_data.csv" contains the stock-price values for 3 hours prior to run-time; this acts as the history-data and helps estimate the market volatility.
* The output file "opt.csv" contains the output (most likely outcome) price-vector from our code. One can use Excel or gnuplot to plot the resulting line graph of the predicted stock pricing.
* (**Linux only**) The script "profiling.sh" runs the parallel code from 1 to the specified number of threads. To use the script,
```
./profiling.sh "number_of_threads"
```
For example, `./profiling.sh 8`.
