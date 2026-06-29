Converts MNIST (or other character datasets) images into skeleton-based graphs and applies spring relaxation with repulsion to adapt edge distances for unit-disk embedding. Designed as preprocessing for graph embedding onto neutral-atom quantum computers.

# Main Scripts

## construct_graph.py
Full pipeline from image to reduced graph: skeletonization, node extraction, connectivity, node merging, collinear node removal, and node value assignment from stroke intensity.

## transform_all_with_repulsion.py
Spring model + repulsion that rescales all edges and finds optimal node positioning for potential embedding. Early stopping when distance MSE converges.

## filter_dataset.py
Filters out overly large graphs (too computationally expensive for quantum simulation) and checks transformation quality via MSE to verify target distances are reached.

Example
python build_mnist_graphs_nx.py
python transform_all_with_repulsion.py
python filter_dataset.py
