# d3.layout.grid

A grid layout for [D3](http://d3js.org).

## API

The grid layout takes a one-dimensional array of data and arranges it on a two-dimensional grid.

<a name="layout-grid" href="#layout-grid">#</a> d3.layout.<b>grid</b>()

Constructs a new grid layout.

<a name="grid" href="#grid">#</a> <b>grid</b>(<i>nodes</i>)

Computes the layout for *nodes*. Per default, the layout tries to keep the column and row number as equal as possible and uses point spacing. Two attributes are set on each node:

* x – the computed *x*-coordinate of the node position.
* y – the computed *y*-coordinate of the node position.

<a name="points" href="#points">#</a> grid.<b>points</b>()

Configure the grid to treat nodes as points, cf. [d3.scale.ordinal().rangePoints()](https://github.com/mbostock/d3/wiki/Ordinal-Scales#wiki-ordinal_rangePoints).

<a name="bands" href="#bands">#</a> grid.<b>bands</b>()

Configure the grid to treat nodes as bands, cf. [d3.scale.ordinal().rangeBands()](https://github.com/mbostock/d3/wiki/Ordinal-Scales#wiki-ordinal_rangeBands)

<a name="padding" href="#padding">#</a> grid.<b>padding</b>([<i>padding</i>])

Specify the *padding* between the node bands as [*x*, *y*]. *x* and *y* are relative to the band width/height, similar to the *padding* parameter of [d3.scale.ordinal().rangeBands()](https://github.com/mbostock/d3/wiki/Ordinal-Scales#wiki-ordinal_rangeBands).

If [nodeSize](#nodeSize) is set, *padding* is absolute. For example, to configure a grid layout for nodes with 100×100px size, and 20px horizontal and vertical padding, use:

```javascript
var grid = d3.layout.grid()
  .nodeSize([100, 100])
  .padding([20, 20]);
```

<a name="cols" href="#cols">#</a> grid.<b>cols</b>([<i>num</i>])

Fixes the layout to *num* columns or returns the number of columns (if it was set before).

<a name="rows" href="#rows">#</a> grid.<b>rows</b>([<i>num</i>])

Fixes the layout to *num* rows or returns the number of rows (if it was set before).

<a name="size" href="#size">#</a> grid.<b>size</b>([<i>size</i>])

If *size* is specified, sets the overall size of the layout as [*x*, *y*]. 

If *size* is set, returns the current *size*. Default size is 1×1.

If instead [nodeSize](#nodeSize) is set, returns the actual size of the layout *after* [grid](#grid) has been called.

<a name="nodeSize" href="#nodeSize">#</a> grid.<b>nodeSize</b>([<i>nodeSize</i>])

If *nodeSize* is specified, sets the size of an individual node as [*x*, *y*].

If *nodeSize* is set, returns the current *nodeSize*.

If instead [size](#size) is set, returns the actual size of a node *after* [grid](#grid) has been called.


## Examples

* [Grid layout demo](http://bl.ocks.org/herrstucki/5684816)

## Author

Jeremy Stucki, [Interactive Things](http://interactivethings.com)

## License

BSD, see LICENSE.txt
