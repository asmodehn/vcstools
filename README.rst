vcstools
========

The vcstools module provides a Python API for interacting with different version control systems (VCS/SCMs).

See http://www.ros.org/doc/independent/api/vcstools/html/

Installing
----------

Install the latest release on Ubuntu using apt-get::

  $ sudo apt-get install vcstools

On other Systems, use the pypi package::

  $ pip install vcstools

Testing
-------

Prerequisites::
subversion, bzr, git and hg must be setup already.
If you are running in a virtual machine, you will need to (taken from .travis.yml):

  $ sudo apt-get install subversion git mercurial bzr
  $ git config --global user.email "foo@example.com"
  $ git config --global user.name "Foo Bar"
  $ echo -e "[ui]\nusername = Your Name <your@mail.com>" >> ~/.hgrc
  $ bzr whoami "Your Name <name@example.com>"

Use the python library nose to test::

  $ nosetests

To test with coverage, make sure to have python-coverage installed and run::

  $ nosetests --with-coverage --cover-package vcstools

To run python3 compatibility tests, run either::

  $ nosetests3
  $ python3 -m unittest discover --pattern*.py

Test Status
-----------

.. image:: https://travis-ci.org/vcstools/vcstools.svg?branch=master
    :target: https://travis-ci.org/vcstools/vcstools

Developer Setup
---------------------

Clone the repository and setup a virtual environment to work (a good habit anyway).

Be aware that your VCS tools from the main system will be used, even if you are working in a virtual environment.

  $ git clone https://github.com/vcstools/vcstools
  $ sudo apt-get install virtualenvwrapper
  $ mkvirtualenv vcstools
  $ pip install -r requirements.txt

Be aware of the Tests Prerequisites ( Hg, SVN, Bzr, and Git must be setup ). Then you can run the tests : 

  $ cd vcstools
  $ make tests






