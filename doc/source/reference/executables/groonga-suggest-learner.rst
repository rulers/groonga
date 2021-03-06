.. -*- rst -*-

.. highlightlang:: none

groonga-suggest-learner
=======================

Summary
-------

groonga-suggest-learner is a program to learn suggest result from data which derived from groonga-suggest-httpd.
Usually, it is used with groonga-suggest-httpd, but It is allowed to launch standalone.
In such a case, groonga-suggest-learner loads data from log directory.

Synopsis
--------

::

  groonga-suggest-learner [options] database_path

Usage
-----

groonga-suggest-leaner supports the two way of learning data.
One is learning data from groonga-suggest-httpd, the other is
learning data from already existing log files.

Learning data from groonga-suggest-httpd
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Execute groonga-suggest-learner.::

  groonga-suggest-learner testdb/db

Learning data from log files
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Execute groonga-suggest-learner with ``-l`` option.

Here is the sample to load log data under ``logs`` directory::

  groonga-suggest-learner -l logs testdb/db

Options
-------

.. cmdoption:: -r

   Specify endpoint for receiver.

.. cmdoption:: -s

   Specify endpoint for sender.

.. cmdoption:: -d

   Specify this option to daemonize.

.. cmdoption:: -l

   Specify log directory.

Parameters
----------

There is one required parameter - ``database_path``.

``database_path``
^^^^^^^^^^^^^^^^^

Specifies the path to a groonga database.



Related tables
--------------

Here is the list of table which learned data is stored. If you specify ``query`` as dataset name, following ``_DATASET`` suffix are replaced. Thus, ``event_query`` table is used.

* event_DATASET


