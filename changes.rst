=============
Version 0.1.4

=============

Added functions
---------------

The following functions were added

*plot_1d()*
    allows to plot from 1d data, useful if you want
    to give only y-values and let gnuplot use the
    ordinal number as x-values or for plots that
    require 1d data, like boxplots

*plot_box()*
    allows to plot a boxplot of the given data

Modified functions
------------------

*plot_curves()*
    now it is possible to give *None* instead of the x-values
    in some or all of the list items, which means that for that
    dataset only y-values are given




=============
Version 0.1.3
=============

Documentation & testing
-----------------------

- the *README.rst* file was updated
- the *test.py* script was updated
- the *demo.py* script was added
- the *__init__* docstring was updated

  
=============
Version 0.1.2
=============

Documentation & testing
-----------------------
Added the test script *test.py*


=============
Version 0.1.1
=============

Added functions
---------------

The following functions were added

*plot_print()* and *plot_print_all()*
    allow to export plots to files as images

Modified functions
------------------

*plot_curves()* and *plot_functions()*
    now the list to pass as argument must include a new item:
    a string which can contain additional options to give to
    gnuplot (or *None* if no additional options are required)

Bug fixies
----------

- The *plot_label()* function did not work for 3D graphs,
  since the z coordinate of the label was fixed to zero,
  now it is 1 for 3D graphs

Documentation
-------------

- The *README.rst* file was updated, and figures were added to it
- This file was added
