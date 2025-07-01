# datadocket

A simple data loading and saving utility library for Python.

## Installation

Install from the root of the repository:

```bash
pip install .
```

## Usage

```python
import datadocket as dd

data = dd.load.load_csv('file.csv')
dd.save.save_csv('out.csv', data)
```

Available modules:
- `dd.load`: Loading functions for txt, json, csv
- `dd.save`: Saving functions for txt, json, csv
- `dd.utils`: Utility functions
- `dd.zip`: Zip file utilities
