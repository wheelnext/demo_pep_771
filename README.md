This repository contains a simple demo package that makes use of a default extras to install recommended dependencies by default.

It is an example usage of the specification described in the PEP
draft at https://github.com/astrofrog/peps/pull/1.

To try this out, you will need the following branch of pip:

https://github.com/astrofrog/pip/tree/default-extras-pep

and this also relies automatically on the following branch of flit:

https://github.com/astrofrog/flit/tree/default-extras-pep

As an example, running:

    pip install .

will automatically install the 'recommended' extras and will be equivalent to:

    pip install ".[recommended]"

Note that numpy gets installed as it is in the recommended dependencies.

On the other hand, if running:

    pip install ".[yaml]"

The recommended dependencies are no longer installed by default.
