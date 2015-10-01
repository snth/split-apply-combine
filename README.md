View the [slides on nbviewer](http://nbviewer.ipython.org/format/slides/github/snth/split-apply-combine/blob/master/The%20Split-Apply-Combine%20Pattern%20in%20Data%20Science%20and%20Python.ipynb#/)

# The Split-Apply-Combine Strategy in Data Science and Python

Many data science problems involve the application of a split-apply-combine pattern, where you break up a big dataset into independent pieces, operate on each piece in isolation and then put all the pieces back together. This crops up in all stages of a data analysis:

  * During data preparation, when performing group-wise ranking, standardisation, or normalisation.

  * During modelling, when fitting separate models to each group.

  * During communication, when creating summaries or visualisations for display or analysis.

Python has many tools that make it easy to utilise this strategy when solving data science problems. These range from list and dictionary comprehensions in the language, the *map* and *reduce* functions and *itertools* and *functools* modules in the standard library to dedicated packages like *Pandas*, *PyToolz*, *Blaze* and *Dask*.

Explicit recognition of the applicability of the pattern allows one to reuse standard components for the bookkeeping code that handles the splitting and combining of the independent pieces. This allows one to concentrate on the data analysis code that is unique to the problem at hand. Since implicit in the pattern is the independence of the pieces, its applicability immediately implies a strategy for parallelisation which allows one to easily scale one's solution from single core to out-of-core computation on multiple machines, often with only very few changes to the code required.

This talk will introduce the pattern and how to recognise it by presenting some common code blocks. We will then look at some of the tools available, in particular *Pandas* and *PyToolz*, demonstrate their use, and discuss their strengths and weaknesses. Finally we'll show how to take a simple analysis and parallelise it to process a dataset that is too large to fit in memory.

