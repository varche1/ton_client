# ton_client

Python API client for blockchain [Telegram Open Network](https://test.ton.org/download.html) liteclient protocol, which is based itself on [tdlib](https://github.com/tdlib/td) library.   

[![Coverage](https://img.shields.io/codecov/c/github/formony/ton_client/master.svg)](https://codecov.io/gh/formony/ton_client)
[![Build Status](https://travis-ci.org/formony/ton_client.svg?branch=master)](https://travis-ci.org/formony/ton_client)
[![PEP8](https://img.shields.io/badge/code%20style-pep8-green.svg)](https://www.python.org/dev/peps/pep-0008/)

## Installation

This client works with Python 3.7 only.

Prerequisites: 
* [Pipfile](https://github.com/pypa/pipfile)

* ton_client is been shipped with prebuilt fullnode's client library for Ubuntu Xenial & latest macOS. 
In case of incompatibility with your distro it's needed to build TON fullnode's libtonlibjson.so / libtonlibjson.dylib depends on archtecture. 
Check [here](https://github.com/formony/ton_client/tree/master/docs/ton.md) for fullnode's build instructions.
Don't forget to copy library file to ton_client/distlib/linux/libtonlibjon.so or ton_client/distlib/darwin/libtonlibjon.dylib

ton_client hasn't been published to PyPI yet so build and install it on your own:

`git clone https://github.com/formony/ton_client.git`

`make setup-all && python ./setup.py install`

# To be done

* [x] parallel multithreading calling of libtonlibjon. Note: there is no GIL problem due using ctypes.CDLL()
* [ ] support all the funcs of libtonlibjon as described in [spec](https://github.com/formony/ton_client/tree/master/docs/tonlib_api.tl). TL itself described [here](https://core.telegram.org/mtproto/TL)
* [ ] asyncio wrapper
* [ ] crypto primitives to work with plain keys
* [ ] support of BIP32 mnemonic
* [ ] support key derivation as in BIP44 
 