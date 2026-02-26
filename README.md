<p align="center">
  <img src="logo.png" alt="datadocket logo" width="100%"/>
</p>

# datadocket

A simple data loading and saving utility library for Python without bloat, no pandas, no numpy, no bs. Just vanilla Python.

## Installation

Install from the root of the repository:

```bash
pip install datadocket
```

## Usage

This is a function-based library. In an unconventional and controversial move, I've decided to name the functions with an upper case initial
so it looks better. I know upper cases are supposed to be for classes... I don't care.

```python
import datadocket as dd

data = dd.load.Csv('file.csv')
dd.save.Csv('out.csv', data)
```

## Available modules:
- `dd.load`: Loading functions for txt, json, csv
  - `Json`: Load JSON data from a file
  - `Txt`: Load text content from a file (with optional line splitting)
  - `Csv`: Load CSV data as a list of rows
- `dd.save`: Saving functions for txt, json, csv
  - `Json`: Save data to JSON file (supports append mode for arrays)
  - `Txt`: Save text data to a file
  - `Csv`: Save list of rows to CSV file
- `dd.utils`: Utility functions
  - `Size`: Get file or directory size in bytes
  - `Delete`: Delete a file or directory
  - `Rename`: Rename a file or directory
  - `Move`: Move a file or directory to another location
  - `List`: List all files in a directory
  - `Empty`: Delete all files in a directory
  - `Copy`: Copy a file or directory
  - `MakeDir`: Create a directory
  - `Exists`: Check if a file or directory exists
- `dd.zip`: Zip file utilities
  - `Zip`: Compress a file into a .zip archive
  - `Unzip`: Decompress a .zip archive


## Run tests

To run the built-in tests, first install your local version of `datadocket` (including any local changes you've made) into your current Python environment by running:

```bash
pip install -e .
```

This command should be run from the root of the repository. The `-e` flag installs the package in "editable" mode, so changes to the source code are immediately reflected without needing a reinstall.

Then, use the following command from the root of the repository:

```bash
python -m tests.test
```

This will execute a suite of quick round-trip tests for TXT, JSON, CSV, and SQL file loading and saving, as well as basic file utilities.
All test outputs will be printed to the console.