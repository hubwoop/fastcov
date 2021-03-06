# ⚡ fastcov

For when you just need a coverage plot.

Feature requests welcome!

![lhzFrLVRbC](https://user-images.githubusercontent.com/23377960/97777205-f1157580-1b6e-11eb-9dd1-908580c52b92.gif)

## Quick start
```
fastcov.py my_alignment.bam another_alignment.bam
```

generates a coverage plot called `fastcov_output.pdf`

## Dependencies
makes use of
* `numpy`
* `pandas`
* `pysam`
* `seaborn`

## Full usage
```
usage: fastcov.py [-h] [-p POSITION] [-l] [-o OUTPUT_FILE] [-c CSV_OUT]
                  bamfile [bamfile ...]

Plot the coverage based on some bam files.

positional arguments:
  bamfile               Alignment files to include in the coverage plot.

optional arguments:
  -h, --help            show this help message and exit
  -p POSITION, --position POSITION
                        Specify a genomic position to plot exclusively.
                        Format: <ref_name>[:<start>-<stop>] Coordinates are
                        1-based and inclusive. Start and/or stop are optional
                        with fallbacks 1 and <length_of_ref> respectively
                        (e.g. 'chr1', 'chr1:-400' and 'chr1:4000-' are legal)
  -l, --logscale        Use logarithmic scale on y-axis.
  -o OUTPUT_FILE, --output_file OUTPUT_FILE
                        Specify plot output filename. File extension defines
                        the format (default: fastcov_output.pdf)
  -c CSV_OUT, --csv_out CSV_OUT
                        Specify csv data output filename. Will disable plot
                        output by default, specify --outfile to re-enable plot
                        output.
```
