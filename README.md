Electrum-LTC - Lightweight Litecoin Wallet
==========================================

# License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Electrum-Litecoin/electrum-ltc/blob/master/LICENCE) file for details.

[![Download for Windows](https://img.shields.io/badge/Download-Windows-blue?logo=gitforwindows&style=for-the-badge&logoWidth=90&labelWidth=200)](https://github.com/Electrum-Litecoin/electrum-ltc/releases/download/v4.2.2.1/electrum-ltc-4.2.2.1-setup.exe)

[![Download for Linux](https://img.shields.io/badge/Download-Linux-orange?logo=linux&style=for-the-badge&logoWidth=90)](https://github.com/Electrum-Litecoin/electrum-ltc/releases/download/v4.2.2.1/electrum-ltc-4.2.2.1-x86_64.AppImage)

[![Download for MacOS](https://img.shields.io/badge/Download-MacOS-black?logo=apple&style=for-the-badge&logoWidth=90)](https://github.com/Electrum-Litecoin/electrum-ltc/releases/download/v4.2.2.1/electrum-ltc-4.2.2.1.dmg)

[![Download for Python](https://img.shields.io/badge/Download-Python-green?logo=python&style=for-the-badge&logoWidth=90)](https://github.com/Electrum-Litecoin/electrum-ltc/releases/download/v4.2.2.1/Electrum-LTC-4.2.2.1.tar.gz)

# Getting Started

Electrum-LTC is a pure Python application. If you want to use the Qt interface, install the Qt dependencies:

```bash
sudo apt-get install python3-pyqt5
```

If you downloaded the official package (tar.gz), you can run Electrum-LTC from its root directory without installing it on your system; all the Python dependencies are included in the 'packages' directory. To run Electrum-LTC from its root directory, simply run:

```bash
./run_electrum
```

You can also install Electrum-LTC on your system by running:

```bash
sudo apt-get install python3-setuptools
python3 -m pip install .[fast]
```

This will download and install the Python dependencies used by Electrum-LTC instead of using the 'packages' directory. The 'fast' extra contains some optional dependencies that are often useful, but not strictly needed.

If you cloned the Git repository, you need to compile extra files before you can run Electrum-LTC. Read the next section, "Development Version".

# Development Version

To get the code from GitHub:

```bash
git clone git://github.com/pooler/electrum-ltc.git
cd electrum-ltc
git submodule update --init
```

To install the dependencies:

```bash
python3 -m pip install .[fast]
```

To compile the protobuf description file:

```bash
sudo apt-get install protobuf-compiler
protoc --proto_path=electrum_ltc --python_out=electrum_ltc electrum_ltc/paymentrequest.proto
```

To create translations (optional):

```bash
sudo apt-get install python-requests gettext
./contrib/pull_locale
```

# Creating Binaries

## Linux (tarball)

See [contrib/build-linux/README.md](contrib/build-linux/README.md).

## Linux (AppImage)

See [contrib/build-linux/appimage/README.md](contrib/build-linux/appimage/README.md).

## macOS

See [contrib/osx/README.md](contrib/osx/README.md).

## Windows

See [contrib/build-wine/README.md](contrib/build-wine/README.md).
