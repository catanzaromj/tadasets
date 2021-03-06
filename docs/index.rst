.. tadasets documentation master file, created by
   sphinx-quickstart on Sun Jul 22 20:37:23 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


|PyPI version| |Travis-CI| |Codecov| |License: MIT|

This package provides some nice utilities for creating and loading data sets that are useful for Topological Data Analysis. Currently, we provide various synthetic data sets with particular topological features.


Setup
------

Installation requires Cython, and currently must be installed from source. An example of how to install is

.. code:: python

    pip install tadasets


Usage
------

The shape constructors are exposed in a functional interface, each returning a numpy array containing data sampled on the object. Available objects include

- torus
- d-sphere
- swiss roll
- infinity sign

Each shape can be embedded in arbitrary ambient dimension by supplying the :code:`ambient` argument. Additionally, noise can be added to the shape through the :code:`noise` argument.

.. code:: python

    import tadasets

    torus = tadasets.torus(n=2000, c=2, a=1, ambient=200, noise=0.2)
    swiss_roll = tadasets.swiss_roll(n=2000, r=4, ambient=10, noise=1.2)
    dsphere = tadasets.dsphere(n=1000, d=12, r=3.14, ambient=14, noise=0.14)
    infty_sign = tadasets.infty_sign(n=3000, noise=0.1)

Contributions
------------------

We welcome contributions of all shapes and sizes. There are lots of opportunities for potential projects, so please get in touch if you would like to help out. Everything from an implementation of your favorite distance, notebooks, examples, and documentation are all equally valuable so please don’t feel you can’t contribute.

To contribute please fork the project make your changes and submit a pull request. We will do our best to work through any issues with you and get your code merged into the main branch.


.. toctree::
    :hidden:
    :maxdepth: 2
    :caption: User Guide

    reference/index
    notebooks/Examples


 
.. |PyPI version| image:: https://badge.fury.io/py/tadasets.svg
   :target: https://badge.fury.io/py/tadasets
.. |Travis-CI| image:: https://travis-ci.org/scikit-tda/tadasets.svg?branch=master
    :target: https://travis-ci.org/scikit-tda/tadasets
.. |Codecov| image:: https://codecov.io/gh/scikit-tda/tadasets/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/scikit-tda/tadasets
.. |License: MIT| image:: https://img.shields.io/badge/License-MIT-yellow.svg
    :target: https://opensource.org/licenses/MIT