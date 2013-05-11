************
Introduction
************

:Date: 11 May 2013
:Authors: Jürgen Hackl
:Contact: hackl.j@gmx.at
:Web site: http://github.com/hackl/pyre
:Copyright: This document has been placed in the public domain.
:License: PyRe is released under the GNU General Public Licence.
:Version: 5.0.1

.. warning::

   This is a preliminary program code!

   I wrote ``pyre`` for my Master's Thesis.
   The work isn't finished yet, so changes in the code are very likely! 

.. note::

   If you have any problems, found bugs in the code or have feature request
   comments or questions, please feel free to send a mail to `Jürgen Hackl`_.


.. _`Jürgen Hackl`: hackl.j@gmx.at



Purpose
=======

PyRe (python Reliability) is a python module for structural reliability
analysis. Its flexibility and extensibility make it applicable to a large
suite of problems. Along with core reliability analysis functionality, PyRe
includes methods for summarizing output.

.. note::

   At the moment only First-Order Reliability Methods are supported!
   Second-Order Reliability Methods and Monte Carlo Simulation will hopefully
   follow soon :)




History
=======

The FERUM (Finite Element Reliability Using Matlab) project was initiated in
1999 at the University of California, Berkeley, by Terje Haukaas and Armen Der
Kiureghian, primarily for pedagogical purposes aimed at teaching and learning
structural reliability and stochastic finite elements methods. [DerKiureghian2006]_
This code consists of an open-source Matlab toolbox, featuring various
structural reliability methods. The latest available version (version 3.1),
which can be downloaded from `FERUM`_. Since 2003, this code is no longer
officially maintained. [Bourinet2010]_

A new version of this open-source code (FERUM 4.x) based on a work carried out
at the Institut Français de Mécanique Avancée (`IFMA`_) in Clermont-Ferrand,
France. This version offers improved capabilities such as simulation-based
technique (Subset Simulation), Global Sensitivity Analysis (based on Sobol’s
indices), Reliability-Based Design Optimization (RBDO) algorithm, Global
Sensitivity Analysis and reliability assessment based on Support Vector
Machine (SVM) surrogates, etc. Beyond the new methods implemented in this
Matlab code. [Bourinet2009]_

Of the purpose, to use structural reliability analysis for the project "Risk
based decision framework for the optimal management of aging reinforced
concrete structures" [Hackl2013]_ a python version of FERUM has been created.

The focus here lies on the reliability analysis and not more on the finite
element method, so only the core function of FERUM are implemented.



Features
========

PyRe provides functionalities to make structural reliability analysis as easy
as possible. Here is a short list of some of its features:

* Perform reliability analysis with First-Order Reliability Methods

* Includes a large suite of well-documented statistical distributions.

* Uses NumPy for numerics wherever possible.

* No limitation on the limit state function

* Correlation between the random variables are possible

* Traces can be saved to the disk as plain text.

* PyRe can be embedded in larger programs, and results can be analyzed
  with the full power of Python.


Getting started
===============

This guide provides all the information needed to install PyRe, code a
reliability model, run the sampler, save and visualize the results. In
addition, it contains a list of the statistical distributions currently
available.

.. _`FERUM`: http://www.ce.berkeley.edu/projects/ferum/

.. _`IFMA`: http://www.ifma.fr/Recherche/Labos/FERUM