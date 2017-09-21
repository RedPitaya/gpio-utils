# GPIO utilities

## Library

Since there is no official release for this library,
a generic version number ``0.1`` was used.

## Tools



## Building

First clone the repository:

.. code-block:: shell-session

   git clone git@github.com:RedPitaya/gpio-utils.git

To build the project do:

.. code-block:: shell-session

   meson builddir --prefix /opt/redpitaya --buildtype release
   cd builddir
   ninja

The library and tools can be installed into the default path using:

.. code-block:: shell-session

   ninja install
