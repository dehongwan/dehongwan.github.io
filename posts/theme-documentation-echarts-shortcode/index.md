# Theme Documentation - Echarts Shortcode


The `echarts` shortcode supports data visualization in Hugo with [ECharts](https://echarts.apache.org/) library.

&lt;!--more--&gt;

**ECharts** is a library helping you to generate interactive data visualization.

The basic chart types ECharts supports include [line series](https://echarts.apache.org/en/option.html#series-line), [bar series](https://echarts.apache.org/en/option.html#series-line), [scatter series](https://echarts.apache.org/en/option.html#series-scatter), [pie charts](https://echarts.apache.org/en/option.html#series-pie), [candle-stick series](https://echarts.apache.org/en/option.html#series-candlestick), [boxplot series](https://echarts.apache.org/en/option.html#series-boxplot) for statistics, [map series](https://echarts.apache.org/en/option.html#series-map), [heatmap series](https://echarts.apache.org/en/option.html#series-heatmap), [lines series](https://echarts.apache.org/en/option.html#series-lines) for directional information, [graph series](https://echarts.apache.org/en/option.html#series-graph) for relationships, [treemap series](https://echarts.apache.org/en/option.html#series-treemap), [sunburst series](https://echarts.apache.org/en/option.html#series-sunburst), [parallel series](https://echarts.apache.org/en/option.html#series-parallel) for multi-dimensional data, [funnel series](https://echarts.apache.org/en/option.html#series-funnel), [gauge series](https://echarts.apache.org/en/option.html#series-gauge). And it&#39;s extremely easy to create a combinition of them with ECharts.

Just insert your ECharts option in `JSON`/`YAML`/`TOML` format in the `echarts` shortcode and that’s it.

Example `echarts` input in `JSON` format:

```json
{{&lt;/* echarts */&gt;}}
{
  &#34;title&#34;: {
    &#34;text&#34;: &#34;Summary Line Chart&#34;,
    &#34;top&#34;: &#34;2%&#34;,
    &#34;left&#34;: &#34;center&#34;
  },
  &#34;tooltip&#34;: {
    &#34;trigger&#34;: &#34;axis&#34;
  },
  &#34;legend&#34;: {
    &#34;data&#34;: [&#34;Email Marketing&#34;, &#34;Affiliate Advertising&#34;, &#34;Video Advertising&#34;, &#34;Direct View&#34;, &#34;Search Engine&#34;],
    &#34;top&#34;: &#34;10%&#34;
  },
  &#34;grid&#34;: {
    &#34;left&#34;: &#34;5%&#34;,
    &#34;right&#34;: &#34;5%&#34;,
    &#34;bottom&#34;: &#34;5%&#34;,
    &#34;top&#34;: &#34;20%&#34;,
    &#34;containLabel&#34;: true
  },
  &#34;toolbox&#34;: {
    &#34;feature&#34;: {
      &#34;saveAsImage&#34;: {
        &#34;title&#34;: &#34;Save as Image&#34;
      }
    }
  },
  &#34;xAxis&#34;: {
    &#34;type&#34;: &#34;category&#34;,
    &#34;boundaryGap&#34;: false,
    &#34;data&#34;: [&#34;Monday&#34;, &#34;Tuesday&#34;, &#34;Wednesday&#34;, &#34;Thursday&#34;, &#34;Friday&#34;, &#34;Saturday&#34;, &#34;Sunday&#34;]
  },
  &#34;yAxis&#34;: {
    &#34;type&#34;: &#34;value&#34;
  },
  &#34;series&#34;: [
    {
      &#34;name&#34;: &#34;Email Marketing&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [120, 132, 101, 134, 90, 230, 210]
    },
    {
      &#34;name&#34;: &#34;Affiliate Advertising&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [220, 182, 191, 234, 290, 330, 310]
    },
    {
      &#34;name&#34;: &#34;Video Advertising&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [150, 232, 201, 154, 190, 330, 410]
    },
    {
      &#34;name&#34;: &#34;Direct View&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [320, 332, 301, 334, 390, 330, 320]
    },
    {
      &#34;name&#34;: &#34;Search Engine&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [820, 932, 901, 934, 1290, 1330, 1320]
    }
  ]
}
{{&lt;/* /echarts */&gt;}}
```

The same in `YAML` format:

```yaml
{{&lt;/* echarts */&gt;}}
title:
    text: Summary Line Chart
    top: 2%
    left: center
tooltip:
    trigger: axis
legend:
    data:
        - Email Marketing
        - Affiliate Advertising
        - Video Advertising
        - Direct View
        - Search Engine
    top: 10%
grid:
    left: 5%
    right: 5%
    bottom: 5%
    top: 20%
    containLabel: true
toolbox:
    feature:
        saveAsImage:
            title: Save as Image
xAxis:
    type: category
    boundaryGap: false
    data:
        - Monday
        - Tuesday
        - Wednesday
        - Thursday
        - Friday
        - Saturday
        - Sunday
yAxis:
    type: value
series:
    - name: Email Marketing
      type: line
      stack: Total
      data:
          - 120
          - 132
          - 101
          - 134
          - 90
          - 230
          - 210
    - name: Affiliate Advertising
      type: line
      stack: Total
      data:
          - 220
          - 182
          - 191
          - 234
          - 290
          - 330
          - 310
    - name: Video Advertising
      type: line
      stack: Total
      data:
          - 150
          - 232
          - 201
          - 154
          - 190
          - 330
          - 410
    - name: Direct View
      type: line
      stack: Total
      data:
          - 320
          - 332
          - 301
          - 334
          - 390
          - 330
          - 320
    - name: Search Engine
      type: line
      stack: Total
      data:
          - 820
          - 932
          - 901
          - 934
          - 1290
          - 1330
          - 1320
{{&lt;/* /echarts */&gt;}}
```

The same in `TOML` format:

```toml
{{&lt;/* echarts */&gt;}}
[title]
text = &#34;Summary Line Chart&#34;
top = &#34;2%&#34;
left = &#34;center&#34;

[tooltip]
trigger = &#34;axis&#34;

[legend]
data = [
  &#34;Email Marketing&#34;,
  &#34;Affiliate Advertising&#34;,
  &#34;Video Advertising&#34;,
  &#34;Direct View&#34;,
  &#34;Search Engine&#34;
]
top = &#34;10%&#34;

[grid]
left = &#34;5%&#34;
right = &#34;5%&#34;
bottom = &#34;5%&#34;
top = &#34;20%&#34;
containLabel = true

[toolbox]
[toolbox.feature]
[toolbox.feature.saveAsImage]
title = &#34;Save as Image&#34;

[xAxis]
type = &#34;category&#34;
boundaryGap = false
data = [
  &#34;Monday&#34;,
  &#34;Tuesday&#34;,
  &#34;Wednesday&#34;,
  &#34;Thursday&#34;,
  &#34;Friday&#34;,
  &#34;Saturday&#34;,
  &#34;Sunday&#34;
]

[yAxis]
type = &#34;value&#34;

[[series]]
name = &#34;Email Marketing&#34;
type = &#34;line&#34;
stack = &#34;Total&#34;
data = [
  120.0,
  132.0,
  101.0,
  134.0,
  90.0,
  230.0,
  210.0
]

[[series]]
name = &#34;Affiliate Advertising&#34;
type = &#34;line&#34;
stack = &#34;Total&#34;
data = [
  220.0,
  182.0,
  191.0,
  234.0,
  290.0,
  330.0,
  310.0
]

[[series]]
name = &#34;Video Advertising&#34;
type = &#34;line&#34;
stack = &#34;Total&#34;
data = [
  150.0,
  232.0,
  201.0,
  154.0,
  190.0,
  330.0,
  410.0
]

[[series]]
name = &#34;Direct View&#34;
type = &#34;line&#34;
stack = &#34;Total&#34;
data = [
  320.0,
  332.0,
  301.0,
  334.0,
  390.0,
  330.0,
  320.0
]

[[series]]
name = &#34;Search Engine&#34;
type = &#34;line&#34;
stack = &#34;Total&#34;
data = [
  820.0,
  932.0,
  901.0,
  934.0,
  1290.0,
  1330.0,
  1320.0
]
{{&lt;/* /echarts */&gt;}}
```

The rendered output looks like this:

{{&lt; echarts &gt;}}
{
  &#34;title&#34;: {
    &#34;text&#34;: &#34;Summary Line Chart&#34;,
    &#34;top&#34;: &#34;2%&#34;,
    &#34;left&#34;: &#34;center&#34;
  },
  &#34;tooltip&#34;: {
    &#34;trigger&#34;: &#34;axis&#34;
  },
  &#34;legend&#34;: {
    &#34;data&#34;: [&#34;Email Marketing&#34;, &#34;Affiliate Advertising&#34;, &#34;Video Advertising&#34;, &#34;Direct View&#34;, &#34;Search Engine&#34;],
    &#34;top&#34;: &#34;10%&#34;
  },
  &#34;grid&#34;: {
    &#34;left&#34;: &#34;5%&#34;,
    &#34;right&#34;: &#34;5%&#34;,
    &#34;bottom&#34;: &#34;5%&#34;,
    &#34;top&#34;: &#34;20%&#34;,
    &#34;containLabel&#34;: true
  },
  &#34;toolbox&#34;: {
    &#34;feature&#34;: {
      &#34;saveAsImage&#34;: {
        &#34;title&#34;: &#34;Save as Image&#34;
      }
    }
  },
  &#34;xAxis&#34;: {
    &#34;type&#34;: &#34;category&#34;,
    &#34;boundaryGap&#34;: false,
    &#34;data&#34;: [&#34;Monday&#34;, &#34;Tuesday&#34;, &#34;Wednesday&#34;, &#34;Thursday&#34;, &#34;Friday&#34;, &#34;Saturday&#34;, &#34;Sunday&#34;]
  },
  &#34;yAxis&#34;: {
    &#34;type&#34;: &#34;value&#34;
  },
  &#34;series&#34;: [
    {
      &#34;name&#34;: &#34;Email Marketing&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [120, 132, 101, 134, 90, 230, 210]
    },
    {
      &#34;name&#34;: &#34;Affiliate Advertising&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [220, 182, 191, 234, 290, 330, 310]
    },
    {
      &#34;name&#34;: &#34;Video Advertising&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [150, 232, 201, 154, 190, 330, 410]
    },
    {
      &#34;name&#34;: &#34;Direct View&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [320, 332, 301, 334, 390, 330, 320]
    },
    {
      &#34;name&#34;: &#34;Search Engine&#34;,
      &#34;type&#34;: &#34;line&#34;,
      &#34;stack&#34;: &#34;Total&#34;,
      &#34;data&#34;: [820, 932, 901, 934, 1290, 1330, 1320]
    }
  ]
}
{{&lt; /echarts &gt;}}

The `echarts` shortcode has also the following named parameters:

* **width** *[optional]* (**first** positional parameter)

    {{&lt; version 0.2.0 &gt;}} Width of the data visualization, default value is `100%`.

* **height** *[optional]* (**second** positional parameter)

    {{&lt; version 0.2.0 &gt;}} Height of the data visualization, default value is `30rem`.


---

> Author: Dillon  
> URL: https://dehongwan.github.io/posts/theme-documentation-echarts-shortcode/  

