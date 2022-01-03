# Spike-Sorting
Using PCA to reduce dimensionality and sort spikes.

Use pf PCA for dimensionality reduction with application to neuronal spike sorting.
Often neurophysiological recordings are done with electrodes places extracellularly in the
brain tissue such that a given electrode can pick up spikes from more than one neuron. However,
accurate interpretation of the data requires that responses of single neurons need to be examined
and quantified. In order to do this, each measured spike will need to be “sorted” according to which
neuron it originates from. The main clue that allows us to distinguish spikes from different cells
and sort them is the shape (i.e., waveform) of the spike itself – two spikes from the same neuron
have similar shapes whereas spikes from different neurons look (more) different. The catch is that
the shape, when just drawn out as a time waveform is a high dimensional quantity (e.g., if you
have 70 time samples that make up the shape of the waveform, then each spike is a 70-dimensional
quantity). If the dimensionality is reduced to small number while retaining key information about
the shape, then sorting becomes a lot easier. 

The file SpikeSorting.mat contains two variables - A continuous time series called voltage, and a
vector spikes containing the times at which spikes were detected using a peak picking algorithm.
