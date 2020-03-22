# Interactive Plotting Test


```python
import numpy as np
import os
import pandas

from bokeh.plotting import figure, show
from bokeh.models import ColumnDataSource
from bokeh.io import output_notebook, output_file
```


```python
output_notebook()
CUR_DIR = os.getcwd()
DATA_DIR = os.path.join(os.path.dirname(CUR_DIR), "data")
```



<div class="bk-root">
    <a href="https://bokeh.org" target="_blank" class="bk-logo bk-logo-small bk-logo-notebook"></a>
    <span id="1153">Loading BokehJS ...</span>
</div>




## Load some data


```python
RAW_DATA = os.path.join(DATA_DIR, "raw")
df = pandas.read_csv(os.path.join(RAW_DATA, "RKI_COVID19.csv"))
```

    Index(['IdBundesland', 'Bundesland', 'Landkreis', 'Altersgruppe', 'Geschlecht',
           'AnzahlFall', 'AnzahlTodesfall', 'ObjectId', 'Meldedatum',
           'IdLandkreis'],
          dtype='object')



```python
print(df.columns)


df.describe()


```

    Index(['IdBundesland', 'Bundesland', 'Landkreis', 'Altersgruppe', 'Geschlecht',
           'AnzahlFall', 'AnzahlTodesfall', 'ObjectId', 'Meldedatum',
           'IdLandkreis'],
          dtype='object')





<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>IdBundesland</th>
      <th>AnzahlFall</th>
      <th>AnzahlTodesfall</th>
      <th>ObjectId</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>8232.000000</td>
      <td>8232.000000</td>
      <td>8232.000000</td>
      <td>8232.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>7.644072</td>
      <td>2.024295</td>
      <td>0.005709</td>
      <td>151051.500000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.209093</td>
      <td>2.361126</td>
      <td>0.076945</td>
      <td>2376.518041</td>
    </tr>
    <tr>
      <th>min</th>
      <td>-1.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>146936.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>5.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>148993.750000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>8.000000</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>151051.500000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>9.000000</td>
      <td>2.000000</td>
      <td>0.000000</td>
      <td>153109.250000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>16.000000</td>
      <td>49.000000</td>
      <td>2.000000</td>
      <td>155167.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python







source = ColumnDataSource(df)
p = figure()
p.circle(x='Bundesland', y='IdBundesland', source=source, size=10, color='green')
```




<div style="display: table;"><div style="display: table-row;"><div style="display: table-cell;"><b title="bokeh.models.renderers.GlyphRenderer">GlyphRenderer</b>(</div><div style="display: table-cell;">id&nbsp;=&nbsp;'1294', <span id="1297" style="cursor: pointer;">&hellip;)</span></div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">data_source&nbsp;=&nbsp;ColumnDataSource(id='1258', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">glyph&nbsp;=&nbsp;Circle(id='1292', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">hover_glyph&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">js_event_callbacks&nbsp;=&nbsp;{},</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">js_property_callbacks&nbsp;=&nbsp;{},</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">level&nbsp;=&nbsp;'glyph',</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">muted&nbsp;=&nbsp;False,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">muted_glyph&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">name&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">nonselection_glyph&nbsp;=&nbsp;Circle(id='1293', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">selection_glyph&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">subscribed_events&nbsp;=&nbsp;[],</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">tags&nbsp;=&nbsp;[],</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">view&nbsp;=&nbsp;CDSView(id='1295', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">visible&nbsp;=&nbsp;True,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">x_range_name&nbsp;=&nbsp;'default',</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">y_range_name&nbsp;=&nbsp;'default')</div></div></div>
<script>
(function() {
  var expanded = false;
  var ellipsis = document.getElementById("1297");
  ellipsis.addEventListener("click", function() {
    var rows = document.getElementsByClassName("1296");
    for (var i = 0; i < rows.length; i++) {
      var el = rows[i];
      el.style.display = expanded ? "none" : "table-row";
    }
    ellipsis.innerHTML = expanded ? "&hellip;)" : "&lsaquo;&lsaquo;&lsaquo;";
    expanded = !expanded;
  });
})();
</script>





```python
p.title.text = 'Corona Fallzahlen nach Bundesländern'
p.xaxis.axis_label = 'Datum'
p.yaxis.axis_label = 'Infizierte'
```


```python
show(p)
```








<div class="bk-root" id="ed2dc385-dde6-4a0f-b9ab-2a67a541dd91" data-root-id="1259"></div>






```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python
N = 4000
```


```python
x = np.random.random(size=N) * 100
y = np.random.random(size=N) * 100
radii = np.random.random(size=N) * 1.5
colors = ["#%02x%02x%02x" % (int(r), int(g), 150) for r, g in zip(np.floor(50+2*x), np.floor(30+2*y))]


```


```python
output_notebook()
```



<div class="bk-root">
    <a href="https://bokeh.org" target="_blank" class="bk-logo bk-logo-small bk-logo-notebook"></a>
    <span id="1258">Loading BokehJS ...</span>
</div>





```python
p = figure()
p.circle(x, y, radius=radii, fill_color=colors, fill_alpha=0.6, line_color=None)
```




<div style="display: table;"><div style="display: table-row;"><div style="display: table-cell;"><b title="bokeh.models.renderers.GlyphRenderer">GlyphRenderer</b>(</div><div style="display: table-cell;">id&nbsp;=&nbsp;'1294', <span id="1297" style="cursor: pointer;">&hellip;)</span></div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">data_source&nbsp;=&nbsp;ColumnDataSource(id='1291', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">glyph&nbsp;=&nbsp;Circle(id='1292', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">hover_glyph&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">js_event_callbacks&nbsp;=&nbsp;{},</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">js_property_callbacks&nbsp;=&nbsp;{},</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">level&nbsp;=&nbsp;'glyph',</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">muted&nbsp;=&nbsp;False,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">muted_glyph&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">name&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">nonselection_glyph&nbsp;=&nbsp;Circle(id='1293', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">selection_glyph&nbsp;=&nbsp;None,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">subscribed_events&nbsp;=&nbsp;[],</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">tags&nbsp;=&nbsp;[],</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">view&nbsp;=&nbsp;CDSView(id='1295', ...),</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">visible&nbsp;=&nbsp;True,</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">x_range_name&nbsp;=&nbsp;'default',</div></div><div class="1296" style="display: none;"><div style="display: table-cell;"></div><div style="display: table-cell;">y_range_name&nbsp;=&nbsp;'default')</div></div></div>
<script>
(function() {
  var expanded = false;
  var ellipsis = document.getElementById("1297");
  ellipsis.addEventListener("click", function() {
    var rows = document.getElementsByClassName("1296");
    for (var i = 0; i < rows.length; i++) {
      var el = rows[i];
      el.style.display = expanded ? "none" : "table-row";
    }
    ellipsis.innerHTML = expanded ? "&hellip;)" : "&lsaquo;&lsaquo;&lsaquo;";
    expanded = !expanded;
  });
})();
</script>





```python
show(p)
```








<div class="bk-root" id="6ac07d84-f8c6-416f-b334-3709c1ec369b" data-root-id="1259"></div>






```python
output
```


```python

```
