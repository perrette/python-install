# python-install
Keep track of installation steps for common python packages under ubuntu, with a focus on geophysics.
Details are provided to solve problems arising from the use of pip (using virtualenv). Instruction for a given
package assume the previous packages have been installed. If you are only interested in one package, you may
look for a specific binary library in previous lines. Note that most packages are their setup.py file are under 
continuous development, so this document will most likely be useful for a short period of time only, under 
the system under consideration (Ubuntu)...

##Dependencies 

- virtualenv==1.11.4
- pip==6.1.1

##Specific Instructions

- __numpy__==1.9.4 : first install with pip might fail, `sudo apt-get install numpy` might be necessary to have the proper 
binaries installed. Subsequent install via virtualenv will work via pip.

- __matplotlib__==1.4.3
  - required binary : freetype 
  - `sudo apt-get install libfreetype6-dev`
  - `pip install matplotlib`
  
- __netCDF4__==1.1.7
  - required binaries : HDF5, NETCDF4
  - `sudo apt-get install libhdf5-serial-dev netcdf-bin libnetcdf-dev`
  - `pip install netCDF4`

- __cartopy__==0.12.0
  - required binaries : PROJ4, GDAL, GEOS
  - `sudo apt-get install libproj-dev libgdal-dev python-gdal libgeos-dev`
  - required python modules not handled with pip: PIL (shipped with Pillow), cython, scipy
  - `pip install cython Pillow scipy cartopy`
