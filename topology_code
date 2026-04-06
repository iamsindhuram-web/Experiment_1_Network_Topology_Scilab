// HYBRID TOPOLOGY (25 Nodes) – Different Shape
clear;
clc;
// 1. TOPOLOGY CREATION
NameOfNetwork = 'Hybrid_Topology_25Nodes';
NumberOfNodes = 25;
// STAR edges
StarStarts = [6 7 8 9 10 11];
StarEnds = [5 5 5 5 5 5];
// HYBRID edges
HybridStarts = [1 2 3 4 5 6 7];
HybridEnds = [2 3 4 5 6 7 8];
// RING edges
RingStarts = [12 13 14 15 16 17];
RingEnds = [13 14 15 16 17 12];
// BUS edges
BusStarts = [8 18 19 20 11 22 23 24];
BusEnds = [18 19 20 21 22 23 24 25];
// Combine edges
StartNodesOfEdge = [StarStarts, HybridStarts, RingStarts, BusStarts];
EndNodesOfEdge = [StarEnds, HybridEnds, RingEnds, BusEnds];
// Coordinates
XCoordinatesOfNodes = [200 300 400 500 600 700 800 900 700 600 ...
500 400 500 600 700 600 500 800 850 900 ...
950 700 650 600 550];
YCoordinatesOfNodes = [800 780 760 740 720 740 760 780 700 680 ...
660 600 580 600 660 700 720 640 620 600 ...
580 520 500 480 460];
// Create graph
[TopologyGraph] = NL_G_MakeGraph( ...
 NameOfNetwork, NumberOfNodes, ...
 StartNodesOfEdge, EndNodesOfEdge, ...
 XCoordinatesOfNodes, YCoordinatesOfNodes);
// Show graph
WindowIndex = 1;
[GraphMain] = NL_G_ShowGraph(TopologyGraph, WindowIndex);
xtitle("Hybrid Topology (25 Nodes)","X","Y");
// Highlight Ring Nodes
NodeColor = 5;
BorderThickness = 10;
NodeDiameter = 25;
WindowIndex = 8;
RingNodes = [12 13 14 15 16 17];
NL_G_HighlightNodes(TopologyGraph, RingNodes, ...
 NodeColor, BorderThickness, NodeDiameter, WindowIndex);
// Highlight Bus Edges
EdgeColor = 3;
EdgeWidth = 8;
WindowIndex = 9;
BusEdges = [20 21 22 23 24 25 26 27];
NL_G_HighlightEdges(TopologyGraph, BusEdges, ...
 EdgeColor, EdgeWidth, WindowIndex);
// Show indices
WindowIndex = 4;
NL_G_ShowGraphNE(TopologyGraph, WindowIndex);
// Console details
[ExtractNode, ExtractEdge] = NL_G_GraphSize(TopologyGraph);
disp("Number of nodes:");
disp(ExtractNode);
disp("Number of edges:");
disp(ExtractEdge);
