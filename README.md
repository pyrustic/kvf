[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PyPI package version](https://img.shields.io/pypi/v/kvf)](https://pypi.org/project/kvf)
[![Downloads](https://static.pepy.tech/badge/kvf)](https://pepy.tech/project/kvf)



<!-- Intro Text -->
# KvF
<b>The key-value file format with sections</b>

# Overview

A config file (`config.kvf`) with [sections](https://github.com/pyrustic/braq) encoded with the [Paradict](https://github.com/pyrustic/paradict) text format:
```
# this comment is part of the
# unnamed section

[section 1]
id = 42
name = 'alex'
books = (dict)
    sci-fi = (list)
        'book 1'
        'book 2'
    thriller = (list)
        'book 3'
```

Reading a config file:

```python
import kvf


MY_CONFIG = {"section 1": {"id": 42,
                           "name": "alex",
                           "books": {"sci-fi": ["book 1", 
                                                "book 2"],
                                     "thriller": ["book 3"]}}}


# read a config file
my_config = kvf.get_config("/path/to/config.kvf")
# my_config is a dictionary object.
# Each key-value item of the dict represents
# a section where the key is the header (string)
# and the value is the body (dictionary) 


# test
assert my_config["section 1"] == MY_CONFIG["section 1"]


# load the config from a file object
with open("path/to/config.kvf", "r", encoding="utf-8") as file:
    my_config = kvf.load(file)

    
# test
assert my_config["section 1"] == MY_CONFIG["section 1"]

```

Writing a config file:

```python
import kvf


MY_CONFIG = {"section 1": {"id": 42,
                           "name": "alex",
                           "books": {"sci-fi": ["book 1", 
                                                "book 2"],
                                     "thriller": ["book 3"]}}}


# write a config file
kvf.put_config(MY_CONFIG, "path/to/config.kvf")


# write config to a file object
with open("/path/to/config.kvf", "w", encoding="utf-8") as file:
    kvf.dump(MY_CONFIG, file)
```


# Testing and contributing
Feel free to **open an issue** to report a bug, suggest some changes, show some useful code snippets, or discuss anything related to this project. You can also directly email [me](https://pyrustic.github.io/#contact).

## Setup your development environment
Following are instructions to setup your development environment

```bash
# create and activate a virtual environment
python -m venv venv
source venv/bin/activate

# clone the project then change into its directory
git clone https://github.com/pyrustic/kvf.git
cd kvf

# install the package locally (editable mode)
pip install -e .

# run tests
python -m tests

# deactivate the virtual environment
deactivate
```

<p align="right"><a href="#readme">Back to top</a></p>

# Installation
**KvF** is **cross-platform**. It is built on [Ubuntu](https://ubuntu.com/download/desktop) and should work on **Python 3.5** or **newer**.

## Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate
```

## Install for the first time

```bash
pip install kvf
```

## Upgrade the package
```bash
pip install kvf --upgrade --upgrade-strategy eager
```

## Deactivate the virtual environment
```bash
deactivate
```

<p align="right"><a href="#readme">Back to top</a></p>

# About the author
Hello world, I'm Alex, a tech enthusiast ! Feel free to get in touch with [me](https://pyrustic.github.io/#contact) !

<br>
<br>
<br>

[Back to top](#readme)

