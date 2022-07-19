# geocat_test_scripts

Each test_* script is a script to test functionality of the GeoCAT meteorology.py and crop.py GPU ported functions. 
The repository for the ported version of the scripts is: https://github.com/haniyeka/geocat-comp/tree/meteorology_and_crop_cupy 

Using CuPy each function is ported such way that by a new argument "use_gpu" which its default value is "False" we can choose whether we want to use GPU. 
With a "True" value, "CuPy" will be imported and the Numpy, Xarray, and Dask arrays will be converted to their CuPy type. 


- NumPy will directly converted to CuPy. 

- Xarray with a NumPy ndarray as its data will be converted to Xarray with a CuPy ndarray. 

- Xarray with a Dask+NumPy ndarray as its data will be converted to Xarray with a Dask+CuPy ndarray.
