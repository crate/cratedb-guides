.. _install-configure:

######################
Configuration Settings
######################

In order to configure CrateDB, please take note of the configuration file
locations and the available environment variables.


Configuration Files
===================

When using the package-based setup flavor for :ref:`install-deb` or
:ref:`install-rpm`, the main CrateDB configuration files are located within the
``/etc/crate`` directory.

When using the :ref:`install-adhoc` setup, or the :ref:`Microsoft Windows <windows-install>`
setup, the configuration files are located within the ``config/`` directory relative to the
working directory.

Environment Variables
=====================

For the vanilla package-based setup flavor, the CrateDB startup script reads
:ref:`crate-reference:conf-env` from the ``/etc/default/crate`` file on Debian systems.
On RPM systems, the ``/etc/sysconfig/crate`` file is used.

When using the :ref:`install-adhoc` setup, or the :ref:`Microsoft Windows <windows-install>`
setup, the environment variables will be defined by ``bin/crate{.sh,.bat}`` relative to the
working directory.

Here is an example::

    # Configure heap size (defaults to 256m min, 1g max).
    CRATE_HEAP_SIZE=2g

    # Maximum number of open files, defaults to 65535.
    # MAX_OPEN_FILES=65535

    # Maximum locked memory size. Set to "unlimited" if you use the
    # bootstrap.mlockall option in crate.yml. You must also set
    # CRATE_HEAP_SIZE.
    MAX_LOCKED_MEMORY=unlimited

    # Provide additional Java OPTS.
    # CRATE_JAVA_OPTS=

    # Force the JVM to use IPv4 only.
    CRATE_USE_IPV4=true


.. _sources: https://en.wikipedia.org/wiki/Source_(command)
