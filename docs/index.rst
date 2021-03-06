.. RedBaron documentation master file, created by
   sphinx-quickstart on Mon Mar 24 06:52:35 2014.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to RedBaron's documentation!
====================================

Introduction
------------

RedBaron is an abstraction on top of Baron to make it easy to use. It is
heavily inspired by BeautifulSoup.

Baron is a FST for Python, a Full Syntax Tree. By opposition to an AST which
drops some syntax information in the process of its creation (like empty lines,
comments, formatting), a FST keeps everything and guarantees the operation
**ast_to_code(code_to_ast(source_code)) == source_code**.

Installation
------------

Not released on pypi yet.

::

    pip install git+https://github.com/Psycojoker/redbaron.git

Basic usage
-----------

::

    from redbaron import RedBaron

    red = RedBaron("print 'hello world!'")
    red[0].value[0].value = "'hello from Baron!'"

    # alternativly, BeautifulSoup-style
    red.string.value = "'hello from Baron!'"

    red.dumps()  # gives you the modified source code

Table of content
----------------

.. toctree::
   :maxdepth: 2

   why


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

