.. Hey Emacs, this is -*- rst -*-

   This file follows reStructuredText markup syntax; see
   http://docutils.sf.net/rst.html for more information.

.. include:: ../../global.inc



================================
  GC3Pie programming tutorials
================================

.. contents::


Implementing scientific workflows with GC3Pie
---------------------------------------------

This is the course material prepared for the GC3Pie for programmers training,
held at the University of Zurich on September 12-13, 2016.

The course aims at showing how to implement patterns commonly seen
in scientific computational workflows using Python and GC3Pie, and
provide users with enough knowledge of the tools available in GC3Pie
to extend and adapt the examples provided.

`Introduction to the training <https://github.com/uzh/gc3pie/tree/training-september-2016/docs/programmers/tutorials/workflows/part00.pdf>`_

  A presentation of the training material and outline of the course.
  Probably not much useful unless you're actually sitting in class.

`Overview of GC3Pie use cases <https://github.com/uzh/gc3pie/tree/training-september-2016/docs/programmers/tutorials/workflows/part01.pdf>`_

  A quick overview of the kind of computational use cases that GC3Pie
  can easily solve.

`GC3Pie basics <https://github.com/uzh/gc3pie/tree/training-september-2016/docs/programmers/tutorials/workflows/part02.pdf>`_

  The basics needed to write simple GC3Pie scripts: the minimal
  session-based script scaffolding, and the properties and features of
  the `Application`:class: object.

`Useful debugging commands <https://github.com/uzh/gc3pie/tree/training-september-2016/docs/programmers/tutorials/workflows/part03.pdf>`_

  Recall a few GC3Pie utilities that are especially useful when
  debugging code.

`Customizing command-line processing <https://github.com/uzh/gc3pie/tree/training-september-2016/docs/programmers/tutorials/workflows/part04.pdf>`_

  How to set up command-line argument and option processing in
  GC3Pie's `SessionBasedScript`:class:

`Application requirements <https://github.com/uzh/gc3pie/tree/training-july-2016/docs/programmers/tutorials/workflows/part05.pdf>`_

  How to specify running requirements for `Application`:class: tasks,
  e.g., how much memory is needed to run.

`Application control and post-processing <https://github.com/uzh/gc3pie/tree/training-july-2016/docs/programmers/tutorials/workflows/part06.pdf>`_

  How to check and react on the termination status of a GC3Pie
  Task/Application.

`Feedback form <https://docs.google.com/forms/d/e/1FAIpQLSdLO4MhQJJaujQrRPDyQvwz95Nki5H1TsSD5e4roIhRtkIC3A/viewform?usp=send_form>`_
  
.. _`Warholize Tutorial`:

The "Warholize" Workflow Tutorial
---------------------------------

In this tutorial we show how to use the GC3Pie libraries in order
to build a command line script which runs a complex workflow with
both parallelly- and sequentially-executing tasks.

The tutorial itself contains the complete source code of the
application (see `Literate Programming`_ on Wikipedia), so that you
will be able to test/modify it and produce a working ``warholize.py``
script by downloading the ``pylit.py``:file: script from the `PyLit
Homepage`_ and running the following command on the
``docs/programmers/tutorials/warholize/warholize.rst`` file,
from within the source tree of GC3Pie::

  $ ./pylit warholize.rst warholize.py


.. toctree::

  warholize/warholize


Example scripts
---------------

A collection of small example scripts highlighting different features
of GC3Pie is available in the source distribution, in folder
``examples/``:file:

`gdemo_simple.py`_

    Simplest script you can create. It only uses `Application` and
    `Engine` classes to create an application, submit it, check its
    status and retrieve its output.

`grun.py`_

    a `SessionBasedScript` that executes its argument as command. It
    can also run it multiple times by wrapping it in a
    ParallelTaskCollection or a SequentialTaskCollection, depending on
    a command line option. Useful for testing a configured resource.

`gdemo_session.py`_

    a simple `SessionBasedScript` that sums two values by customizing
    a `SequentialTaskCollection`.

`warholize.py`_

    an enhanced version of the `warholize` script proposed in the
    :ref:`Warholize Tutorial`

.. _`gdemo_simple.py`: https://github.com/uzh/gc3pie/tree/master/examples/gdemo_simple.py
.. _`gdemo_session.py`: https://github.com/uzh/gc3pie/tree/master/examples/gdemo_session.py
.. _`grun.py`: https://github.com/uzh/gc3pie/tree/master/examples/grun.py
.. _`warholize.py`: https://github.com/uzh/gc3pie/tree/master/examples/warholize.py



.. References:

.. _`GC3Pie 2012 Training event`: https://www.gc3.uzh.ch/edu/gc3pie2012/
.. _`Literate Programming`: http://en.wikipedia.org/wiki/Literate_programming
.. _`PyLit Homepage`: https://github.com/gmilde/PyLit
