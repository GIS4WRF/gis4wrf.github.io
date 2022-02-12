The installation of GIS4WRF requires the **latest version** of **QGIS 3**. Make sure that you follow the same steps in the same order as described below to avoid problems.

!!! tip
    For best user-experience and easiest installation, install on Windows.

## Supported platforms
GIS4WRF has been tested on Windows, macOS, and Ubuntu.

## Install QGIS

### Windows
Download the **latest version** of **QGIS Standalone Installer** from the [QGIS download page](https://www.qgis.org/en/site/forusers/download#windows) and install it using the guided installation. After you have successfully installed QGIS 3, go to [Install GIS4WRF](#install-gis4wrf).

### macOS
Download the **latest version** of **QGIS macOS Installer** from the [QGIS download page](https://qgis.org/en/site/forusers/download.html#mac)  and install it using the guided installation. After you have successfully installed QGIS 3, go to [Install GIS4WRF](#install-gis4wrf).

### Ubuntu

Copy, paste and execute the following in your Terminal prompt:

```bash
sudo apt-get install -y software-properties-common gnupg
wget -qO - https://qgis.org/downloads/qgis-2021.gpg.key | sudo gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/qgis-archive.gpg --import
sudo chmod a+r /etc/apt/trusted.gpg.d/qgis-archive.gpg
sudo add-apt-repository "deb https://qgis.org/ubuntu $(lsb_release -c -s) main"
sudo apt-get update
sudo apt-get install -y qgis mpich python3-pip
pip3 install --user f90nml netCDF4
```

After you have successfully installed QGIS 3, go to [Install GIS4WRF](#install-gis4wrf).

## Install GIS4WRF

The installation of GIS4WRF is straightforward and can be done directly in QGIS under the `Plugins` > `Manage and Install Plugins...` menu. If you want to know how to download pre-built binaries for WPS and WRF so that you can run simulations on Windows, macOS and Linux, see the [Configuration](../configuration) section. To learn how to use GIS4WRF see the [Documentation](../documentation/overview) or [Tutorials](../tutorials) section.

![Install GIS4WRF](../assets/images/gis4wrf-installation.gif)

!!! bug "Bug?"
    If you find a bug, or would like to suggest a new feature, please do let us know by [opening an issue on GitHub](https://github.com/GIS4WRF/gis4wrf/issues).