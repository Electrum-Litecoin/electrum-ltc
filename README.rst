Electrum-LTC - Lightweight Litecoin client
==========================================

**Electrum Litecoin** is a fast and secure wallet for Litecoin. It is designed to be lightweight and easy to use across multiple platforms.  

Features  
=============
- **Fast Transactions**: Low transaction fees and high speed with Litecoin’s network.  
- **Lightweight**: No need to download the entire blockchain.  
- **Multi-Platform Support**: Available for Windows, macOS, and Linux.  
- **Security**: Integration with hardware wallets for extra protection.


Getting started
===============

Electrum-LTC is a pure python application. If you want to use the
Qt interface, install the Qt dependencies::

    sudo apt-get install python3-pyqt5

If you downloaded the official package (tar.gz), you can run
Electrum-LTC from its root directory without installing it on your
system; all the python dependencies are included in the 'packages'
directory. To run Electrum-LTC from its root directory, just do::

    ./run_electrum

You can also install Electrum-LTC on your system, by running this command::

    sudo apt-get install python3-setuptools
    python3 -m pip install .[fast]

This will download and install the Python dependencies used by
Electrum-LTC instead of using the 'packages' directory.
The 'fast' extra contains some optional dependencies that we think
are often useful but they are not strictly needed.

If you cloned the git repository, you need to compile extra files
before you can run Electrum-LTC. Read the next section, "Development
Version".



Development version
===================

Check out the code from GitHub::

    git clone git://github.com/pooler/electrum-ltc.git
    cd electrum-ltc
    git submodule update --init

Run install (this should install dependencies)::

    python3 -m pip install .[fast]


Compile the protobuf description file::

    sudo apt-get install protobuf-compiler
    protoc --proto_path=electrum_ltc --python_out=electrum_ltc electrum_ltc/paymentrequest.proto

Create translations (optional)::

    sudo apt-get install python-requests gettext
    ./contrib/pull_locale




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

See :code:`electrum_ltc/gui/kivy/Readme.md`.
