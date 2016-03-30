# variantviewer

A JBrowse plugin that adds some custom glyphs for variants


## Options

* heightScaler - Numerical value to collapse or exapand y-axis. By default 1px is 1 unit in -log10(pvalue) units, so making heightScaler: 2 makes smaller -log10(pvalue) scores more visible
* maxHeight - Numerical value to set track height. Default: 210px
* style->color - A color callback for the variables
* style->label - A string or callback for the feature label. Can be useful to only show labels above a certain score, e.g. `"style": { "label": "function(feature) { return -Math.log(feature.get('score'))>50 ? feature.get('name') : null; }"`
* showLabels - False by default
* useMyVariantInfo - Clicking on variant launches myvariant.info popup. Default: false


## Example configuration

      {
         "maxFeatureScreenDensity": 6,
         "storeClass" : "JBrowse/Store/SeqFeature/BEDTabix",
         "urlTemplate" : "HDL_pval_name.sort.bed.gz",
         "label" : "HDL_pvals",
         "type" : "VariantViewer/View/Track/VariantPlotter"
      }

## Screenshot

![](img/plotter.png)




