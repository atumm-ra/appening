# Appening - Your favorite DIY desktop app creator!

[![image](https://github.com/giswqs/pypackage/workflows/build/badge.svg)](https://github.com/giswqs/pypackage/actions?query=workflow%3Abuild)
[![image](https://github.com/giswqs/pypackage/workflows/docs/badge.svg)](https://giswqs.github.io/pypackage)

In a nutshell this creates the source code for a python app that can be installed on any linux flavor

Supported platforms:
[x] Linux

## Requirements
1. python3.9
2. make
3. PDM
```bash
pip install -U pdm
```
## Features

- PDM managed
- Uses PySide6 for rendering
- Self-contained cookiejar


## Quickstart

#### Using Cruft

    pip install -U cruft

Generate an app package project:

    cruft create git@github.com:atumm-ra/appening.git

### Using Cookiecutter

Install the latest Cookiecutter if you haven't installed it yet (this
requires Cookiecutter 1.4.0 or higher):

    pip install -U cookiecutter

Generate a Python package project:

    cookiecutter gh:atumm-ra/appening

Now after following the interactive console, you'll end up with a project that uses PySide6 to embed the web application you want

### Running the produced desktop application

- to be written....


