Electrum-BTX - Lightweight Bitcore client
=========================================

::

  Licence: MIT Licence
  Author: Thomas Voegtlin, LIMXTEC developers
  Language: Python (>= 3.6)
  Homepage: https://github.com/LIMXTEC/electrum-btx/releases

Getting started
===============

Electrum-BTX is a pure python application. If you want to use the
Qt interface, install the Qt dependencies::

    sudo apt-get install python3-pyqt5

If you downloaded the official package (tar.gz), you can run
Electrum-BTX from its root directory, without installing it on your
system; all the python dependencies are included in the 'packages'
directory. To run Electrum from its root directory, just do::

    ./run_electrum-btx

You can also install Electrum-BTX on your system, by running this command::

    sudo apt-get install python3-setuptools
    python3 -m pip install .[fast]

This will download and install the Python dependencies used by
Electrum-BTX, instead of using the 'packages' directory.
The 'fast' extra contains some optional dependencies that we think
are often useful but they are not strictly needed.

If you cloned the git repository, you need to compile extra files
before you can run Electrum-BTX. Read the next section, "Development
Version".



Development version
===================

Check out the code from GitHub::

    git clone git://github.com/LIMXTEC/electrum-btx.git
    cd electrum-btx

Run install (this should install dependencies)::

    python3 -m pip install .[fast]

Compile the protobuf description file::

    sudo apt-get install protobuf-compiler
    protoc --proto_path=lib/ --python_out=lib/ lib/paymentrequest.proto

Create translations (optional)::

    sudo apt-get install python-requests gettext
    ./contrib/make_locale



Creating Binaries
=================

Linux (tarball)
---------------

See :code:`contrib/build-linux/README.md`.


Linux (AppImage)
----------------

See :code:`contrib/build-linux/appimage/README.md`.


Mac OS X / macOS
----------------

See :code:`contrib/osx/README.md`.


Windows
-------

See :code:`contrib/build-wine/README.md`.


Android
-------

See :code:`electrum/gui/kivy/Readme.md`.
