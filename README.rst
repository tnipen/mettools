Yr-tools
==============================

Yr-tools consists of a set of tools to plot data from MEPS, Senorge, Netatmo, and KDVH


Features
--------

* Neighbourhood methods
* Timeseries

Examples
--------
Create a timeseries for Oslo showing two MEPS runs, Netatmo, and KDVH values

.. code-block:: bash

  yrtools plot -o figure.png -m meps:2017080100,meps:2017080106,netatmo,kdvh -lat 60 -lon 10 -r 10

Installing on Ubuntu
--------------------

**Prerequisites**

Yr-tools requires NetCDF as well as the python packages numpy, scipy, and matplotlib. The python
package mpltoolkits.basemap is optional, but provides a background map when verification scores are
plotted on a map. Install the packages as follows:

.. code-block:: bash

  sudo apt-get update
  sudo apt-get install netcdf-bin libnetcdf-dev libhdf5-serial-dev
  sudo apt-get install python-setuptools python-pip
  sudo apt-get install python-numpy python-scipy python-matplotlib python-mpltoolkits.basemap

**Installing from source**

Download the source code of the latest version:
https://github.com/WFRT/verif/releases/. Unzip the file and navigate into the extracted folder.

Then install Yr-tools by executing the following inside the extracted folder:

.. code-block:: bash

  sudo pip install -r requirements.txt
  sudo python setup.py install

This will create the executable ``/usr/local/bin/yrtools``. Add ``/usr/local/bin`` to your PATH environment
variable if necessary. If you do not have sudo privileges do:

.. code-block:: bash

  pip install -r requirements.txt --user
  python setup.py install --user

This will create the executable ``~/.local/bin/yrtools``. Add ``~/.local/bin`` to your PATH environment
variable.

Copyright and license
---------------------

Copyright (C) 2017 MET Norway. yrtools is licensed under `LGPL version 3
<https://github.com/tnipen/yrtools/blob/master/LICENSE>`_ or (at your option) any later version.
