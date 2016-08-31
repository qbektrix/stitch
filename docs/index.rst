.. stitch documentation master file, created by
   sphinx-quickstart on Wed Aug 31 11:29:51 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

stitch
======

`stitch <https://github.com/TomAugspurger/stitch>`__ is a library for
making reproducible reports. It takes a markdown source file, executes
the code chunks, captures the output, and stitches the output into the
destination file.

While ``stitch`` is written in python, it can be used for
any of the dozens of `Jupyter
kernels <https://github.com/ipython/ipython/wiki/IPython-kernels-for-other-languages>`__.

Install
-------

At the moment, the name stitch is taken on PyPI via an inactive project.
You can install stitch from PyPI via

.. code-block:: sh

   pip install knotr

I know, it's confusing.
I've filed a claim for ``stitch`` on PyPI, but I think the people working that support queue are over-worked.
Once that gets processed, I'll put it up on conda-forge as well.
If you need a mnemonic, it's "I want knitr, but `not` the one written in `R`.
Also I wanted to confuse R users.
And knots are kind of like a buggy version of knits.

But to be clear the package name and command-line tool is ``stitch``.

Examples
--------

See the `example site <https://pystitch.github.io>`__ for a side-by-side
comparison of the markdown source and rendered output.
Links to a more complicated document rendered in various formats
is also provided.

What's in a Name?
-----------------

The name ``stitch`` has a couple meanings. Like R's ``knit``, we are
taking a source document, executing code chunks, and ``knit``\ ing or
``stitch``\ ing the output back into the document.

The second meaning is for ``stitch`` bringing together a bunch of great
libraries, minimizing the work we have to do ourselves. ``stitch`` uses

-  `Pandoc <http://pandoc.org/MANUAL.html>`__ markdown parsing and
   conversion to the destination output
-  `jupyter <http://jupyter.org>`__, specifically
   `jupyter-client <https://jupyter-client.readthedocs.io/en/latest/>`__
   for managing kernels, passing code to kernels, and capturing the
   output
-  `pandocfilters <https://github.com/jgm/pandocfilters/>`__ for
   converting code-chunk output to pandoc's AST
-  `pypandoc <https://github.com/coldfix/pypandoc>`__ for communicating
   with pandoc
-  `click <http://click.pocoo.org>`__ for the command-line interface.

``stitch`` itself is fairly minimal. The main tasks are

-  processing code-chunk arguments
-  passing the correct outputs from the jupyter kernel to pandocfilters
-  assembling all the chunks of text, code, and output in a sensible way
-  making things look nice

Contents:

.. toctree::
   :maxdepth: 2

   self
   api


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

