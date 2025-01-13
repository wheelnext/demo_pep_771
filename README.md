This repository contains a simple demo package that makes use of a default extras to install recommended dependencies by default.

It is an example usage of the specification described in the PEP
draft at https://github.com/astrofrog/peps/pull/1.

To try this out, you will need the following branch of pip:

https://github.com/astrofrog/pip/tree/default-extras-pep

and this also relies automatically on the following branch of flit:

https://github.com/astrofrog/flit/tree/default-extras-pep

If you change to the ``package-recommended-extra``, you should be able to do:

* Install the package including the recommended extra:

    pip install .

* Install the package with the recommended extras explicitly:

    pip install ".[recommended]"

* Do a minimal installation of the package with no recommended extra:

    pip install ".[minimal]"

* Install the package with the ``yaml`` extra which causes the recommended extra to still be installed:

    pip install ".[yaml]"

* Install the package with the ``test`` extra which installs test dependencies and disables the default ``recommended`` extra

    pip install ".[test]"
