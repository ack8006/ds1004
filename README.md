# ds1004

Code for NYC Taxi analysis.

## Deliverable 1

The main parts of the submission are the per-column analysis files and scripts
to generate plots in the report.

### Per-column analyzer

This is a Spark 1 job that loads the yellow taxis dataset and analyzes each
column value independently. The program takes a directory and reads files for
each month in the given years.

The script expects file names in a certain format:

``$inputdir/yellow_tripdata_$year-$month.csv``

For a given year, all months from January to December must be present. It then
dumps results to a directory in HDFS of your choosing:

``
taxis_test_results/DOLocationID.csv
taxis_test_results/PULocationID.csv
taxis_test_results/RatecodeID.csv
taxis_test_results/VendorID.csv
...
``

The easiest way to run the script is to call one of the starter shell scripts
``run_test.sh`` or ``run_real.sh``.
