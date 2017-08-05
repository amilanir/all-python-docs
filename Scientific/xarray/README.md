![Imgur](http://i.imgur.com/Jj5JINC.png)

# What is xarray?

* originally developed by employees (Stephan Hoyer, Alex Kleeman and Eugene Brevdo) at [The Climate Corporation](https://climate.com/)
* xarray extends some of the core functionality of the Pandas library:
    * operations over _named_ dimensions
    * selection by label instead of integer location
    * powerful _groupby_ functionality
    * database-like joins

# When to use xarray:

* if your data are multidimensional (e.g. climate data: x, y, z, time)
* if your data are structured on a regular grid
* if you can represent your data in netCDF format

# Basic xarray data structures:
* NetCDF forms the basis of the xarray data structure
* two main data structures are the `DataArray` and the `Dataset`

## `DataArray`
* the `DataArray` is xarray's implementation of a labeled, multi-dimensional array
* the `DataArray` has these key properties:
  * `data`: N-dimensional array (NumPy or dask) holding the array's values,
  * `dims`: dimension names for each axis,
  * `coords`: dictionary-like container of arrays that label each point, and
  * `attrs`: ordered dictionary holding metadata


## `Dataset`
* xarray's multi-dimensional equivalent of a Pandas `DataFrame`
* dict-like container of DataArray objects with aligned dimensions
* Datasets have these key properties:
  * `dims`: dictionary mapping from dimension names to the fixed length of each dimension,
  * `data_vars`: dict-like container of `DataArrays` corresponding to data variables,
  * `coords`: dictionary-like container of `DataArrays` intended to label points used in data_vars
  * `attrs`: ordered dictionary holding metadata
  
# Notebooks

- [Plotting](https://nbviewer.jupyter.org/github/andersy005/all-python-docs/blob/master/Scientific/xarray/04-plotting.ipynb)
