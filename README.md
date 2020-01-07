# D3 Tree Visualization with Variable Branch Length
This is a visualization for displaying hierarchical, tree-like relationships. It is an extension of the work others have done, in which I sought to allow the branch lengths to vary based on values provided in the source data. View the example at this link: [add link here]

Tree visualization features include:
* Variable branch length
* Expanding and collapsing nodes
* Panning
* Zooming
* Search for node name
* highlighting and centering on found node

I altered this visualization specifically for visualizing hierarchical clustering models. The example data here is a tree relationship of pop music artists, clustered via agglomerative clustering. The source file is data/example-musicians.json. Within this file, the tree is represented as a series of nested JSON objects. Each node has the following attributes:

* "name": The name of this node (e.g., artist name).
* "total_width": The distance from the root (left side) of the tree. This is used to produce branches of varying length.
* "children": A list of child nodes. An empty list denotes that this is a leaf node.

In this example, I've provided (fictitious) numbers to illustrate the kinds of statistics that can accompany this kind of visualization. At the leaves, I provide the artist's name and audience size, and at the non-leaf nodes I provide the combined audience total for all artists in the subtree below the node.

If you create your own example in a JSON file, the data source can be altered by changing the URL parameter value for "tree," as long as you put your file in the /data subdirectory.

## Running locally
* `./serve.sh`
* Point your web browser to http://localhost:8000/?tree=example-musicians

## License
MIT License.

Based on:
* https://gist.github.com/adamfeuer/a8950c5197fe491f13969a03100159d5
* https://gist.github.com/robschmuecker/7880033
* https://gist.github.com/PBrockmann/0f22818096428b12ea23
