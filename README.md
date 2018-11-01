# Synthetic Dataset mimicking the network of intermediate filaments (IFs)

Please, use Python with Pickle library to read the ground truth graph. See example below:

```
import numpy as np
import networkx as nx
import cPickle as pickle


def unpickle_graph(filename):
    """
    The function returns a networkx graph representation and numpy array with 
    coordinates of the nodes. The nodes are numbered from 0 to N-1.
    """
    with open(filename, 'rb') as fin:
        data = pickle.load(fin)
        return data['graph'], data['positions']
    return None, None

```
