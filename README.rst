=============
 run-iwyu.py
=============
------------------------------------------------------
 Lint files and directories with include-what-you-use
------------------------------------------------------

.. contents::
   :local:

Introduction
============

A wrapper script around include-what-you-use,
suitable for linting multiple files
and to use for continuous integration.

This is an alternative to iwyu-tool.py,
that returns a sensible exit code,
and make it easy to run on a subset of a compilation database.


How to use?
===========

Copy `run-iwyu.py <run-iwyu.py>`_ in your project,
then run it on specific files or whole directories::

  ./run-iwyu.py -b build/ src include foo.cpp

It's possible to exclude paths from the recursive search::

  ./run-iwyu.py \
      --exclude src/third_party \
      --exclude '*_test.cpp' \
      src include
