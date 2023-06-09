# memoirs
> Because _built in Rust_ must mean it's blazingly fast... right?

---

## Description

Rust that compiles into a Python package that offers simple in-*memoir*y caching...
or is it more like *memoir*ization? 🤔 (Okay, I'll stop.)

```python
import memoirs

@memoirs.Cache
def my_fancy_func(*args) -> str:
    print('running') 
    return ' '.join(str(a) for a in args)

```

Once a function return is memoized, subsequent invocations return a cached result without running the function again.

```python

>>> my_fancy_func('Hello', 'World!') 
running
'Hello World!'

>>> my_fancy_func('Hello', 'World!') 
'Hello World!'

```

For something more interesting (well, if you like basic arithmetic), take a look at [this example](https://github.com/rdghosal/memoirs/tree/master/examples/test.ipynb).

---

## Installation

To play around with it (please don't use this in prod):

### 1. Set up a virtual environment and install [`maturin`](https://github.com/PyO3/maturin)

```bash
$ python -m venv .venv
$ source .venv/bin/activate
$ pip install maturin

```

### 2. Install a dev version of the package into your virtual environment

```bash
$ maturin develop

```

There. Good to go.

---

## But, how?

This project is made possible by `pyo3`. [Check 'em out!](https://github.com/PyO3)!

