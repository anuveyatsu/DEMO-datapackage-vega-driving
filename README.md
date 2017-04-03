This Demo Data Package implements an example from [here](https://vega.github.io/vega-editor/?mode=vega&spec=driving).

In the views spec, we use "Vega Graph Spec" - must be specified in `specType` attribute as `vega` (as in line 34 of code snippet below).
Only difference when using Vega spec is `data` attribute that is removed from the spec (see starting from line 35). Everything else is identical:

<script src="https://gist.github.com/anuveyatsu/8a3db6b83422fc7dc592bf1963fee275.js"></script>

Outside of `spec` attribute there are some other important parameters to note:

* `name` (line 32) - unique identifier for view within list of views.

* `title` (lines 33) - title for this graph.

* `resources` - data sources for this spec. It can be either resource name or index. By default it is the first resource so we could skip this property as we did in this example.

* `specType` (line 34) - used for defining syntax. In this demo datapackage we use `vega` (Vega Graph Spec).
