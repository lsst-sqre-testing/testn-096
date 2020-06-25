.. image:: https://img.shields.io/badge/testn--096-lsst.io-brightgreen.svg
   :target: https://testn-096.lsst.io
.. image:: https://github.com/lsst-sqre-testing/testn-096/workflows/CI/badge.svg
   :target: https://github.com/lsst-sqre-testing/testn-096/actions/

####
Test
####

TESTN-096
=========

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin facilisis pharetra neque, at semper nulla mattis auctor. Proin semper mollis enim eget interdum. Mauris eleifend eget diam vitae bibendum. Praesent ut aliquet odio, sodales imperdiet nisi. Nam interdum imperdiet tortor sed fringilla. Maecenas efficitur mi sodales nulla commodo rutrum. Ut ornare diam quam, sed commodo turpis aliquam et. In nec enim consequat, suscipit tortor sit amet, luctus ante. Integer dictum augue diam, non pulvinar massa euismod in. Morbi viverra condimentum auctor. Nullam et metus mauris. Cras risus ex, porta sit amet nibh et, dapibus auctor leo.

Links
=====

- Live drafts: https://testn-096.lsst.io
- GitHub: https://github.com/lsst-sqre-testing/testn-096

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-sqre-testing/testn-096

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
