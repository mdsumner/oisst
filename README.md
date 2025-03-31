just trying to get  a useable example, I was missing the to float64 step ...



```
ds = virtualizarr.open_virtual_dataset(f[0], loadable_variables = None, drop_variables = ["zlev"])

ds = ds.assign_coords({"lat": numpy.float64(ds.lat.values)})
ds = ds.assign_coords({"lon": numpy.float64(ds.lon.values)})
ds.virtualize.to_kerchunk("oisst.json", format  = "json")
```
