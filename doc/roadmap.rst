++++++++++++++++++++++++++++++
Roadmap for a new Python C API
++++++++++++++++++++++++++++++

Roadmap
=======

* Step 1: Identify :ref:`Bad C API <bad-api>` and list functions that should
  be modified or even removed
* Step 2: Add an **opt-in** new C API with these cleanups. Test :ref:`popular
  C extensions <consumers>` to measure how much code is broken. Start to fix
  these C extensions. Slowly involve more and more players into the game.
* Step 3: Remove more functions. Maybe replace Py_INCREF() macro with a
  function call. Finish to all PyObject structure. Measure the performance.
  Decide what to do.
* Step 4: if step 3 gone fine and most people are still ok to continue, make
  the new C API as the default in CPython and add an option for **opt-out**.

Status
======

* 2018-07-29: `pythoncapi project <https://github.com/vstinner/pythoncapi>`_
  created on GitHub
* 2017-12-21: It's an idea. There is an old PEP draft, but no implementation,
  the PEP has no number and was not accepted yet (nor really proposed).

Players
=======

* CPython: Victor Stinner
* PyPy (cpyext): Ronan Lamy
* Cython: Stefan Behnel

Unknown status:

* `RustPython <https://github.com/RustPython/RustPython>`_
* MicroPython?
* IronPython?
* Jython?
* Pyjion
* Pyston
* any other?

Timeline
========

* 2018-06: capi-sig mailing list migrated to Mailman 3
* 2017-11: Idea proposed on python-dev, `[Python-Dev] Make the stable API-ABI
  usable
  <https://mail.python.org/pipermail/python-dev/2017-November/150607.html>`_
* 2017-09: Blog post: `A New C API for CPython
  <https://vstinner.github.io/new-python-c-api.html>`_
* 2017-09: Idea discussed at the CPython sprint at Instagram (California).
  Liked by all core developers. The expected performance slowdown is likely to
  be accepted.
* 2017-07: Idea proposed on python-ideas. `[Python-ideas] PEP: Hide
  implementation details in the C API
  <https://mail.python.org/pipermail/python-ideas/2017-July/046399.html>`_
* 2017-05: Idea proposed at the Python Language Summit, during Pycon US 2017.
  My `"Python performance" slides (PDF)
  <https://github.com/vstinner/conf/raw/master/2017-PyconUS/summit.pdf>`_.
  LWN article: `Keeping Python competitive
  <https://lwn.net/Articles/723752/#723949>`_.