# Extract GPIT system suppliers from Appointments in General Practice data

This script extracts a mapping of GP codes to their main GP IT system from the Appointments in General Practice data.

## Prerequisites

The prerequisites are specified in the `.tool-versions` file.

- Python 3.14
- uv

## Setup

```bash
uv sync
```

This will install the dependencies specified in the `pyproject.toml` file.

## Running

```bash
uv run bin/download_gpad.py --month 2025-01
```

The code does the following:

- Downloads the Appointments in General Practice data for a given month
- Unzips the data
- Processes the data to create a mapping of GP codes to their main GP IT system
- Writes the mapping to a CSV file

The output file will be written to `data/gp_suppliers.csv` and is checked into the repository so updates to the data are visible over time.
