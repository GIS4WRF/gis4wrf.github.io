The installation of GIS4WRF requires the **latest version** of **QGIS 3**. Make sure that you follow the same steps in the same order as described below to avoid problems.

!!! tip
    For best user-experience and easiest installation, install on Windows.

## Supported platforms
We currently support the following operating systems (OS) and versions:

| OS Name       | Version     | Code name                                 |
|---------------|------------ |-------------------------------------------|
|Windows        | 7, 8, 10    | n/a                                       |
|macOS          | 10.11 - .14 | El Capitan , Sierra , High Sierra, Mojave |
|Linux (Ubuntu) | 17.x, 18.x  | Artful, Bionic                            |

## Install QGIS

### Windows
Download the **latest version** of **QGIS Standalone Installer** from the [QGIS download page](https://www.qgis.org/en/site/forusers/download#windows) and install it using the guided installation. After you have successfully installed QGIS 3, go to [Install GIS4WRF](#install-gis4wrf).

### macOS

You need to have [Homebrew](https://brew.sh/) installed on your system. Then, simply copy, paste and execute the following in your Terminal prompt:

```bash
brew tap osgeo/osgeo4mac &&
brew install qgis3 && brew install qgis3 && # avoid issues with current formula
brew install gcc mpich python hdf5 netcdf &&
pip3 install --user f90nml pyyaml netCDF4 wrf-python
```

You can now launch QGIS 3 from your Terminal prompt with the `qgis3` command. To install GIS4WRF, go to [Install GIS4WRF](#install-gis4wrf).

### Ubuntu
The installation of QGIS on Ubuntu is slightly different depending on your version of Ubuntu. If you are running a version prior to Ubuntu 17.x, you must upgrade to the most recent version. If do not know what version of Ubuntu you are running, run `lsb_release -a | grep Release` in your Terminal prompt.

#### 17.x (Artful)

Copy, paste and execute the following in your Terminal prompt:

```bash
sudo apt-get install -y software-properties-common &&
wget -O - https://qgis.org/downloads/qgis-2017.gpg.key | gpg --import &&
gpg --fingerprint CAEB3DC3BDF7FB45 &&
gpg --export --armor CAEB3DC3BDF7FB45 | sudo apt-key add - &&
sudo add-apt-repository -s 'deb https://qgis.org/debian artful main' &&
sudo apt-get update &&
sudo apt-get install -y qgis python-qgis gfortran mpich &&
sudo apt-get install -y python3-pip &&
pip3 install --user f90nml pyyaml netCDF4 wrf-python
```

After you have successfully installed QGIS 3, go to [Install GIS4WRF](#install-gis4wrf).

#### 18.x (Bionic)

Copy, paste and execute the following in your Terminal prompt:

```bash
sudo apt-get install -y software-properties-common &&
wget -O - https://qgis.org/downloads/qgis-2017.gpg.key | gpg --import &&
gpg --fingerprint CAEB3DC3BDF7FB45 &&
gpg --export --armor CAEB3DC3BDF7FB45 | sudo apt-key add - &&
sudo add-apt-repository -s 'deb https://qgis.org/debian bionic main' &&
sudo apt-get update &&
sudo apt-get install -y qgis python-qgis gfortran mpich &&
sudo apt-get install -y python3-pip &&
pip3 install --user f90nml pyyaml netCDF4 wrf-python
```
After you have successfully installed QGIS 3, go to [Install GIS4WRF](#install-gis4wrf).

## Install GIS4WRF

The installation of GIS4WRF is straightforward and can be done directly in QGIS under the `Plugins` > `Manage and Install Plugins...` menu. If you want to know how to download pre-built binaries for WPS and WRF so that you can run simulations on Windows, macOS and Linux, see the [Configuration](../configuration) section. To learn how to use GIS4WRF see the [Documentation](../documentation/overview) or [Tutorials](../tutorials) section.

![Install GIS4WRF](../assets/images/gis4wrf-installation.gif)

!!! bug "Bug?"
    If you find a bug, or would like to suggest a new feature, please do let us know by [opening an issue on GitHub](https://github.com/GIS4WRF/gis4wrf/issues).