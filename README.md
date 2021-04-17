# pre-commit-example

Example configuration of a java project with pre-commit-hooks

## Requirements

- `Python 3.6+`
- `pre-commit`
- `mdformat`

## Installation

1. Install all needed packages

   Using pip:

   ```
   python pip install pre-commit mdformat
   ```

   Using requirements.txt:

   ```
   python pip -r requirements.txt
   ```

1. Copy the `.pre-commit-config.yaml` to the root directory

1. Install the pre-commit hooks

   ```
   pre-commit install
   ```

1. (Optional) Run initialy against all files

   ```
   pre-commit run --all-files
   ```

## What it does

This config runs against following files:

- `.md` - pretty format
- `.ini` - pretty format
- `.java` - check against Google Codestyle
- `.json` - verify syntax and pretty format
- `.xml` - verify syntax
- `.toml` - verify Syntax
- `.yaml` - verify Syntax and sort

It also:

- detects private keys
- fixes the end of files (removes and adds newline)
- removes trailing whitespaces
- checks for files `>5` (ignores lfs files)
