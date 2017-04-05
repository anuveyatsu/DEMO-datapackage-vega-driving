Relationship between gasoline prices and driving habits in the US based on [Driving Shifts Into Reverse](http://www.nytimes.com/imagepages/2010/05/02/business/02metrics.html) by Hannah Fairfield. The New York Times (May 2, 2010).

This is an example DataPackage that demonstrates usage of "Vega Graph Specifications". This Demo Data Package based on [this example](https://vega.github.io/vega-editor/?mode=vega&spec=driving).

## Views

To create graphs for your tabular DataPackage, the datapackage.json should include the views attribute that defines data views.

### Vega Graph Specifications

<script src="https://gist.github.com/anuveyatsu/8a3db6b83422fc7dc592bf1963fee275.js"></script>
To use "Vega Graph Specification" `specType` inside `views` attribute should be set to `vega` - line 34. You can use almost the same specifications inside `spec` attribute, that are used for setting the vega graphs. Only difference is that in `data` property, all `url` and `path` attributes are moved out. Instead of that, `source` attribute is used to reference a dataset - line 41.

### Simple Graph Specifications

On line 183 we define the second view that uses "Simple Graph Spec", `specType` inside `views` attribute is set to `simple` - line 186.

There are only 3 properties enough to define graph specifications. They should be set inside `spec` attribute - line 187.

<table class="table table-bordered table-striped resource-summary">
  <thead>
   <tr>
     <th>Attribute</th>
     <th>Type</th>
     <th>Description</th>
   </tr>
  </thead>
  <tbody>
    <tr>
      <th>type</th>
      <td>String</td>
      <td>line, bar, pie (defaults to line)</td>
    </tr>
    <tr>
      <th>group</th>
      <td>String</td>
      <td>Field name, that will be used as abscissa (usually date field)</td>
    </tr>
    <tr>
      <th>series</th>
      <td>Array</td>
      <td>Field name(s) that will be used as ordinate</td>
    </tr>
  </tbody>
</table>

Outside of `spec` attribute there are some other important parameters to note:

<table class="table table-bordered table-striped resource-summary">
  <thead>
   <tr>
     <th>Attribute</th>
     <th>Type</th>
     <th>Description</th>
   </tr>
  </thead>
  <tbody>
    <tr>
      <th>name</th>
      <td>String</td>
      <td>Unique identifier for view within list of views (lines 51 and 62)</td>
    </tr>
    <tr>
      <th>title</th>
      <td>String</td>
      <td>Title for the graph (lines 52 and 63)</td>
    </tr>
    <tr>
      <th>resources</th>
      <td>Array</td>
      <td>Data sources for this spec. It can be either resource name or index. By default it is the first resource (lines 53 and 64)</td>
    </tr>
    <tr>
      <th>specType</th>
      <td>String</td>
      <td>Available options: simple, vega, plotly <strong>(Required)</strong></td>
    </tr>
  </tbody>
</table>
