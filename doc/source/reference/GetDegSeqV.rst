GetDegSeqV
'''''''''''''''

.. function:: GetDegSeqV(Graph, InDegV, OutDegV)

Returns in- and out-degree sequence vectors for all nodes.

Parameters:

- *Graph*: graph (input)
    A Snap.py graph or a network

- *InDegV*: TIntV (output)
    In-degree sequence vector

- *OutDegV*: TIntV (output)
    Out-degree sequence vector

Return Value:

- None

The following examples shows how to obtain the in- and out-degree sequence vectors for networks of class :class:`TNGraph`, :class:`TUNGraph`, and :class:`TNEANet`::

    import snap

    Graph = snap.GenRndGnm(snap.PNGraph, 100, 1000)
    result_in_degree = snap.TIntV()
    result_out_degree = snap.TIntV()
    snap.GetDegSeqV(Graph, result_in_degree, result_out_degree)
    for i in range(0, result_in_degree.Len()):
      print "Node %s has in-degree %s and out-degree %s" % (i,result_in_degree[i], result_out_degree[i])

    Graph = snap.GenRndGnm(snap.PUNGraph, 100, 1000)
    result_in_degree = snap.TIntV()
    result_out_degree = snap.TIntV()
    snap.GetDegSeqV(Graph, result_in_degree, result_out_degree)
    for i in range(0, result_in_degree.Len()):
      print "Node %s has in-degree %s and out-degree %s" % (i,result_in_degree[i], result_out_degree[i])

    Graph = snap.GenRndGnm(snap.PNEANet, 100, 1000)
    result_in_degree = snap.TIntV()
    result_out_degree = snap.TIntV()
    snap.GetDegSeqV(Graph, result_in_degree, result_out_degree)
    for i in range(0, result_in_degree.Len()):
      print "Node %s has in-degree %s and out-degree %s" % (i,result_in_degree[i], result_out_degree[i])

    