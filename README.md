**NOTE:** This repository is out of date and unmaintained. The current pydygraphs project is maintained [here](https://github.com/dinkelk/PyDyGraphs).

PyDyGraphs
-----
*Southwest Research Institute*
![alt tag](http://www.boulder.swri.edu/clark/swrilogo.gif)

An interactive charting library using [Dygraphs](http://dygraphs.com/) for the [Ipython Notebook](http://ipython.org/notebook.html), without the need for any remote hosting.

## Intent

The [Ipython Notebook](http://ipython.org/notebook.html) is an excellent tool for interacting with python and displaying data in real time. While tools like [matplotlib](http://matplotlib.org/) can generate static plots in the [Ipython Notebook](http://ipython.org/notebook.html), interactive javascript plots are often more useful for exploring the data. This module can be readily included in an [Ipython Notebook](http://ipython.org/notebook.html) and then used to generate beautiful time series plots with [Dygraphs](http://dygraphs.com/).

## Screenshots 

Simple Example
![SinglePlot](http://i.imgur.com/etR5a21.png)

Subplot with Range Selector
![RangeSelector](http://i.imgur.com/bAL7pH6)

Pandas Dataframe Plot
![Dataframe](http://i.imgur.com/eMaCXOM.png)


## How It Works

This python module generates javascript that interacts with the [Dygraphs](http://dygraphs.com/) library, and passes it to the [Ipython Notebook](http://ipython.org/notebook.html) kernel for execution.

Currently the *PyDyGraphs* module depends on [Pandas](http://pandas.pydata.org/) to generate a JSON representation of the data for plotting. This required dependancy may be removed with future work. [Pandas](http://pandas.pydata.org/) can be installed via [pip](https://pypi.python.org/pypi/pip).

## Example
Run the included example:examples/PyDyGraphTester.ipynb, or paste this code into an [Ipython Notebook](http://ipython.org/notebook.html) to generate an interactive timeseries plot:

    # Import pydygraphs and numpy
    import pydygraphs
    import numpy as np

    # Forma figure
    fig = pydygraphs.figure(width = 600, height = 400)

    # Generate data for the plot
    x = np.array(range(100))
    y = [np.sin(np.random.rand(100)),-np.sin(np.random.rand(100))]

    # Plot the data on the figure
    fig.plot(x,y, color=['navy','magenta'])
    fig.title("Figure 1")
    fig.xlabel('Series')
    fig.ylabel('Value')

    # Show the figure in this cell of the notebook
    fig.show()

## Installation:
Simply clone this repository and include the *pydygraphs.py* module in your [Ipython Notebooks](http://ipython.org/notebook.html).

## Want to contribute:
Please submit a pull request! Email dinkelk@gmail.com for questions.
