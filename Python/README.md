# causaldata

This Python package contains data sets that can be used to implement the code examples in causal inference textbooks.

As of the moment, this contains data sets from [The Effect](http://www.nickchk.com/causalitybook.html) by Huntington-Klein and  [Causal Inference: The Mixtape](https://mixtape.scunning.com/index.html) by Scott Cunningham are included in the package. The `judge_fe` data set from The Mixtape is too large to include, and so is omitted.

Data sets are stored as submodules. This package uses the same structure as, and imports code from, the **statsmodels.datasets** package, so the documentation on use [here](https://www.statsmodels.org/devel/datasets/index.html) applies to **causaldata**.

For example, to load and view documentation for the `black_politicians` data set:

Load as **numpy** array or **pandas** `DataFrame`:

```python
d_numpy = causaldata.black_politicians.load().data
d_pandas = causaldata.black_politicians.load_pandas().data
```

To view the descriptions of the variables, the description of the data overall, and the source:

```python
print(causaldata.black_politicians.NOTE)
print(causaldata.black_politicians.DESCRLONG)
print(causaldata.black_politicians.SOURCE)
```

To see a list of all included data sets, do `dir(causaldata)`

At some point I will figure out how to tell you to install this package from GitHub. But for now, [download this package](https://github.com/NickCH-K/causaldata/archive/refs/heads/main.zip), unzip it, change the directory to the `causaldata/Python` folder, and install with:

```python
python setup.py install
```

Or, if you're using something with IPython like Spyder, you might use

```python
runfile('the/full/path/to/causaldata/Python/setup.py', wdir='your/working/directory',args='install')
```