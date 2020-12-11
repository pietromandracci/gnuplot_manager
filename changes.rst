=============
Version 0.1.5
=============

Modified functions
------------------

*plot_check()* and *plot_list()*
    now give an additional information: the index of the plot window
    inside of the *window_list* global variable

*plot_print()* and *plot_print_all()*
    now accept the *dirname* argument, by which it is possible
    to specify the directory where files must be saved.

Some parts of some functions have been rewritten, without
changing the way they are called, in a more optimized way
(at least I hope).

Documentation and testing
-------------------------

The *README.rst* file was updated.
    

=============
Version 0.1.4
=============

Package structure
-----------------

The *funcutils.py* module has been added and some
methods of the *_PlotWindow* class have been turned to
functions and moved there

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

*new_plot()*
    now it is possible to pass the *purge* argument, which is
    *True* by default, with which the data files are automatically
    deleted each time new data or functions are plotted without
    the *replot* option, and when the window is closes

*plot_curves()*
    now it is possible to give *None* instead of the x-values
    in some or all of the list items, which means that for that
    dataset only y-values are given.

*plot_close()*
    now the datafiles are deleted or not depending if the window
    has been opened with the *purge*options

*plot_close_all()*
    now tries to delete the *gnuplot_manager.out* directory,
    if it is empty

The functions used to plot from data now support the *volatile*
argument, which allows to pass data to gnuplot inline (without
writing them to disk) using the special filename *'-'*.
However, if the plot window contains plots made in this way,
plotting other data or functions on it using the *replot* option
is not possible.

Documentation & testing
-----------------------

- the *README.rst* file was updated
- the *demo.py* and *test.py* scripts were updated


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
