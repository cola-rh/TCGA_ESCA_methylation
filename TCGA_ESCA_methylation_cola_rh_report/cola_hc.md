cola Report for Hierarchical Partitioning - 'TCGA_ESCA_methylation'
==================

**Date**: 2021-07-22 16:26:36 CEST, **cola version**: 1.9.4

----------------------------------------------------------------

<style type='text/css'>

body, td, th {
   font-family: Arial,Helvetica,sans-serif;
   background-color: white;
   font-size: 13px;
  max-width: 800px;
  margin: auto;
  margin-left:210px;
  padding: 0px 10px 0px 10px;
  border-left: 1px solid #EEEEEE;
  line-height: 150%;
}

tt, code, pre {
   font-family: 'DejaVu Sans Mono', 'Droid Sans Mono', 'Lucida Console', Consolas, Monaco, 

monospace;
}

h1 {
   font-size:2.2em;
}

h2 {
   font-size:1.8em;
}

h3 {
   font-size:1.4em;
}

h4 {
   font-size:1.0em;
}

h5 {
   font-size:0.9em;
}

h6 {
   font-size:0.8em;
}

a {
  text-decoration: none;
  color: #0366d6;
}

a:hover {
  text-decoration: underline;
}

a:visited {
   color: #0366d6;
}

pre, img {
  max-width: 100%;
}
pre {
  overflow-x: auto;
}
pre code {
   display: block; padding: 0.5em;
}

code {
  font-size: 92%;
  border: 1px solid #ccc;
}

code[class] {
  background-color: #F8F8F8;
}

table, td, th {
  border: 1px solid #ccc;
}

blockquote {
   color:#666666;
   margin:0;
   padding-left: 1em;
   border-left: 0.5em #EEE solid;
}

hr {
   height: 0px;
   border-bottom: none;
   border-top-width: thin;
   border-top-style: dotted;
   border-top-color: #999999;
}

@media print {
   * {
      background: transparent !important;
      color: black !important;
      filter:none !important;
      -ms-filter: none !important;
   }

   body {
      font-size:12pt;
      max-width:100%;
   }

   a, a:visited {
      text-decoration: underline;
   }

   hr {
      visibility: hidden;
      page-break-before: always;
   }

   pre, blockquote {
      padding-right: 1em;
      page-break-inside: avoid;
   }

   tr, img {
      page-break-inside: avoid;
   }

   img {
      max-width: 100% !important;
   }

   @page :left {
      margin: 15mm 20mm 15mm 10mm;
   }

   @page :right {
      margin: 15mm 10mm 15mm 20mm;
   }

   p, h2, h3 {
      orphans: 3; widows: 3;
   }

   h2, h3 {
      page-break-after: avoid;
   }
}
</style>




## Summary



First the variable is renamed to `res_rh`.


```r
res_rh = rh
```



The partition hierarchy and all available functions which can be applied to `res_rh` object.


```r
res_rh
```

```
#> A 'HierarchicalPartition' object with 4 combinations of top-value methods and partitioning methods.
#>   On a matrix with 376149 rows and 202 columns.
#>   Performed in total 63000 partitions.
#>   There are 31 groups under the following parameters:
#>     - min_samples: 6
#>     - mean_silhouette_cutoff: 0.9
#>     - min_n_signatures: 1000 (signatures are selected based on:)
#>       - fdr_cutoff: 0.05
#>       - group_diff: 0.25
#> 
#> Hierarchy of the partition:
#>   0, 202 cols
#>   |-- 01, 71 cols, 18356 signatures
#>   |   |-- 011, 28 cols, 9255 signatures
#>   |   |   |-- 0111, 9 cols (b)
#>   |   |   |-- 0112, 11 cols (b)
#>   |   |   `-- 0113, 8 cols (b)
#>   |   |-- 012, 20 cols, 1449 signatures
#>   |   |   |-- 0121, 10 cols (b)
#>   |   |   |-- 0122, 5 cols (b)
#>   |   |   `-- 0123, 5 cols (b)
#>   |   `-- 013, 23 cols, 3489 signatures
#>   |       |-- 0131, 8 cols (b)
#>   |       |-- 0132, 7 cols (b)
#>   |       `-- 0133, 8 cols (b)
#>   |-- 02, 75 cols, 16138 signatures
#>   |   |-- 021, 15 cols, 10873 signatures
#>   |   |   |-- 0211, 6 cols (b)
#>   |   |   `-- 0212, 9 cols (b)
#>   |   |-- 022, 46 cols, 13097 signatures
#>   |   |   |-- 0221, 14 cols, 486 signatures (c)
#>   |   |   |-- 0222, 25 cols, 3429 signatures
#>   |   |   |   |-- 02221, 12 cols, 1432 signatures
#>   |   |   |   |   |-- 022211, 8 cols (b)
#>   |   |   |   |   `-- 022212, 4 cols (b)
#>   |   |   |   |-- 02222, 8 cols (b)
#>   |   |   |   `-- 02223, 5 cols (b)
#>   |   |   `-- 0223, 7 cols (b)
#>   |   `-- 023, 14 cols, 2070 signatures
#>   |       |-- 0231, 7 cols (b)
#>   |       |-- 0232, 4 cols (b)
#>   |       `-- 0233, 3 cols (b)
#>   |-- 03, 20 cols, 34722 signatures
#>   |   |-- 031, 5 cols (b)
#>   |   |-- 032, 5 cols (b)
#>   |   |-- 033, 4 cols (b)
#>   |   |-- 034, 4 cols (b)
#>   |   `-- 035, 2 cols (b)
#>   |-- 04, 14 cols, 4028 signatures
#>   |   |-- 041, 4 cols (b)
#>   |   |-- 042, 6 cols (b)
#>   |   `-- 043, 4 cols (b)
#>   `-- 05, 22 cols, 37386 signatures
#>       |-- 051, 8 cols (b)
#>       |-- 052, 8 cols (b)
#>       `-- 053, 6 cols (b)
#> Stop reason:
#>   b) Subgroup had too few columns.
#>   c) There were too few signatures.
#> 
#> Following methods can be applied to this 'HierarchicalPartition' object:
#>  [1] "all_leaves"            "all_nodes"             "cola_report"           "collect_classes"      
#>  [5] "colnames"              "compare_signatures"    "dimension_reduction"   "functional_enrichment"
#>  [9] "get_anno_col"          "get_anno"              "get_children_nodes"    "get_classes"          
#> [13] "get_matrix"            "get_signatures"        "is_leaf_node"          "max_depth"            
#> [17] "merge_node"            "ncol"                  "node_info"             "node_level"           
#> [21] "nrow"                  "rownames"              "show"                  "split_node"           
#> [25] "suggest_best_k"        "test_to_known_factors" "top_rows_heatmap"      "top_rows_overlap"     
#> 
#> You can get result for a single node by e.g. object["01"]
```

The call of `hierarchical_partition()` was:


```
#> hierarchical_partition(data = mat, top_n = 1000, top_value_method = c("SD", "ATC"), 
#>     partition_method = c("kmeans", "skmeans"), subset = 500, group_diff = 0.25, min_n_signatures = 1000, 
#>     filter_fun = function(mat) {
#>         s = rowSds(mat)
#>         order(-s)[1:30000]
#>     }, max_k = 8, scale_rows = FALSE, cores = 4)
```

Dimension of the input matrix:


```r
mat = get_matrix(res_rh)
dim(mat)
```

```
#> [1] 376149    202
```

All the methods that were tried:


```r
res_rh@param$combination_method
```

```
#> [[1]]
#> [1] "SD"     "kmeans"
#> 
#> [[2]]
#> [1] "ATC"    "kmeans"
#> 
#> [[3]]
#> [1] "SD"      "skmeans"
#> 
#> [[4]]
#> [1] "ATC"     "skmeans"
```

### Density distribution

The density distribution for each sample is visualized as one column in the following heatmap.
The clustering is based on the distance which is the Kolmogorov-Smirnov statistic between two distributions.




```r
library(ComplexHeatmap)
densityHeatmap(mat, ylab = "value", cluster_columns = TRUE, show_column_names = FALSE,
    mc.cores = 1)
```

![plot of chunk density-heatmap](figure_cola/density-heatmap-1.png)



Some values about the hierarchy:


```r
all_nodes(res_rh)
```

```
#>  [1] "0"      "01"     "011"    "0111"   "0112"   "0113"   "012"    "0121"   "0122"   "0123"  
#> [11] "013"    "0131"   "0132"   "0133"   "02"     "021"    "0211"   "0212"   "022"    "0221"  
#> [21] "0222"   "02221"  "022211" "022212" "02222"  "02223"  "0223"   "023"    "0231"   "0232"  
#> [31] "0233"   "03"     "031"    "032"    "033"    "034"    "035"    "04"     "041"    "042"   
#> [41] "043"    "05"     "051"    "052"    "053"
```

```r
all_leaves(res_rh)
```

```
#>  [1] "0111"   "0112"   "0113"   "0121"   "0122"   "0123"   "0131"   "0132"   "0133"   "0211"  
#> [11] "0212"   "0221"   "022211" "022212" "02222"  "02223"  "0223"   "0231"   "0232"   "0233"  
#> [21] "031"    "032"    "033"    "034"    "035"    "041"    "042"    "043"    "051"    "052"   
#> [31] "053"
```

```r
node_info(res_rh)
```

```
#>        id best_method depth best_k n_columns n_signatures p_signatures is_leaf
#> 1       0  SD:skmeans     1      5       202        67663      0.17988   FALSE
#> 2      01  ATC:kmeans     2      3        71        18356      0.04880   FALSE
#> 3     011  ATC:kmeans     3      3        28         9255      0.02460   FALSE
#> 4    0111 not applied     4     NA         9           NA           NA    TRUE
#> 5    0112 not applied     4     NA        11           NA           NA    TRUE
#> 6    0113 not applied     4     NA         8           NA           NA    TRUE
#> 7     012  ATC:kmeans     3      3        20         1449      0.00385   FALSE
#> 8    0121 not applied     4     NA        10           NA           NA    TRUE
#> 9    0122 not applied     4     NA         5           NA           NA    TRUE
#> 10   0123 not applied     4     NA         5           NA           NA    TRUE
#> 11    013  ATC:kmeans     3      3        23         3489      0.00928   FALSE
#> 12   0131 not applied     4     NA         8           NA           NA    TRUE
#> 13   0132 not applied     4     NA         7           NA           NA    TRUE
#> 14   0133 not applied     4     NA         8           NA           NA    TRUE
#> 15     02 ATC:skmeans     2      3        75        16138      0.04290   FALSE
#> 16    021  ATC:kmeans     3      2        15        10873      0.02891   FALSE
#> 17   0211 not applied     4     NA         6           NA           NA    TRUE
#> 18   0212 not applied     4     NA         9           NA           NA    TRUE
#> 19    022  ATC:kmeans     3      3        46        13097      0.03482   FALSE
#> 20   0221 ATC:skmeans     4      3        14          486      0.00129    TRUE
#> 21   0222  ATC:kmeans     4      3        25         3429      0.00912   FALSE
#> 22  02221  ATC:kmeans     5      2        12         1432      0.00381   FALSE
#> 23 022211 not applied     6     NA         8           NA           NA    TRUE
#> 24 022212 not applied     6     NA         4           NA           NA    TRUE
#> 25  02222 not applied     5     NA         8           NA           NA    TRUE
#> 26  02223 not applied     5     NA         5           NA           NA    TRUE
#> 27   0223 not applied     4     NA         7           NA           NA    TRUE
#> 28    023  ATC:kmeans     3      3        14         2070      0.00550   FALSE
#> 29   0231 not applied     4     NA         7           NA           NA    TRUE
#> 30   0232 not applied     4     NA         4           NA           NA    TRUE
#> 31   0233 not applied     4     NA         3           NA           NA    TRUE
#> 32     03  SD:skmeans     2      5        20        34722      0.09231   FALSE
#> 33    031 not applied     3     NA         5           NA           NA    TRUE
#> 34    032 not applied     3     NA         5           NA           NA    TRUE
#> 35    033 not applied     3     NA         4           NA           NA    TRUE
#> 36    034 not applied     3     NA         4           NA           NA    TRUE
#> 37    035 not applied     3     NA         2           NA           NA    TRUE
#> 38     04  ATC:kmeans     2      3        14         4028      0.01071   FALSE
#> 39    041 not applied     3     NA         4           NA           NA    TRUE
#> 40    042 not applied     3     NA         6           NA           NA    TRUE
#> 41    043 not applied     3     NA         4           NA           NA    TRUE
#> 42     05  ATC:kmeans     2      3        22        37386      0.09939   FALSE
#> 43    051 not applied     3     NA         8           NA           NA    TRUE
#> 44    052 not applied     3     NA         8           NA           NA    TRUE
#> 45    053 not applied     3     NA         6           NA           NA    TRUE
```

In the output from `node_info()`, there are the following columns:

- `id`: The node id.
- `best_method`: The best method selected.
- `depth`: Depth of the node in the hierarchy.
- `best_k`: Best number of groups of the partition on that node.
- `n_columns`: Number of columns in the submatrix.
- `n_signatures`: Number of signatures with the `best_k`.
- `p_signatures`: Proportion of hte signatures in total number of rows in the matrix.
- `is_leaf`: Whether the node is a leaf.

Labels of nodes are encoded in a special way. The number of digits
correspond to the depth of the node in the hierarchy and the value of the
digits correspond to the index of the subgroup in the current node, E.g. a label
of “012” means the node is the second subgroup of the partition which is the
first subgroup of the root node.

### Suggest the best k



Following table shows the best `k` (number of partitions) for each node in the
partition hierarchy. Clicking on the node name in the table goes to the
corresponding section for the partitioning on that node.

[The cola vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13)
explains the definition of the metrics used for determining the best
number of partitions.



```r
suggest_best_k(res_rh)
```


|Node                    |Best method                                         |Is leaf   |Best k |1-PAC |Mean silhouette |Concordance | #samples|   |
|:-----------------------|:---------------------------------------------------|:---------|:------|:-----|:---------------|:-----------|--------:|:--|
|[Node0](#Node0)         |SD:skmeans                                          |          |5      |1.00  |0.95            |0.98        |      202|** |
|[Node01](#Node01)       |ATC:kmeans                                          |          |3      |1.00  |0.96            |0.98        |       71|** |
|[Node011](#Node011)     |ATC:kmeans                                          |          |5      |0.90  |0.92            |0.91        |       28|*  |
|Node0111-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        9|   |
|Node0112-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |       11|   |
|Node0113-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|[Node012](#Node012)     |ATC:kmeans                                          |          |3      |1.00  |0.99            |0.99        |       20|** |
|Node0121-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |       10|   |
|Node0122-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        5|   |
|Node0123-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        5|   |
|[Node013](#Node013)     |ATC:kmeans                                          |          |3      |1.00  |0.95            |0.98        |       23|** |
|Node0131-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|Node0132-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        7|   |
|Node0133-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|[Node02](#Node02)       |ATC:skmeans                                         |          |3      |0.96  |0.95            |0.98        |       75|** |
|[Node021](#Node021)     |ATC:kmeans                                          |          |2      |1.00  |1.00            |1.00        |       15|** |
|Node0211-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        6|   |
|Node0212-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        9|   |
|[Node022](#Node022)     |ATC:kmeans                                          |          |3      |1.00  |0.97            |0.99        |       46|** |
|Node0221-leaf           |ATC:skmeans                                         |✓ (&#99;) |5      |0.91  |0.78            |0.94        |       14|*  |
|[Node0222](#Node0222)   |ATC:kmeans                                          |          |3      |1.00  |0.95            |0.98        |       25|** |
|[Node02221](#Node02221) |ATC:kmeans                                          |          |5      |0.91  |0.80            |0.95        |       12|*  |
|Node022211-leaf         |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|Node022212-leaf         |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        4|   |
|Node02222-leaf          |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|Node02223-leaf          |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        5|   |
|Node0223-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        7|   |
|[Node023](#Node023)     |ATC:kmeans                                          |          |3      |1.00  |1.00            |1.00        |       14|** |
|Node0231-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        7|   |
|Node0232-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        4|   |
|Node0233-leaf           |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        3|   |
|[Node03](#Node03)       |SD:skmeans                                          |          |5      |0.93  |0.97            |0.97        |       20|*  |
|Node031-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        5|   |
|Node032-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        5|   |
|Node033-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        4|   |
|Node034-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        4|   |
|Node035-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        2|   |
|[Node04](#Node04)       |ATC:kmeans                                          |          |3      |1.00  |1.00            |1.00        |       14|** |
|Node041-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        4|   |
|Node042-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        6|   |
|Node043-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        4|   |
|[Node05](#Node05)       |ATC:kmeans                                          |          |3      |1.00  |0.99            |0.99        |       22|** |
|Node051-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|Node052-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        8|   |
|Node053-leaf            |<span style='color:grey;'><i>not applied</i></span> |✓ (b)     |       |      |                |            |        6|   |


Stop reason: b) Subgroup had too few columns. c) There were too few signatures. 

\*\*: 1-PAC > 0.95, \*: 1-PAC > 0.9


### Partition hierarchy

The nodes of the hierarchy can be merged by setting the `merge_node` parameters. Here we 
control the hierarchy with the `min_n_signatures` parameter. The value of `min_n_signatures` is
from `node_info()`.





<style type='text/css'>



.ui-helper-hidden {
	display: none;
}
.ui-helper-hidden-accessible {
	border: 0;
	clip: rect(0 0 0 0);
	height: 1px;
	margin: -1px;
	overflow: hidden;
	padding: 0;
	position: absolute;
	width: 1px;
}
.ui-helper-reset {
	margin: 0;
	padding: 0;
	border: 0;
	outline: 0;
	line-height: 1.3;
	text-decoration: none;
	font-size: 100%;
	list-style: none;
}
.ui-helper-clearfix:before,
.ui-helper-clearfix:after {
	content: "";
	display: table;
	border-collapse: collapse;
}
.ui-helper-clearfix:after {
	clear: both;
}
.ui-helper-zfix {
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	position: absolute;
	opacity: 0;
	filter:Alpha(Opacity=0); 
}

.ui-front {
	z-index: 100;
}



.ui-state-disabled {
	cursor: default !important;
	pointer-events: none;
}



.ui-icon {
	display: inline-block;
	vertical-align: middle;
	margin-top: -.25em;
	position: relative;
	text-indent: -99999px;
	overflow: hidden;
	background-repeat: no-repeat;
}

.ui-widget-icon-block {
	left: 50%;
	margin-left: -8px;
	display: block;
}




.ui-widget-overlay {
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
}
.ui-accordion .ui-accordion-header {
	display: block;
	cursor: pointer;
	position: relative;
	margin: 2px 0 0 0;
	padding: .5em .5em .5em .7em;
	font-size: 100%;
}
.ui-accordion .ui-accordion-content {
	padding: 1em 2.2em;
	border-top: 0;
	overflow: auto;
}
.ui-autocomplete {
	position: absolute;
	top: 0;
	left: 0;
	cursor: default;
}
.ui-menu {
	list-style: none;
	padding: 0;
	margin: 0;
	display: block;
	outline: 0;
}
.ui-menu .ui-menu {
	position: absolute;
}
.ui-menu .ui-menu-item {
	margin: 0;
	cursor: pointer;
	
	list-style-image: url("data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7");
}
.ui-menu .ui-menu-item-wrapper {
	position: relative;
	padding: 3px 1em 3px .4em;
}
.ui-menu .ui-menu-divider {
	margin: 5px 0;
	height: 0;
	font-size: 0;
	line-height: 0;
	border-width: 1px 0 0 0;
}
.ui-menu .ui-state-focus,
.ui-menu .ui-state-active {
	margin: -1px;
}


.ui-menu-icons {
	position: relative;
}
.ui-menu-icons .ui-menu-item-wrapper {
	padding-left: 2em;
}


.ui-menu .ui-icon {
	position: absolute;
	top: 0;
	bottom: 0;
	left: .2em;
	margin: auto 0;
}


.ui-menu .ui-menu-icon {
	left: auto;
	right: 0;
}
.ui-button {
	padding: .4em 1em;
	display: inline-block;
	position: relative;
	line-height: normal;
	margin-right: .1em;
	cursor: pointer;
	vertical-align: middle;
	text-align: center;
	-webkit-user-select: none;
	-moz-user-select: none;
	-ms-user-select: none;
	user-select: none;

	
	overflow: visible;
}

.ui-button,
.ui-button:link,
.ui-button:visited,
.ui-button:hover,
.ui-button:active {
	text-decoration: none;
}


.ui-button-icon-only {
	width: 2em;
	box-sizing: border-box;
	text-indent: -9999px;
	white-space: nowrap;
}


input.ui-button.ui-button-icon-only {
	text-indent: 0;
}


.ui-button-icon-only .ui-icon {
	position: absolute;
	top: 50%;
	left: 50%;
	margin-top: -8px;
	margin-left: -8px;
}

.ui-button.ui-icon-notext .ui-icon {
	padding: 0;
	width: 2.1em;
	height: 2.1em;
	text-indent: -9999px;
	white-space: nowrap;

}

input.ui-button.ui-icon-notext .ui-icon {
	width: auto;
	height: auto;
	text-indent: 0;
	white-space: normal;
	padding: .4em 1em;
}



input.ui-button::-moz-focus-inner,
button.ui-button::-moz-focus-inner {
	border: 0;
	padding: 0;
}
.ui-controlgroup {
	vertical-align: middle;
	display: inline-block;
}
.ui-controlgroup > .ui-controlgroup-item {
	float: left;
	margin-left: 0;
	margin-right: 0;
}
.ui-controlgroup > .ui-controlgroup-item:focus,
.ui-controlgroup > .ui-controlgroup-item.ui-visual-focus {
	z-index: 9999;
}
.ui-controlgroup-vertical > .ui-controlgroup-item {
	display: block;
	float: none;
	width: 100%;
	margin-top: 0;
	margin-bottom: 0;
	text-align: left;
}
.ui-controlgroup-vertical .ui-controlgroup-item {
	box-sizing: border-box;
}
.ui-controlgroup .ui-controlgroup-label {
	padding: .4em 1em;
}
.ui-controlgroup .ui-controlgroup-label span {
	font-size: 80%;
}
.ui-controlgroup-horizontal .ui-controlgroup-label + .ui-controlgroup-item {
	border-left: none;
}
.ui-controlgroup-vertical .ui-controlgroup-label + .ui-controlgroup-item {
	border-top: none;
}
.ui-controlgroup-horizontal .ui-controlgroup-label.ui-widget-content {
	border-right: none;
}
.ui-controlgroup-vertical .ui-controlgroup-label.ui-widget-content {
	border-bottom: none;
}


.ui-controlgroup-vertical .ui-spinner-input {

	
	width: 75%;
	width: calc( 100% - 2.4em );
}
.ui-controlgroup-vertical .ui-spinner .ui-spinner-up {
	border-top-style: solid;
}

.ui-checkboxradio-label .ui-icon-background {
	box-shadow: inset 1px 1px 1px #ccc;
	border-radius: .12em;
	border: none;
}
.ui-checkboxradio-radio-label .ui-icon-background {
	width: 16px;
	height: 16px;
	border-radius: 1em;
	overflow: visible;
	border: none;
}
.ui-checkboxradio-radio-label.ui-checkboxradio-checked .ui-icon,
.ui-checkboxradio-radio-label.ui-checkboxradio-checked:hover .ui-icon {
	background-image: none;
	width: 8px;
	height: 8px;
	border-width: 4px;
	border-style: solid;
}
.ui-checkboxradio-disabled {
	pointer-events: none;
}
.ui-datepicker {
	width: 17em;
	padding: .2em .2em 0;
	display: none;
}
.ui-datepicker .ui-datepicker-header {
	position: relative;
	padding: .2em 0;
}
.ui-datepicker .ui-datepicker-prev,
.ui-datepicker .ui-datepicker-next {
	position: absolute;
	top: 2px;
	width: 1.8em;
	height: 1.8em;
}
.ui-datepicker .ui-datepicker-prev-hover,
.ui-datepicker .ui-datepicker-next-hover {
	top: 1px;
}
.ui-datepicker .ui-datepicker-prev {
	left: 2px;
}
.ui-datepicker .ui-datepicker-next {
	right: 2px;
}
.ui-datepicker .ui-datepicker-prev-hover {
	left: 1px;
}
.ui-datepicker .ui-datepicker-next-hover {
	right: 1px;
}
.ui-datepicker .ui-datepicker-prev span,
.ui-datepicker .ui-datepicker-next span {
	display: block;
	position: absolute;
	left: 50%;
	margin-left: -8px;
	top: 50%;
	margin-top: -8px;
}
.ui-datepicker .ui-datepicker-title {
	margin: 0 2.3em;
	line-height: 1.8em;
	text-align: center;
}
.ui-datepicker .ui-datepicker-title select {
	font-size: 1em;
	margin: 1px 0;
}
.ui-datepicker select.ui-datepicker-month,
.ui-datepicker select.ui-datepicker-year {
	width: 45%;
}
.ui-datepicker table {
	width: 100%;
	font-size: .9em;
	border-collapse: collapse;
	margin: 0 0 .4em;
}
.ui-datepicker th {
	padding: .7em .3em;
	text-align: center;
	font-weight: bold;
	border: 0;
}
.ui-datepicker td {
	border: 0;
	padding: 1px;
}
.ui-datepicker td span,
.ui-datepicker td a {
	display: block;
	padding: .2em;
	text-align: right;
	text-decoration: none;
}
.ui-datepicker .ui-datepicker-buttonpane {
	background-image: none;
	margin: .7em 0 0 0;
	padding: 0 .2em;
	border-left: 0;
	border-right: 0;
	border-bottom: 0;
}
.ui-datepicker .ui-datepicker-buttonpane button {
	float: right;
	margin: .5em .2em .4em;
	cursor: pointer;
	padding: .2em .6em .3em .6em;
	width: auto;
	overflow: visible;
}
.ui-datepicker .ui-datepicker-buttonpane button.ui-datepicker-current {
	float: left;
}


.ui-datepicker.ui-datepicker-multi {
	width: auto;
}
.ui-datepicker-multi .ui-datepicker-group {
	float: left;
}
.ui-datepicker-multi .ui-datepicker-group table {
	width: 95%;
	margin: 0 auto .4em;
}
.ui-datepicker-multi-2 .ui-datepicker-group {
	width: 50%;
}
.ui-datepicker-multi-3 .ui-datepicker-group {
	width: 33.3%;
}
.ui-datepicker-multi-4 .ui-datepicker-group {
	width: 25%;
}
.ui-datepicker-multi .ui-datepicker-group-last .ui-datepicker-header,
.ui-datepicker-multi .ui-datepicker-group-middle .ui-datepicker-header {
	border-left-width: 0;
}
.ui-datepicker-multi .ui-datepicker-buttonpane {
	clear: left;
}
.ui-datepicker-row-break {
	clear: both;
	width: 100%;
	font-size: 0;
}


.ui-datepicker-rtl {
	direction: rtl;
}
.ui-datepicker-rtl .ui-datepicker-prev {
	right: 2px;
	left: auto;
}
.ui-datepicker-rtl .ui-datepicker-next {
	left: 2px;
	right: auto;
}
.ui-datepicker-rtl .ui-datepicker-prev:hover {
	right: 1px;
	left: auto;
}
.ui-datepicker-rtl .ui-datepicker-next:hover {
	left: 1px;
	right: auto;
}
.ui-datepicker-rtl .ui-datepicker-buttonpane {
	clear: right;
}
.ui-datepicker-rtl .ui-datepicker-buttonpane button {
	float: left;
}
.ui-datepicker-rtl .ui-datepicker-buttonpane button.ui-datepicker-current,
.ui-datepicker-rtl .ui-datepicker-group {
	float: right;
}
.ui-datepicker-rtl .ui-datepicker-group-last .ui-datepicker-header,
.ui-datepicker-rtl .ui-datepicker-group-middle .ui-datepicker-header {
	border-right-width: 0;
	border-left-width: 1px;
}


.ui-datepicker .ui-icon {
	display: block;
	text-indent: -99999px;
	overflow: hidden;
	background-repeat: no-repeat;
	left: .5em;
	top: .3em;
}
.ui-dialog {
	position: absolute;
	top: 0;
	left: 0;
	padding: .2em;
	outline: 0;
}
.ui-dialog .ui-dialog-titlebar {
	padding: .4em 1em;
	position: relative;
}
.ui-dialog .ui-dialog-title {
	float: left;
	margin: .1em 0;
	white-space: nowrap;
	width: 90%;
	overflow: hidden;
	text-overflow: ellipsis;
}
.ui-dialog .ui-dialog-titlebar-close {
	position: absolute;
	right: .3em;
	top: 50%;
	width: 20px;
	margin: -10px 0 0 0;
	padding: 1px;
	height: 20px;
}
.ui-dialog .ui-dialog-content {
	position: relative;
	border: 0;
	padding: .5em 1em;
	background: none;
	overflow: auto;
}
.ui-dialog .ui-dialog-buttonpane {
	text-align: left;
	border-width: 1px 0 0 0;
	background-image: none;
	margin-top: .5em;
	padding: .3em 1em .5em .4em;
}
.ui-dialog .ui-dialog-buttonpane .ui-dialog-buttonset {
	float: right;
}
.ui-dialog .ui-dialog-buttonpane button {
	margin: .5em .4em .5em 0;
	cursor: pointer;
}
.ui-dialog .ui-resizable-n {
	height: 2px;
	top: 0;
}
.ui-dialog .ui-resizable-e {
	width: 2px;
	right: 0;
}
.ui-dialog .ui-resizable-s {
	height: 2px;
	bottom: 0;
}
.ui-dialog .ui-resizable-w {
	width: 2px;
	left: 0;
}
.ui-dialog .ui-resizable-se,
.ui-dialog .ui-resizable-sw,
.ui-dialog .ui-resizable-ne,
.ui-dialog .ui-resizable-nw {
	width: 7px;
	height: 7px;
}
.ui-dialog .ui-resizable-se {
	right: 0;
	bottom: 0;
}
.ui-dialog .ui-resizable-sw {
	left: 0;
	bottom: 0;
}
.ui-dialog .ui-resizable-ne {
	right: 0;
	top: 0;
}
.ui-dialog .ui-resizable-nw {
	left: 0;
	top: 0;
}
.ui-draggable .ui-dialog-titlebar {
	cursor: move;
}
.ui-draggable-handle {
	-ms-touch-action: none;
	touch-action: none;
}
.ui-resizable {
	position: relative;
}
.ui-resizable-handle {
	position: absolute;
	font-size: 0.1px;
	display: block;
	-ms-touch-action: none;
	touch-action: none;
}
.ui-resizable-disabled .ui-resizable-handle,
.ui-resizable-autohide .ui-resizable-handle {
	display: none;
}
.ui-resizable-n {
	cursor: n-resize;
	height: 7px;
	width: 100%;
	top: -5px;
	left: 0;
}
.ui-resizable-s {
	cursor: s-resize;
	height: 7px;
	width: 100%;
	bottom: -5px;
	left: 0;
}
.ui-resizable-e {
	cursor: e-resize;
	width: 7px;
	right: -5px;
	top: 0;
	height: 100%;
}
.ui-resizable-w {
	cursor: w-resize;
	width: 7px;
	left: -5px;
	top: 0;
	height: 100%;
}
.ui-resizable-se {
	cursor: se-resize;
	width: 12px;
	height: 12px;
	right: 1px;
	bottom: 1px;
}
.ui-resizable-sw {
	cursor: sw-resize;
	width: 9px;
	height: 9px;
	left: -5px;
	bottom: -5px;
}
.ui-resizable-nw {
	cursor: nw-resize;
	width: 9px;
	height: 9px;
	left: -5px;
	top: -5px;
}
.ui-resizable-ne {
	cursor: ne-resize;
	width: 9px;
	height: 9px;
	right: -5px;
	top: -5px;
}
.ui-progressbar {
	height: 2em;
	text-align: left;
	overflow: hidden;
}
.ui-progressbar .ui-progressbar-value {
	margin: -1px;
	height: 100%;
}
.ui-progressbar .ui-progressbar-overlay {
	background: url("data:image/gif;base64,R0lGODlhKAAoAIABAAAAAP///yH/C05FVFNDQVBFMi4wAwEAAAAh+QQJAQABACwAAAAAKAAoAAACkYwNqXrdC52DS06a7MFZI+4FHBCKoDeWKXqymPqGqxvJrXZbMx7Ttc+w9XgU2FB3lOyQRWET2IFGiU9m1frDVpxZZc6bfHwv4c1YXP6k1Vdy292Fb6UkuvFtXpvWSzA+HycXJHUXiGYIiMg2R6W459gnWGfHNdjIqDWVqemH2ekpObkpOlppWUqZiqr6edqqWQAAIfkECQEAAQAsAAAAACgAKAAAApSMgZnGfaqcg1E2uuzDmmHUBR8Qil95hiPKqWn3aqtLsS18y7G1SzNeowWBENtQd+T1JktP05nzPTdJZlR6vUxNWWjV+vUWhWNkWFwxl9VpZRedYcflIOLafaa28XdsH/ynlcc1uPVDZxQIR0K25+cICCmoqCe5mGhZOfeYSUh5yJcJyrkZWWpaR8doJ2o4NYq62lAAACH5BAkBAAEALAAAAAAoACgAAAKVDI4Yy22ZnINRNqosw0Bv7i1gyHUkFj7oSaWlu3ovC8GxNso5fluz3qLVhBVeT/Lz7ZTHyxL5dDalQWPVOsQWtRnuwXaFTj9jVVh8pma9JjZ4zYSj5ZOyma7uuolffh+IR5aW97cHuBUXKGKXlKjn+DiHWMcYJah4N0lYCMlJOXipGRr5qdgoSTrqWSq6WFl2ypoaUAAAIfkECQEAAQAsAAAAACgAKAAAApaEb6HLgd/iO7FNWtcFWe+ufODGjRfoiJ2akShbueb0wtI50zm02pbvwfWEMWBQ1zKGlLIhskiEPm9R6vRXxV4ZzWT2yHOGpWMyorblKlNp8HmHEb/lCXjcW7bmtXP8Xt229OVWR1fod2eWqNfHuMjXCPkIGNileOiImVmCOEmoSfn3yXlJWmoHGhqp6ilYuWYpmTqKUgAAIfkECQEAAQAsAAAAACgAKAAAApiEH6kb58biQ3FNWtMFWW3eNVcojuFGfqnZqSebuS06w5V80/X02pKe8zFwP6EFWOT1lDFk8rGERh1TTNOocQ61Hm4Xm2VexUHpzjymViHrFbiELsefVrn6XKfnt2Q9G/+Xdie499XHd2g4h7ioOGhXGJboGAnXSBnoBwKYyfioubZJ2Hn0RuRZaflZOil56Zp6iioKSXpUAAAh+QQJAQABACwAAAAAKAAoAAACkoQRqRvnxuI7kU1a1UU5bd5tnSeOZXhmn5lWK3qNTWvRdQxP8qvaC+/yaYQzXO7BMvaUEmJRd3TsiMAgswmNYrSgZdYrTX6tSHGZO73ezuAw2uxuQ+BbeZfMxsexY35+/Qe4J1inV0g4x3WHuMhIl2jXOKT2Q+VU5fgoSUI52VfZyfkJGkha6jmY+aaYdirq+lQAACH5BAkBAAEALAAAAAAoACgAAAKWBIKpYe0L3YNKToqswUlvznigd4wiR4KhZrKt9Upqip61i9E3vMvxRdHlbEFiEXfk9YARYxOZZD6VQ2pUunBmtRXo1Lf8hMVVcNl8JafV38aM2/Fu5V16Bn63r6xt97j09+MXSFi4BniGFae3hzbH9+hYBzkpuUh5aZmHuanZOZgIuvbGiNeomCnaxxap2upaCZsq+1kAACH5BAkBAAEALAAAAAAoACgAAAKXjI8By5zf4kOxTVrXNVlv1X0d8IGZGKLnNpYtm8Lr9cqVeuOSvfOW79D9aDHizNhDJidFZhNydEahOaDH6nomtJjp1tutKoNWkvA6JqfRVLHU/QUfau9l2x7G54d1fl995xcIGAdXqMfBNadoYrhH+Mg2KBlpVpbluCiXmMnZ2Sh4GBqJ+ckIOqqJ6LmKSllZmsoq6wpQAAAh+QQJAQABACwAAAAAKAAoAAAClYx/oLvoxuJDkU1a1YUZbJ59nSd2ZXhWqbRa2/gF8Gu2DY3iqs7yrq+xBYEkYvFSM8aSSObE+ZgRl1BHFZNr7pRCavZ5BW2142hY3AN/zWtsmf12p9XxxFl2lpLn1rseztfXZjdIWIf2s5dItwjYKBgo9yg5pHgzJXTEeGlZuenpyPmpGQoKOWkYmSpaSnqKileI2FAAACH5BAkBAAEALAAAAAAoACgAAAKVjB+gu+jG4kORTVrVhRlsnn2dJ3ZleFaptFrb+CXmO9OozeL5VfP99HvAWhpiUdcwkpBH3825AwYdU8xTqlLGhtCosArKMpvfa1mMRae9VvWZfeB2XfPkeLmm18lUcBj+p5dnN8jXZ3YIGEhYuOUn45aoCDkp16hl5IjYJvjWKcnoGQpqyPlpOhr3aElaqrq56Bq7VAAAOw==");
	height: 100%;
	filter: alpha(opacity=25); 
	opacity: 0.25;
}
.ui-progressbar-indeterminate .ui-progressbar-value {
	background-image: none;
}
.ui-selectable {
	-ms-touch-action: none;
	touch-action: none;
}
.ui-selectable-helper {
	position: absolute;
	z-index: 100;
	border: 1px dotted black;
}
.ui-selectmenu-menu {
	padding: 0;
	margin: 0;
	position: absolute;
	top: 0;
	left: 0;
	display: none;
}
.ui-selectmenu-menu .ui-menu {
	overflow: auto;
	overflow-x: hidden;
	padding-bottom: 1px;
}
.ui-selectmenu-menu .ui-menu .ui-selectmenu-optgroup {
	font-size: 1em;
	font-weight: bold;
	line-height: 1.5;
	padding: 2px 0.4em;
	margin: 0.5em 0 0 0;
	height: auto;
	border: 0;
}
.ui-selectmenu-open {
	display: block;
}
.ui-selectmenu-text {
	display: block;
	margin-right: 20px;
	overflow: hidden;
	text-overflow: ellipsis;
}
.ui-selectmenu-button.ui-button {
	text-align: left;
	white-space: nowrap;
	width: 14em;
}
.ui-selectmenu-icon.ui-icon {
	float: right;
	margin-top: 0;
}
.ui-slider {
	position: relative;
	text-align: left;
}
.ui-slider .ui-slider-handle {
	position: absolute;
	z-index: 2;
	width: 1.2em;
	height: 1.2em;
	cursor: default;
	-ms-touch-action: none;
	touch-action: none;
}
.ui-slider .ui-slider-range {
	position: absolute;
	z-index: 1;
	font-size: .7em;
	display: block;
	border: 0;
	background-position: 0 0;
}


.ui-slider.ui-state-disabled .ui-slider-handle,
.ui-slider.ui-state-disabled .ui-slider-range {
	filter: inherit;
}

.ui-slider-horizontal {
	height: .8em;
}
.ui-slider-horizontal .ui-slider-handle {
	top: -.3em;
	margin-left: -.6em;
}
.ui-slider-horizontal .ui-slider-range {
	top: 0;
	height: 100%;
}
.ui-slider-horizontal .ui-slider-range-min {
	left: 0;
}
.ui-slider-horizontal .ui-slider-range-max {
	right: 0;
}

.ui-slider-vertical {
	width: .8em;
	height: 100px;
}
.ui-slider-vertical .ui-slider-handle {
	left: -.3em;
	margin-left: 0;
	margin-bottom: -.6em;
}
.ui-slider-vertical .ui-slider-range {
	left: 0;
	width: 100%;
}
.ui-slider-vertical .ui-slider-range-min {
	bottom: 0;
}
.ui-slider-vertical .ui-slider-range-max {
	top: 0;
}
.ui-sortable-handle {
	-ms-touch-action: none;
	touch-action: none;
}
.ui-spinner {
	position: relative;
	display: inline-block;
	overflow: hidden;
	padding: 0;
	vertical-align: middle;
}
.ui-spinner-input {
	border: none;
	background: none;
	color: inherit;
	padding: .222em 0;
	margin: .2em 0;
	vertical-align: middle;
	margin-left: .4em;
	margin-right: 2em;
}
.ui-spinner-button {
	width: 1.6em;
	height: 50%;
	font-size: .5em;
	padding: 0;
	margin: 0;
	text-align: center;
	position: absolute;
	cursor: default;
	display: block;
	overflow: hidden;
	right: 0;
}

.ui-spinner a.ui-spinner-button {
	border-top-style: none;
	border-bottom-style: none;
	border-right-style: none;
}
.ui-spinner-up {
	top: 0;
}
.ui-spinner-down {
	bottom: 0;
}
.ui-tabs {
	position: relative;
	padding: .2em;
}
.ui-tabs .ui-tabs-nav {
	margin: 0;
	padding: .2em .2em 0;
}
.ui-tabs .ui-tabs-nav li {
	list-style: none;
	float: left;
	position: relative;
	top: 0;
	margin: 1px .2em 0 0;
	border-bottom-width: 0;
	padding: 0;
	white-space: nowrap;
}
.ui-tabs .ui-tabs-nav .ui-tabs-anchor {
	float: left;
	padding: .5em 1em;
	text-decoration: none;
}
.ui-tabs .ui-tabs-nav li.ui-tabs-active {
	margin-bottom: -1px;
	padding-bottom: 1px;
}
.ui-tabs .ui-tabs-nav li.ui-tabs-active .ui-tabs-anchor,
.ui-tabs .ui-tabs-nav li.ui-state-disabled .ui-tabs-anchor,
.ui-tabs .ui-tabs-nav li.ui-tabs-loading .ui-tabs-anchor {
	cursor: text;
}
.ui-tabs-collapsible .ui-tabs-nav li.ui-tabs-active .ui-tabs-anchor {
	cursor: pointer;
}
.ui-tabs .ui-tabs-panel {
	display: block;
	border-width: 0;
	padding: 1em 1.4em;
	background: none;
}
.ui-tooltip {
	padding: 8px;
	position: absolute;
	z-index: 9999;
	max-width: 300px;
}
body .ui-tooltip {
	border-width: 2px;
}

.ui-widget {
	font-family: Arial,Helvetica,sans-serif;
	font-size: 1em;
}
.ui-widget .ui-widget {
	font-size: 1em;
}
.ui-widget input,
.ui-widget select,
.ui-widget textarea,
.ui-widget button {
	font-family: Arial,Helvetica,sans-serif;
	font-size: 1em;
}
.ui-widget.ui-widget-content {
	border: 1px solid #c5c5c5;
}
.ui-widget-content {
	border: 1px solid #dddddd;
	background: #ffffff;
	color: #333333;
}
.ui-widget-content a {
	color: #333333;
}
.ui-widget-header {
	border: 1px solid #dddddd;
	background: #e9e9e9;
	color: #333333;
	font-weight: bold;
}
.ui-widget-header a {
	color: #333333;
}


.ui-state-default,
.ui-widget-content .ui-state-default,
.ui-widget-header .ui-state-default,
.ui-button,


html .ui-button.ui-state-disabled:hover,
html .ui-button.ui-state-disabled:active {
	border: 1px solid #c5c5c5;
	background: #f6f6f6;
	font-weight: normal;
	color: #454545;
}
.ui-state-default a,
.ui-state-default a:link,
.ui-state-default a:visited,
a.ui-button,
a:link.ui-button,
a:visited.ui-button,
.ui-button {
	color: #454545;
	text-decoration: none;
}
.ui-state-hover,
.ui-widget-content .ui-state-hover,
.ui-widget-header .ui-state-hover,
.ui-state-focus,
.ui-widget-content .ui-state-focus,
.ui-widget-header .ui-state-focus,
.ui-button:hover,
.ui-button:focus {
	border: 1px solid #cccccc;
	background: #ededed;
	font-weight: normal;
	color: #2b2b2b;
}
.ui-state-hover a,
.ui-state-hover a:hover,
.ui-state-hover a:link,
.ui-state-hover a:visited,
.ui-state-focus a,
.ui-state-focus a:hover,
.ui-state-focus a:link,
.ui-state-focus a:visited,
a.ui-button:hover,
a.ui-button:focus {
	color: #2b2b2b;
	text-decoration: none;
}

.ui-visual-focus {
	box-shadow: 0 0 3px 1px rgb(94, 158, 214);
}
.ui-state-active,
.ui-widget-content .ui-state-active,
.ui-widget-header .ui-state-active,
a.ui-button:active,
.ui-button:active,
.ui-button.ui-state-active:hover {
	border: 1px solid #003eff;
	background: #007fff;
	font-weight: normal;
	color: #ffffff;
}
.ui-icon-background,
.ui-state-active .ui-icon-background {
	border: #003eff;
	background-color: #ffffff;
}
.ui-state-active a,
.ui-state-active a:link,
.ui-state-active a:visited {
	color: #ffffff;
	text-decoration: none;
}


.ui-state-highlight,
.ui-widget-content .ui-state-highlight,
.ui-widget-header .ui-state-highlight {
	border: 1px solid #dad55e;
	background: #fffa90;
	color: #777620;
}
.ui-state-checked {
	border: 1px solid #dad55e;
	background: #fffa90;
}
.ui-state-highlight a,
.ui-widget-content .ui-state-highlight a,
.ui-widget-header .ui-state-highlight a {
	color: #777620;
}
.ui-state-error,
.ui-widget-content .ui-state-error,
.ui-widget-header .ui-state-error {
	border: 1px solid #f1a899;
	background: #fddfdf;
	color: #5f3f3f;
}
.ui-state-error a,
.ui-widget-content .ui-state-error a,
.ui-widget-header .ui-state-error a {
	color: #5f3f3f;
}
.ui-state-error-text,
.ui-widget-content .ui-state-error-text,
.ui-widget-header .ui-state-error-text {
	color: #5f3f3f;
}
.ui-priority-primary,
.ui-widget-content .ui-priority-primary,
.ui-widget-header .ui-priority-primary {
	font-weight: bold;
}
.ui-priority-secondary,
.ui-widget-content .ui-priority-secondary,
.ui-widget-header .ui-priority-secondary {
	opacity: .7;
	filter:Alpha(Opacity=70); 
	font-weight: normal;
}
.ui-state-disabled,
.ui-widget-content .ui-state-disabled,
.ui-widget-header .ui-state-disabled {
	opacity: .35;
	filter:Alpha(Opacity=35); 
	background-image: none;
}
.ui-state-disabled .ui-icon {
	filter:Alpha(Opacity=35); 
}




.ui-icon {
	width: 16px;
	height: 16px;
}
.ui-icon,
.ui-widget-content .ui-icon {
	background-image: url("images/ui-icons_444444_256x240.png");
}
.ui-widget-header .ui-icon {
	background-image: url("images/ui-icons_444444_256x240.png");
}
.ui-state-hover .ui-icon,
.ui-state-focus .ui-icon,
.ui-button:hover .ui-icon,
.ui-button:focus .ui-icon {
	background-image: url("images/ui-icons_555555_256x240.png");
}
.ui-state-active .ui-icon,
.ui-button:active .ui-icon {
	background-image: url("images/ui-icons_ffffff_256x240.png");
}
.ui-state-highlight .ui-icon,
.ui-button .ui-state-highlight.ui-icon {
	background-image: url("images/ui-icons_777620_256x240.png");
}
.ui-state-error .ui-icon,
.ui-state-error-text .ui-icon {
	background-image: url("images/ui-icons_cc0000_256x240.png");
}
.ui-button .ui-icon {
	background-image: url("images/ui-icons_777777_256x240.png");
}


.ui-icon-blank { background-position: 16px 16px; }
.ui-icon-caret-1-n { background-position: 0 0; }
.ui-icon-caret-1-ne { background-position: -16px 0; }
.ui-icon-caret-1-e { background-position: -32px 0; }
.ui-icon-caret-1-se { background-position: -48px 0; }
.ui-icon-caret-1-s { background-position: -65px 0; }
.ui-icon-caret-1-sw { background-position: -80px 0; }
.ui-icon-caret-1-w { background-position: -96px 0; }
.ui-icon-caret-1-nw { background-position: -112px 0; }
.ui-icon-caret-2-n-s { background-position: -128px 0; }
.ui-icon-caret-2-e-w { background-position: -144px 0; }
.ui-icon-triangle-1-n { background-position: 0 -16px; }
.ui-icon-triangle-1-ne { background-position: -16px -16px; }
.ui-icon-triangle-1-e { background-position: -32px -16px; }
.ui-icon-triangle-1-se { background-position: -48px -16px; }
.ui-icon-triangle-1-s { background-position: -65px -16px; }
.ui-icon-triangle-1-sw { background-position: -80px -16px; }
.ui-icon-triangle-1-w { background-position: -96px -16px; }
.ui-icon-triangle-1-nw { background-position: -112px -16px; }
.ui-icon-triangle-2-n-s { background-position: -128px -16px; }
.ui-icon-triangle-2-e-w { background-position: -144px -16px; }
.ui-icon-arrow-1-n { background-position: 0 -32px; }
.ui-icon-arrow-1-ne { background-position: -16px -32px; }
.ui-icon-arrow-1-e { background-position: -32px -32px; }
.ui-icon-arrow-1-se { background-position: -48px -32px; }
.ui-icon-arrow-1-s { background-position: -65px -32px; }
.ui-icon-arrow-1-sw { background-position: -80px -32px; }
.ui-icon-arrow-1-w { background-position: -96px -32px; }
.ui-icon-arrow-1-nw { background-position: -112px -32px; }
.ui-icon-arrow-2-n-s { background-position: -128px -32px; }
.ui-icon-arrow-2-ne-sw { background-position: -144px -32px; }
.ui-icon-arrow-2-e-w { background-position: -160px -32px; }
.ui-icon-arrow-2-se-nw { background-position: -176px -32px; }
.ui-icon-arrowstop-1-n { background-position: -192px -32px; }
.ui-icon-arrowstop-1-e { background-position: -208px -32px; }
.ui-icon-arrowstop-1-s { background-position: -224px -32px; }
.ui-icon-arrowstop-1-w { background-position: -240px -32px; }
.ui-icon-arrowthick-1-n { background-position: 1px -48px; }
.ui-icon-arrowthick-1-ne { background-position: -16px -48px; }
.ui-icon-arrowthick-1-e { background-position: -32px -48px; }
.ui-icon-arrowthick-1-se { background-position: -48px -48px; }
.ui-icon-arrowthick-1-s { background-position: -64px -48px; }
.ui-icon-arrowthick-1-sw { background-position: -80px -48px; }
.ui-icon-arrowthick-1-w { background-position: -96px -48px; }
.ui-icon-arrowthick-1-nw { background-position: -112px -48px; }
.ui-icon-arrowthick-2-n-s { background-position: -128px -48px; }
.ui-icon-arrowthick-2-ne-sw { background-position: -144px -48px; }
.ui-icon-arrowthick-2-e-w { background-position: -160px -48px; }
.ui-icon-arrowthick-2-se-nw { background-position: -176px -48px; }
.ui-icon-arrowthickstop-1-n { background-position: -192px -48px; }
.ui-icon-arrowthickstop-1-e { background-position: -208px -48px; }
.ui-icon-arrowthickstop-1-s { background-position: -224px -48px; }
.ui-icon-arrowthickstop-1-w { background-position: -240px -48px; }
.ui-icon-arrowreturnthick-1-w { background-position: 0 -64px; }
.ui-icon-arrowreturnthick-1-n { background-position: -16px -64px; }
.ui-icon-arrowreturnthick-1-e { background-position: -32px -64px; }
.ui-icon-arrowreturnthick-1-s { background-position: -48px -64px; }
.ui-icon-arrowreturn-1-w { background-position: -64px -64px; }
.ui-icon-arrowreturn-1-n { background-position: -80px -64px; }
.ui-icon-arrowreturn-1-e { background-position: -96px -64px; }
.ui-icon-arrowreturn-1-s { background-position: -112px -64px; }
.ui-icon-arrowrefresh-1-w { background-position: -128px -64px; }
.ui-icon-arrowrefresh-1-n { background-position: -144px -64px; }
.ui-icon-arrowrefresh-1-e { background-position: -160px -64px; }
.ui-icon-arrowrefresh-1-s { background-position: -176px -64px; }
.ui-icon-arrow-4 { background-position: 0 -80px; }
.ui-icon-arrow-4-diag { background-position: -16px -80px; }
.ui-icon-extlink { background-position: -32px -80px; }
.ui-icon-newwin { background-position: -48px -80px; }
.ui-icon-refresh { background-position: -64px -80px; }
.ui-icon-shuffle { background-position: -80px -80px; }
.ui-icon-transfer-e-w { background-position: -96px -80px; }
.ui-icon-transferthick-e-w { background-position: -112px -80px; }
.ui-icon-folder-collapsed { background-position: 0 -96px; }
.ui-icon-folder-open { background-position: -16px -96px; }
.ui-icon-document { background-position: -32px -96px; }
.ui-icon-document-b { background-position: -48px -96px; }
.ui-icon-note { background-position: -64px -96px; }
.ui-icon-mail-closed { background-position: -80px -96px; }
.ui-icon-mail-open { background-position: -96px -96px; }
.ui-icon-suitcase { background-position: -112px -96px; }
.ui-icon-comment { background-position: -128px -96px; }
.ui-icon-person { background-position: -144px -96px; }
.ui-icon-print { background-position: -160px -96px; }
.ui-icon-trash { background-position: -176px -96px; }
.ui-icon-locked { background-position: -192px -96px; }
.ui-icon-unlocked { background-position: -208px -96px; }
.ui-icon-bookmark { background-position: -224px -96px; }
.ui-icon-tag { background-position: -240px -96px; }
.ui-icon-home { background-position: 0 -112px; }
.ui-icon-flag { background-position: -16px -112px; }
.ui-icon-calendar { background-position: -32px -112px; }
.ui-icon-cart { background-position: -48px -112px; }
.ui-icon-pencil { background-position: -64px -112px; }
.ui-icon-clock { background-position: -80px -112px; }
.ui-icon-disk { background-position: -96px -112px; }
.ui-icon-calculator { background-position: -112px -112px; }
.ui-icon-zoomin { background-position: -128px -112px; }
.ui-icon-zoomout { background-position: -144px -112px; }
.ui-icon-search { background-position: -160px -112px; }
.ui-icon-wrench { background-position: -176px -112px; }
.ui-icon-gear { background-position: -192px -112px; }
.ui-icon-heart { background-position: -208px -112px; }
.ui-icon-star { background-position: -224px -112px; }
.ui-icon-link { background-position: -240px -112px; }
.ui-icon-cancel { background-position: 0 -128px; }
.ui-icon-plus { background-position: -16px -128px; }
.ui-icon-plusthick { background-position: -32px -128px; }
.ui-icon-minus { background-position: -48px -128px; }
.ui-icon-minusthick { background-position: -64px -128px; }
.ui-icon-close { background-position: -80px -128px; }
.ui-icon-closethick { background-position: -96px -128px; }
.ui-icon-key { background-position: -112px -128px; }
.ui-icon-lightbulb { background-position: -128px -128px; }
.ui-icon-scissors { background-position: -144px -128px; }
.ui-icon-clipboard { background-position: -160px -128px; }
.ui-icon-copy { background-position: -176px -128px; }
.ui-icon-contact { background-position: -192px -128px; }
.ui-icon-image { background-position: -208px -128px; }
.ui-icon-video { background-position: -224px -128px; }
.ui-icon-script { background-position: -240px -128px; }
.ui-icon-alert { background-position: 0 -144px; }
.ui-icon-info { background-position: -16px -144px; }
.ui-icon-notice { background-position: -32px -144px; }
.ui-icon-help { background-position: -48px -144px; }
.ui-icon-check { background-position: -64px -144px; }
.ui-icon-bullet { background-position: -80px -144px; }
.ui-icon-radio-on { background-position: -96px -144px; }
.ui-icon-radio-off { background-position: -112px -144px; }
.ui-icon-pin-w { background-position: -128px -144px; }
.ui-icon-pin-s { background-position: -144px -144px; }
.ui-icon-play { background-position: 0 -160px; }
.ui-icon-pause { background-position: -16px -160px; }
.ui-icon-seek-next { background-position: -32px -160px; }
.ui-icon-seek-prev { background-position: -48px -160px; }
.ui-icon-seek-end { background-position: -64px -160px; }
.ui-icon-seek-start { background-position: -80px -160px; }

.ui-icon-seek-first { background-position: -80px -160px; }
.ui-icon-stop { background-position: -96px -160px; }
.ui-icon-eject { background-position: -112px -160px; }
.ui-icon-volume-off { background-position: -128px -160px; }
.ui-icon-volume-on { background-position: -144px -160px; }
.ui-icon-power { background-position: 0 -176px; }
.ui-icon-signal-diag { background-position: -16px -176px; }
.ui-icon-signal { background-position: -32px -176px; }
.ui-icon-battery-0 { background-position: -48px -176px; }
.ui-icon-battery-1 { background-position: -64px -176px; }
.ui-icon-battery-2 { background-position: -80px -176px; }
.ui-icon-battery-3 { background-position: -96px -176px; }
.ui-icon-circle-plus { background-position: 0 -192px; }
.ui-icon-circle-minus { background-position: -16px -192px; }
.ui-icon-circle-close { background-position: -32px -192px; }
.ui-icon-circle-triangle-e { background-position: -48px -192px; }
.ui-icon-circle-triangle-s { background-position: -64px -192px; }
.ui-icon-circle-triangle-w { background-position: -80px -192px; }
.ui-icon-circle-triangle-n { background-position: -96px -192px; }
.ui-icon-circle-arrow-e { background-position: -112px -192px; }
.ui-icon-circle-arrow-s { background-position: -128px -192px; }
.ui-icon-circle-arrow-w { background-position: -144px -192px; }
.ui-icon-circle-arrow-n { background-position: -160px -192px; }
.ui-icon-circle-zoomin { background-position: -176px -192px; }
.ui-icon-circle-zoomout { background-position: -192px -192px; }
.ui-icon-circle-check { background-position: -208px -192px; }
.ui-icon-circlesmall-plus { background-position: 0 -208px; }
.ui-icon-circlesmall-minus { background-position: -16px -208px; }
.ui-icon-circlesmall-close { background-position: -32px -208px; }
.ui-icon-squaresmall-plus { background-position: -48px -208px; }
.ui-icon-squaresmall-minus { background-position: -64px -208px; }
.ui-icon-squaresmall-close { background-position: -80px -208px; }
.ui-icon-grip-dotted-vertical { background-position: 0 -224px; }
.ui-icon-grip-dotted-horizontal { background-position: -16px -224px; }
.ui-icon-grip-solid-vertical { background-position: -32px -224px; }
.ui-icon-grip-solid-horizontal { background-position: -48px -224px; }
.ui-icon-gripsmall-diagonal-se { background-position: -64px -224px; }
.ui-icon-grip-diagonal-se { background-position: -80px -224px; }





.ui-corner-all,
.ui-corner-top,
.ui-corner-left,
.ui-corner-tl {
	border-top-left-radius: 3px;
}
.ui-corner-all,
.ui-corner-top,
.ui-corner-right,
.ui-corner-tr {
	border-top-right-radius: 3px;
}
.ui-corner-all,
.ui-corner-bottom,
.ui-corner-left,
.ui-corner-bl {
	border-bottom-left-radius: 3px;
}
.ui-corner-all,
.ui-corner-bottom,
.ui-corner-right,
.ui-corner-br {
	border-bottom-right-radius: 3px;
}


.ui-widget-overlay {
	background: #aaaaaa;
	opacity: .3;
	filter: Alpha(Opacity=30); 
}
.ui-widget-shadow {
	-webkit-box-shadow: 0px 0px 5px #666666;
	box-shadow: 0px 0px 5px #666666;
} 
</style>
<script src='js/jquery-1.12.4.js'></script>
<script src='js/jquery-ui.js'></script>

<script>
$( function() {
	$( '#tabs-collect-classes-from-hierarchical-partition' ).tabs();
} );
</script>
<div id='tabs-collect-classes-from-hierarchical-partition'>
<ul>
<li><a href='#tab-collect-classes-from-hierarchical-partition-1'>n_signatures ≥ 1432</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-2'>n_signatures ≥ 1449</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-3'>n_signatures ≥ 2070</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-4'>n_signatures ≥ 3429</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-5'>n_signatures ≥ 3489</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-6'>n_signatures ≥ 4028</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-7'>n_signatures ≥ 9255</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-8'>n_signatures ≥ 10873</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-9'>n_signatures ≥ 13097</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-10'>n_signatures ≥ 16138</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-11'>n_signatures ≥ 18356</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-12'>n_signatures ≥ 34722</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-13'>n_signatures ≥ 37386</a></li>
<li><a href='#tab-collect-classes-from-hierarchical-partition-14'>n_signatures ≥ 67663</a></li>
</ul>
<div id='tab-collect-classes-from-hierarchical-partition-1'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 1432))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-1-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-1"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-2'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 1449))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-2-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-2"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-3'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 2070))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-3-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-3"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-4'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 3429))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-4-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-4"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-5'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 3489))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-5-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-5"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-6'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 4028))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-6-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-6"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-7'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 9255))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-7-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-7"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-8'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 10873))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-8-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-8"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-9'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 13097))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-9-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-9"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-10'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 16138))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-10-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-10"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-11'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 18356))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-11-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-11"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-12'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 34722))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-12-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-12"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-13'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 37386))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-13-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-13"/></p>

</div>
<div id='tab-collect-classes-from-hierarchical-partition-14'>
<pre><code class="r">collect_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 67663))
</code></pre>

<p><img src="figure_cola/tab-collect-classes-from-hierarchical-partition-14-1.png" alt="plot of chunk tab-collect-classes-from-hierarchical-partition-14"/></p>

</div>
</div>

Following shows the table of the partitions (You need to click the **show/hide
code output** link to see it).


<script>
$( function() {
	$( '#tabs-get-classes-from-hierarchical-partition' ).tabs();
} );
</script>
<div id='tabs-get-classes-from-hierarchical-partition'>
<ul>
<li><a href='#tab-get-classes-from-hierarchical-partition-1'>n_signatures ≥ 1432</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-2'>n_signatures ≥ 1449</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-3'>n_signatures ≥ 2070</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-4'>n_signatures ≥ 3429</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-5'>n_signatures ≥ 3489</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-6'>n_signatures ≥ 4028</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-7'>n_signatures ≥ 9255</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-8'>n_signatures ≥ 10873</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-9'>n_signatures ≥ 13097</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-10'>n_signatures ≥ 16138</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-11'>n_signatures ≥ 18356</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-12'>n_signatures ≥ 34722</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-13'>n_signatures ≥ 37386</a></li>
<li><a href='#tab-get-classes-from-hierarchical-partition-14'>n_signatures ≥ 67663</a></li>
</ul>

<div id='tab-get-classes-from-hierarchical-partition-1'>
<p><a id='tab-get-classes-from-hierarchical-partition-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 1432))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;          &quot;0122&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;          &quot;0133&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;          &quot;0121&quot;         &quot;02222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;         &quot;02223&quot;          &quot;0132&quot;          &quot;0132&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;          &quot;0121&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;          &quot;0121&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;          &quot;0231&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;          &quot;0122&quot;          &quot;0121&quot;           &quot;053&quot;          &quot;0233&quot;           &quot;031&quot;          &quot;0122&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;          &quot;0131&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;          &quot;0123&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;          &quot;0123&quot;          &quot;0212&quot;          &quot;0121&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;          &quot;0131&quot;          &quot;0111&quot;          &quot;0232&quot;          &quot;0132&quot;          &quot;0121&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;          &quot;0133&quot;        &quot;022212&quot;          &quot;0112&quot;          &quot;0132&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;          &quot;0133&quot;           &quot;033&quot;          &quot;0123&quot;          &quot;0112&quot;           &quot;053&quot;          &quot;0132&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;          &quot;0231&quot;           &quot;041&quot;           &quot;033&quot;          &quot;0231&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;          &quot;0231&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;           &quot;042&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;         &quot;02223&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;          &quot;0121&quot;          &quot;0231&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;        &quot;022212&quot;          &quot;0223&quot;          &quot;0131&quot;          &quot;0123&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;         &quot;02223&quot;        &quot;022212&quot;         &quot;02223&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;         &quot;02222&quot;           &quot;042&quot;          &quot;0231&quot;        &quot;022211&quot;        &quot;022211&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;          &quot;0121&quot;          &quot;0232&quot;          &quot;0211&quot;           &quot;034&quot;          &quot;0121&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;        &quot;022211&quot;          &quot;0131&quot;          &quot;0121&quot;          &quot;0112&quot;          &quot;0223&quot;          &quot;0122&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;          &quot;0122&quot;          &quot;0112&quot;          &quot;0212&quot;           &quot;042&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;          &quot;0133&quot;        &quot;022212&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;          &quot;0133&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;           &quot;042&quot;          &quot;0123&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;          &quot;0233&quot;        &quot;022211&quot;         &quot;02222&quot;           &quot;052&quot;           &quot;043&quot;           &quot;042&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;          &quot;0131&quot;         &quot;02222&quot;          &quot;0111&quot;           &quot;043&quot;        &quot;022211&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;         &quot;02222&quot;          &quot;0212&quot;          &quot;0232&quot;          &quot;0211&quot;         &quot;02222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;          &quot;0131&quot;          &quot;0223&quot;         &quot;02222&quot;        &quot;022211&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;          &quot;0133&quot;         &quot;02222&quot;          &quot;0221&quot;           &quot;043&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;           &quot;041&quot;          &quot;0232&quot;          &quot;0133&quot;          &quot;0231&quot;        &quot;022211&quot;          &quot;0132&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;          &quot;0233&quot;           &quot;041&quot;          &quot;0133&quot;          &quot;0131&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;          &quot;0132&quot;          &quot;0221&quot;         &quot;02223&quot;           &quot;043&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;        &quot;022211&quot;          &quot;0221&quot;           &quot;042&quot;           &quot;041&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-1-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-1-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-2'>
<p><a id='tab-get-classes-from-hierarchical-partition-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 1449))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;          &quot;0122&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;          &quot;0133&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;          &quot;0121&quot;         &quot;02222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;         &quot;02223&quot;          &quot;0132&quot;          &quot;0132&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;          &quot;0121&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;          &quot;0121&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;          &quot;0231&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;          &quot;0122&quot;          &quot;0121&quot;           &quot;053&quot;          &quot;0233&quot;           &quot;031&quot;          &quot;0122&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;          &quot;0131&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;          &quot;0123&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;          &quot;0123&quot;          &quot;0212&quot;          &quot;0121&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;          &quot;0131&quot;          &quot;0111&quot;          &quot;0232&quot;          &quot;0132&quot;          &quot;0121&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;          &quot;0133&quot;         &quot;02221&quot;          &quot;0112&quot;          &quot;0132&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;          &quot;0133&quot;           &quot;033&quot;          &quot;0123&quot;          &quot;0112&quot;           &quot;053&quot;          &quot;0132&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;          &quot;0231&quot;           &quot;041&quot;           &quot;033&quot;          &quot;0231&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;          &quot;0231&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;           &quot;042&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;         &quot;02223&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;          &quot;0121&quot;          &quot;0231&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;         &quot;02221&quot;          &quot;0223&quot;          &quot;0131&quot;          &quot;0123&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;         &quot;02223&quot;         &quot;02221&quot;         &quot;02223&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;         &quot;02222&quot;           &quot;042&quot;          &quot;0231&quot;         &quot;02221&quot;         &quot;02221&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;          &quot;0121&quot;          &quot;0232&quot;          &quot;0211&quot;           &quot;034&quot;          &quot;0121&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;         &quot;02221&quot;          &quot;0131&quot;          &quot;0121&quot;          &quot;0112&quot;          &quot;0223&quot;          &quot;0122&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;          &quot;0122&quot;          &quot;0112&quot;          &quot;0212&quot;           &quot;042&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;          &quot;0133&quot;         &quot;02221&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;          &quot;0133&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;           &quot;042&quot;          &quot;0123&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;          &quot;0233&quot;         &quot;02221&quot;         &quot;02222&quot;           &quot;052&quot;           &quot;043&quot;           &quot;042&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;          &quot;0131&quot;         &quot;02222&quot;          &quot;0111&quot;           &quot;043&quot;         &quot;02221&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;         &quot;02222&quot;          &quot;0212&quot;          &quot;0232&quot;          &quot;0211&quot;         &quot;02222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;          &quot;0131&quot;          &quot;0223&quot;         &quot;02222&quot;         &quot;02221&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;          &quot;0133&quot;         &quot;02222&quot;          &quot;0221&quot;           &quot;043&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;           &quot;041&quot;          &quot;0232&quot;          &quot;0133&quot;          &quot;0231&quot;         &quot;02221&quot;          &quot;0132&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;          &quot;0233&quot;           &quot;041&quot;          &quot;0133&quot;          &quot;0131&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;          &quot;0132&quot;          &quot;0221&quot;         &quot;02223&quot;           &quot;043&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;         &quot;02221&quot;          &quot;0221&quot;           &quot;042&quot;           &quot;041&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-2-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-2-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-3'>
<p><a id='tab-get-classes-from-hierarchical-partition-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 2070))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;          &quot;0133&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;           &quot;012&quot;         &quot;02222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;         &quot;02223&quot;          &quot;0132&quot;          &quot;0132&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;          &quot;0231&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;          &quot;0233&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;          &quot;0131&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;          &quot;0212&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;          &quot;0131&quot;          &quot;0111&quot;          &quot;0232&quot;          &quot;0132&quot;           &quot;012&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;          &quot;0133&quot;         &quot;02221&quot;          &quot;0112&quot;          &quot;0132&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;          &quot;0133&quot;           &quot;033&quot;           &quot;012&quot;          &quot;0112&quot;           &quot;053&quot;          &quot;0132&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;          &quot;0231&quot;           &quot;041&quot;           &quot;033&quot;          &quot;0231&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;          &quot;0231&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;           &quot;042&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;         &quot;02223&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;           &quot;012&quot;          &quot;0231&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;         &quot;02221&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;         &quot;02223&quot;         &quot;02221&quot;         &quot;02223&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;         &quot;02222&quot;           &quot;042&quot;          &quot;0231&quot;         &quot;02221&quot;         &quot;02221&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;          &quot;0232&quot;          &quot;0211&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;         &quot;02221&quot;          &quot;0131&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0212&quot;           &quot;042&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;          &quot;0133&quot;         &quot;02221&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;          &quot;0133&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;           &quot;042&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;          &quot;0233&quot;         &quot;02221&quot;         &quot;02222&quot;           &quot;052&quot;           &quot;043&quot;           &quot;042&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;          &quot;0131&quot;         &quot;02222&quot;          &quot;0111&quot;           &quot;043&quot;         &quot;02221&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;         &quot;02222&quot;          &quot;0212&quot;          &quot;0232&quot;          &quot;0211&quot;         &quot;02222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;          &quot;0131&quot;          &quot;0223&quot;         &quot;02222&quot;         &quot;02221&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;          &quot;0133&quot;         &quot;02222&quot;          &quot;0221&quot;           &quot;043&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;           &quot;041&quot;          &quot;0232&quot;          &quot;0133&quot;          &quot;0231&quot;         &quot;02221&quot;          &quot;0132&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;          &quot;0233&quot;           &quot;041&quot;          &quot;0133&quot;          &quot;0131&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;          &quot;0132&quot;          &quot;0221&quot;         &quot;02223&quot;           &quot;043&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;         &quot;02221&quot;          &quot;0221&quot;           &quot;042&quot;           &quot;041&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-3-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-3-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-4'>
<p><a id='tab-get-classes-from-hierarchical-partition-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 3429))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;          &quot;0133&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;           &quot;012&quot;         &quot;02222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;         &quot;02223&quot;          &quot;0132&quot;          &quot;0132&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;          &quot;0131&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;          &quot;0212&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;          &quot;0131&quot;          &quot;0111&quot;           &quot;023&quot;          &quot;0132&quot;           &quot;012&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;          &quot;0133&quot;         &quot;02221&quot;          &quot;0112&quot;          &quot;0132&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;          &quot;0133&quot;           &quot;033&quot;           &quot;012&quot;          &quot;0112&quot;           &quot;053&quot;          &quot;0132&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;           &quot;041&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;           &quot;042&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;         &quot;02223&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;         &quot;02221&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;         &quot;02223&quot;         &quot;02221&quot;         &quot;02223&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;         &quot;02222&quot;           &quot;042&quot;           &quot;023&quot;         &quot;02221&quot;         &quot;02221&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;          &quot;0211&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;         &quot;02221&quot;          &quot;0131&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0212&quot;           &quot;042&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;          &quot;0133&quot;         &quot;02221&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;          &quot;0133&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;           &quot;042&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;         &quot;02221&quot;         &quot;02222&quot;           &quot;052&quot;           &quot;043&quot;           &quot;042&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;          &quot;0131&quot;         &quot;02222&quot;          &quot;0111&quot;           &quot;043&quot;         &quot;02221&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;         &quot;02222&quot;          &quot;0212&quot;           &quot;023&quot;          &quot;0211&quot;         &quot;02222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;          &quot;0131&quot;          &quot;0223&quot;         &quot;02222&quot;         &quot;02221&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;          &quot;0133&quot;         &quot;02222&quot;          &quot;0221&quot;           &quot;043&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;           &quot;041&quot;           &quot;023&quot;          &quot;0133&quot;           &quot;023&quot;         &quot;02221&quot;          &quot;0132&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;           &quot;041&quot;          &quot;0133&quot;          &quot;0131&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;          &quot;0132&quot;          &quot;0221&quot;         &quot;02223&quot;           &quot;043&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;         &quot;02221&quot;          &quot;0221&quot;           &quot;042&quot;           &quot;041&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-4-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-4-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-5'>
<p><a id='tab-get-classes-from-hierarchical-partition-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 3489))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;          &quot;0133&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;           &quot;012&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;          &quot;0222&quot;          &quot;0132&quot;          &quot;0132&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;          &quot;0131&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;          &quot;0212&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;          &quot;0131&quot;          &quot;0111&quot;           &quot;023&quot;          &quot;0132&quot;           &quot;012&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;          &quot;0133&quot;          &quot;0222&quot;          &quot;0112&quot;          &quot;0132&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;          &quot;0133&quot;           &quot;033&quot;           &quot;012&quot;          &quot;0112&quot;           &quot;053&quot;          &quot;0132&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;           &quot;041&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;           &quot;042&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;          &quot;0222&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;          &quot;0222&quot;          &quot;0223&quot;          &quot;0131&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;          &quot;0222&quot;           &quot;042&quot;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;          &quot;0211&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;          &quot;0222&quot;          &quot;0131&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0212&quot;           &quot;042&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;          &quot;0133&quot;          &quot;0222&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;          &quot;0133&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;           &quot;042&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;052&quot;           &quot;043&quot;           &quot;042&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;          &quot;0131&quot;          &quot;0222&quot;          &quot;0111&quot;           &quot;043&quot;          &quot;0222&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;          &quot;0222&quot;          &quot;0212&quot;           &quot;023&quot;          &quot;0211&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;          &quot;0131&quot;          &quot;0223&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;          &quot;0133&quot;          &quot;0222&quot;          &quot;0221&quot;           &quot;043&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;           &quot;041&quot;           &quot;023&quot;          &quot;0133&quot;           &quot;023&quot;          &quot;0222&quot;          &quot;0132&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;           &quot;041&quot;          &quot;0133&quot;          &quot;0131&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;          &quot;0132&quot;          &quot;0221&quot;          &quot;0222&quot;           &quot;043&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;          &quot;0222&quot;          &quot;0221&quot;           &quot;042&quot;           &quot;041&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-5-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-5-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-6'>
<p><a id='tab-get-classes-from-hierarchical-partition-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 4028))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;           &quot;013&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;           &quot;012&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;          &quot;0222&quot;           &quot;013&quot;           &quot;013&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;           &quot;013&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;          &quot;0212&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;           &quot;013&quot;          &quot;0111&quot;           &quot;023&quot;           &quot;013&quot;           &quot;012&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;           &quot;013&quot;          &quot;0222&quot;          &quot;0112&quot;           &quot;013&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;           &quot;013&quot;           &quot;033&quot;           &quot;012&quot;          &quot;0112&quot;           &quot;053&quot;           &quot;013&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;           &quot;041&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;           &quot;042&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;          &quot;0222&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;          &quot;0222&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;          &quot;0222&quot;           &quot;042&quot;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;          &quot;0211&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;          &quot;0222&quot;           &quot;013&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0212&quot;           &quot;042&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;           &quot;013&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;           &quot;042&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;052&quot;           &quot;043&quot;           &quot;042&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;          &quot;0111&quot;           &quot;043&quot;          &quot;0222&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;          &quot;0222&quot;          &quot;0212&quot;           &quot;023&quot;          &quot;0211&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;013&quot;          &quot;0223&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;          &quot;0221&quot;           &quot;043&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;           &quot;041&quot;           &quot;023&quot;           &quot;013&quot;           &quot;023&quot;          &quot;0222&quot;           &quot;013&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;           &quot;041&quot;           &quot;013&quot;           &quot;013&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;           &quot;013&quot;          &quot;0221&quot;          &quot;0222&quot;           &quot;043&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;          &quot;0222&quot;          &quot;0221&quot;           &quot;042&quot;           &quot;041&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-6-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-6-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-7'>
<p><a id='tab-get-classes-from-hierarchical-partition-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 9255))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;          &quot;0112&quot;           &quot;031&quot;           &quot;013&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;          &quot;0113&quot;           &quot;031&quot;          &quot;0113&quot;          &quot;0221&quot;           &quot;012&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;          &quot;0113&quot;           &quot;031&quot;          &quot;0222&quot;           &quot;013&quot;           &quot;013&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0221&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0113&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;           &quot;013&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;          &quot;0212&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;          &quot;0111&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;           &quot;013&quot;          &quot;0111&quot;           &quot;023&quot;           &quot;013&quot;           &quot;012&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;           &quot;013&quot;          &quot;0222&quot;          &quot;0112&quot;           &quot;013&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;           &quot;013&quot;           &quot;033&quot;           &quot;012&quot;          &quot;0112&quot;           &quot;053&quot;           &quot;013&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;            &quot;04&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;          &quot;0113&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;          &quot;0111&quot;           &quot;052&quot;          &quot;0223&quot;            &quot;04&quot;          &quot;0111&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;          &quot;0222&quot;           &quot;034&quot;          &quot;0111&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;          &quot;0222&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;051&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;          &quot;0222&quot;            &quot;04&quot;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0111&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;          &quot;0211&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;          &quot;0222&quot;           &quot;013&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;           &quot;012&quot;          &quot;0112&quot;          &quot;0212&quot;            &quot;04&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;           &quot;013&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;          &quot;0113&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;            &quot;04&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;          &quot;0111&quot;            &quot;04&quot;          &quot;0222&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;          &quot;0222&quot;          &quot;0212&quot;           &quot;023&quot;          &quot;0211&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;          &quot;0113&quot;          &quot;0111&quot;           &quot;013&quot;          &quot;0223&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;          &quot;0221&quot;            &quot;04&quot;          &quot;0112&quot;          &quot;0112&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;           &quot;023&quot;           &quot;013&quot;           &quot;023&quot;          &quot;0222&quot;           &quot;013&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;            &quot;04&quot;           &quot;013&quot;           &quot;013&quot;          &quot;0112&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;          &quot;0112&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;           &quot;013&quot;          &quot;0221&quot;          &quot;0222&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;          &quot;0222&quot;          &quot;0221&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-7-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-7-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-8'>
<p><a id='tab-get-classes-from-hierarchical-partition-8-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 10873))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;013&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;011&quot;          &quot;0221&quot;           &quot;012&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;           &quot;011&quot;           &quot;031&quot;          &quot;0222&quot;           &quot;013&quot;           &quot;013&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;           &quot;011&quot;          &quot;0221&quot;          &quot;0221&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;          &quot;0211&quot;           &quot;032&quot;           &quot;052&quot;           &quot;011&quot;          &quot;0221&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;           &quot;013&quot;           &quot;032&quot;          &quot;0212&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;          &quot;0212&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;           &quot;013&quot;           &quot;011&quot;           &quot;023&quot;           &quot;013&quot;           &quot;012&quot;          &quot;0212&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;           &quot;013&quot;          &quot;0222&quot;           &quot;011&quot;           &quot;013&quot;          &quot;0211&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;           &quot;013&quot;           &quot;033&quot;           &quot;012&quot;           &quot;011&quot;           &quot;053&quot;           &quot;013&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;            &quot;04&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;           &quot;011&quot;           &quot;052&quot;          &quot;0223&quot;            &quot;04&quot;           &quot;011&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;          &quot;0222&quot;           &quot;034&quot;           &quot;011&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;          &quot;0222&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;051&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;          &quot;0222&quot;            &quot;04&quot;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;          &quot;0211&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;          &quot;0222&quot;           &quot;013&quot;           &quot;012&quot;           &quot;011&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;          &quot;0211&quot;           &quot;012&quot;           &quot;011&quot;          &quot;0212&quot;            &quot;04&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;           &quot;051&quot;          &quot;0212&quot;          &quot;0211&quot;           &quot;013&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;           &quot;011&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;052&quot;            &quot;04&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;           &quot;011&quot;            &quot;04&quot;          &quot;0222&quot;          &quot;0212&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;          &quot;0222&quot;          &quot;0212&quot;           &quot;023&quot;          &quot;0211&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;013&quot;          &quot;0223&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;          &quot;0221&quot;            &quot;04&quot;           &quot;011&quot;           &quot;011&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;           &quot;023&quot;           &quot;013&quot;           &quot;023&quot;          &quot;0222&quot;           &quot;013&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;            &quot;04&quot;           &quot;013&quot;           &quot;013&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;           &quot;011&quot;          &quot;0221&quot;          &quot;0212&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;           &quot;013&quot;          &quot;0221&quot;          &quot;0222&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;          &quot;0222&quot;          &quot;0221&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-8-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-8-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-8-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-9'>
<p><a id='tab-get-classes-from-hierarchical-partition-9-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 13097))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;          &quot;0221&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;          &quot;0223&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;013&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;011&quot;          &quot;0221&quot;           &quot;012&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;           &quot;011&quot;           &quot;031&quot;          &quot;0222&quot;           &quot;013&quot;           &quot;013&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;          &quot;0221&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;          &quot;0223&quot;           &quot;012&quot;           &quot;011&quot;          &quot;0221&quot;          &quot;0221&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;           &quot;021&quot;           &quot;032&quot;           &quot;052&quot;           &quot;011&quot;          &quot;0221&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;           &quot;013&quot;           &quot;032&quot;           &quot;021&quot;          &quot;0221&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;           &quot;021&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;           &quot;013&quot;           &quot;011&quot;           &quot;023&quot;           &quot;013&quot;           &quot;012&quot;           &quot;021&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;           &quot;013&quot;          &quot;0222&quot;           &quot;011&quot;           &quot;013&quot;           &quot;021&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;           &quot;013&quot;           &quot;033&quot;           &quot;012&quot;           &quot;011&quot;           &quot;053&quot;           &quot;013&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;            &quot;04&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;           &quot;011&quot;           &quot;052&quot;          &quot;0223&quot;            &quot;04&quot;           &quot;011&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;          &quot;0222&quot;           &quot;034&quot;           &quot;011&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;          &quot;0222&quot;          &quot;0223&quot;           &quot;013&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;051&quot;          &quot;0222&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;          &quot;0222&quot;            &quot;04&quot;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;           &quot;021&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;          &quot;0222&quot;           &quot;013&quot;           &quot;012&quot;           &quot;011&quot;          &quot;0223&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;           &quot;021&quot;           &quot;012&quot;           &quot;011&quot;           &quot;021&quot;            &quot;04&quot;          &quot;0221&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;           &quot;051&quot;           &quot;021&quot;           &quot;021&quot;           &quot;013&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;           &quot;011&quot;          &quot;0221&quot;           &quot;021&quot;           &quot;052&quot;            &quot;04&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;          &quot;0222&quot;          &quot;0222&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;           &quot;011&quot;            &quot;04&quot;          &quot;0222&quot;           &quot;021&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;          &quot;0222&quot;           &quot;021&quot;           &quot;023&quot;           &quot;021&quot;          &quot;0222&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;013&quot;          &quot;0223&quot;          &quot;0222&quot;          &quot;0222&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;           &quot;013&quot;          &quot;0222&quot;          &quot;0221&quot;            &quot;04&quot;           &quot;011&quot;           &quot;011&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;           &quot;023&quot;           &quot;013&quot;           &quot;023&quot;          &quot;0222&quot;           &quot;013&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;            &quot;04&quot;           &quot;013&quot;           &quot;013&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;          &quot;0221&quot;           &quot;011&quot;          &quot;0221&quot;           &quot;021&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;           &quot;013&quot;          &quot;0221&quot;          &quot;0222&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;          &quot;0222&quot;          &quot;0221&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-9-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-9-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-9-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-10'>
<p><a id='tab-get-classes-from-hierarchical-partition-10-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 16138))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;           &quot;022&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;           &quot;022&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;013&quot;           &quot;022&quot;           &quot;013&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;011&quot;           &quot;022&quot;           &quot;012&quot;           &quot;022&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;           &quot;011&quot;           &quot;031&quot;           &quot;022&quot;           &quot;013&quot;           &quot;013&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;           &quot;022&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;           &quot;022&quot;           &quot;012&quot;           &quot;011&quot;           &quot;022&quot;           &quot;022&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;           &quot;021&quot;           &quot;032&quot;           &quot;052&quot;           &quot;011&quot;           &quot;022&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;           &quot;023&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;           &quot;013&quot;           &quot;032&quot;           &quot;021&quot;           &quot;022&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;           &quot;021&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;           &quot;013&quot;           &quot;011&quot;           &quot;023&quot;           &quot;013&quot;           &quot;012&quot;           &quot;021&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;           &quot;013&quot;           &quot;022&quot;           &quot;011&quot;           &quot;013&quot;           &quot;021&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;           &quot;013&quot;           &quot;033&quot;           &quot;012&quot;           &quot;011&quot;           &quot;053&quot;           &quot;013&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;           &quot;023&quot;            &quot;04&quot;           &quot;033&quot;           &quot;023&quot;           &quot;052&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;           &quot;023&quot;           &quot;011&quot;           &quot;052&quot;           &quot;022&quot;            &quot;04&quot;           &quot;011&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;           &quot;022&quot;           &quot;034&quot;           &quot;011&quot;           &quot;051&quot;           &quot;012&quot;           &quot;023&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;           &quot;022&quot;           &quot;022&quot;           &quot;013&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;051&quot;           &quot;022&quot;           &quot;022&quot;           &quot;022&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;           &quot;022&quot;            &quot;04&quot;           &quot;023&quot;           &quot;022&quot;           &quot;022&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;           &quot;023&quot;           &quot;021&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;           &quot;022&quot;           &quot;013&quot;           &quot;012&quot;           &quot;011&quot;           &quot;022&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;           &quot;021&quot;           &quot;012&quot;           &quot;011&quot;           &quot;021&quot;            &quot;04&quot;           &quot;022&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;           &quot;013&quot;           &quot;022&quot;           &quot;051&quot;           &quot;021&quot;           &quot;021&quot;           &quot;013&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;           &quot;011&quot;           &quot;022&quot;           &quot;021&quot;           &quot;052&quot;            &quot;04&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;           &quot;023&quot;           &quot;022&quot;           &quot;022&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;           &quot;013&quot;           &quot;022&quot;           &quot;011&quot;            &quot;04&quot;           &quot;022&quot;           &quot;021&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;           &quot;022&quot;           &quot;021&quot;           &quot;023&quot;           &quot;021&quot;           &quot;022&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;013&quot;           &quot;022&quot;           &quot;022&quot;           &quot;022&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;           &quot;013&quot;           &quot;022&quot;           &quot;022&quot;            &quot;04&quot;           &quot;011&quot;           &quot;011&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;           &quot;023&quot;           &quot;013&quot;           &quot;023&quot;           &quot;022&quot;           &quot;013&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;           &quot;023&quot;            &quot;04&quot;           &quot;013&quot;           &quot;013&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;           &quot;022&quot;           &quot;011&quot;           &quot;022&quot;           &quot;021&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;           &quot;013&quot;           &quot;022&quot;           &quot;022&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;           &quot;022&quot;           &quot;022&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-10-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-10-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-10-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-11'>
<p><a id='tab-get-classes-from-hierarchical-partition-11-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 18356))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;            &quot;02&quot;           &quot;053&quot;           &quot;012&quot;           &quot;051&quot;            &quot;02&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;013&quot;            &quot;02&quot;           &quot;013&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;           &quot;011&quot;           &quot;031&quot;           &quot;011&quot;            &quot;02&quot;           &quot;012&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;           &quot;011&quot;           &quot;031&quot;            &quot;02&quot;           &quot;013&quot;           &quot;013&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;           &quot;012&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;            &quot;02&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;            &quot;02&quot;           &quot;012&quot;           &quot;011&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;            &quot;02&quot;           &quot;032&quot;           &quot;052&quot;           &quot;011&quot;            &quot;02&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;           &quot;012&quot;           &quot;012&quot;           &quot;053&quot;            &quot;02&quot;           &quot;031&quot;           &quot;012&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;           &quot;013&quot;           &quot;032&quot;            &quot;02&quot;            &quot;02&quot;           &quot;012&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;           &quot;012&quot;            &quot;02&quot;           &quot;012&quot;           &quot;051&quot;           &quot;033&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;           &quot;013&quot;           &quot;011&quot;            &quot;02&quot;           &quot;013&quot;           &quot;012&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;           &quot;013&quot;            &quot;02&quot;           &quot;011&quot;           &quot;013&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;           &quot;013&quot;           &quot;033&quot;           &quot;012&quot;           &quot;011&quot;           &quot;053&quot;           &quot;013&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;            &quot;02&quot;            &quot;04&quot;           &quot;033&quot;            &quot;02&quot;           &quot;052&quot;           &quot;011&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;            &quot;02&quot;           &quot;011&quot;           &quot;052&quot;            &quot;02&quot;            &quot;04&quot;           &quot;011&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;            &quot;02&quot;           &quot;034&quot;           &quot;011&quot;           &quot;051&quot;           &quot;012&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;            &quot;02&quot;            &quot;02&quot;           &quot;013&quot;           &quot;012&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;051&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;           &quot;012&quot;            &quot;02&quot;            &quot;02&quot;           &quot;034&quot;           &quot;012&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;            &quot;02&quot;           &quot;013&quot;           &quot;012&quot;           &quot;011&quot;            &quot;02&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;            &quot;02&quot;           &quot;012&quot;           &quot;011&quot;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;           &quot;013&quot;            &quot;02&quot;           &quot;051&quot;            &quot;02&quot;            &quot;02&quot;           &quot;013&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;           &quot;011&quot;            &quot;02&quot;            &quot;02&quot;           &quot;052&quot;            &quot;04&quot;           &quot;012&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;           &quot;013&quot;            &quot;02&quot;           &quot;011&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;           &quot;011&quot;           &quot;011&quot;           &quot;013&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;           &quot;013&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;           &quot;011&quot;           &quot;011&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;            &quot;02&quot;           &quot;013&quot;            &quot;02&quot;            &quot;02&quot;           &quot;013&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;            &quot;02&quot;            &quot;04&quot;           &quot;013&quot;           &quot;013&quot;           &quot;011&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;            &quot;02&quot;           &quot;011&quot;            &quot;02&quot;            &quot;02&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;           &quot;013&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-11-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-11-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-11-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-12'>
<p><a id='tab-get-classes-from-hierarchical-partition-12-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 34722))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;            &quot;02&quot;           &quot;053&quot;            &quot;01&quot;           &quot;051&quot;            &quot;02&quot;           &quot;032&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;            &quot;01&quot;           &quot;031&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;           &quot;032&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;            &quot;01&quot;           &quot;031&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;            &quot;01&quot;           &quot;031&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;            &quot;01&quot;           &quot;035&quot;           &quot;032&quot;           &quot;053&quot;            &quot;02&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;            &quot;02&quot;           &quot;032&quot;           &quot;052&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;            &quot;01&quot;            &quot;01&quot;           &quot;053&quot;            &quot;02&quot;           &quot;031&quot;            &quot;01&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;            &quot;01&quot;           &quot;032&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot;           &quot;031&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;           &quot;051&quot;           &quot;033&quot;            &quot;01&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;            &quot;01&quot;           &quot;033&quot;            &quot;01&quot;            &quot;01&quot;           &quot;053&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;            &quot;02&quot;            &quot;04&quot;           &quot;033&quot;            &quot;02&quot;           &quot;052&quot;            &quot;01&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;            &quot;02&quot;            &quot;01&quot;           &quot;052&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;            &quot;02&quot;           &quot;034&quot;            &quot;01&quot;           &quot;051&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;           &quot;033&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;           &quot;034&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;            &quot;01&quot;            &quot;01&quot;           &quot;051&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;           &quot;034&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;            &quot;01&quot;            &quot;02&quot;           &quot;051&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;           &quot;052&quot;            &quot;04&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;           &quot;035&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;           &quot;034&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-12-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-12-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-12-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-13'>
<p><a id='tab-get-classes-from-hierarchical-partition-13-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 37386))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;            &quot;02&quot;           &quot;053&quot;            &quot;01&quot;           &quot;051&quot;            &quot;02&quot;            &quot;03&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;03&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;           &quot;053&quot;            &quot;01&quot;            &quot;03&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;           &quot;052&quot;            &quot;01&quot;            &quot;03&quot;            &quot;03&quot;           &quot;053&quot;            &quot;02&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;            &quot;02&quot;            &quot;03&quot;           &quot;052&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;            &quot;01&quot;            &quot;01&quot;           &quot;053&quot;            &quot;02&quot;            &quot;03&quot;            &quot;01&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot;            &quot;03&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;           &quot;051&quot;            &quot;03&quot;            &quot;01&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;           &quot;051&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;01&quot;            &quot;01&quot;           &quot;053&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;            &quot;02&quot;            &quot;04&quot;            &quot;03&quot;            &quot;02&quot;           &quot;052&quot;            &quot;01&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;            &quot;02&quot;            &quot;01&quot;           &quot;052&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;            &quot;02&quot;            &quot;03&quot;            &quot;01&quot;           &quot;051&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;            &quot;03&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;03&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;            &quot;01&quot;            &quot;01&quot;           &quot;051&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;           &quot;053&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;03&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;            &quot;01&quot;            &quot;02&quot;           &quot;051&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;           &quot;052&quot;            &quot;04&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;           &quot;052&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;           &quot;052&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;            &quot;03&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;            &quot;03&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;           &quot;051&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;           &quot;052&quot;           &quot;051&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-13-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-13-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-13-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-get-classes-from-hierarchical-partition-14'>
<p><a id='tab-get-classes-from-hierarchical-partition-14-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">get_classes(res_rh, merge_node = merge_node_param(min_n_signatures = 67663))
</code></pre>

<pre><code>#&gt; TCGA.JY.A6FB.01 TCGA.LN.A49L.01 TCGA.LN.A4A4.01 TCGA.LN.A49M.01 TCGA.Q9.A6FW.01 TCGA.Z6.AAPN.01 
#&gt;            &quot;02&quot;            &quot;05&quot;            &quot;01&quot;            &quot;05&quot;            &quot;02&quot;            &quot;03&quot; 
#&gt; TCGA.Q9.A6FU.01 TCGA.L5.A43C.11 TCGA.S8.A6BW.01 TCGA.S8.A6BV.01 TCGA.V5.A7RC.01 TCGA.VR.A8ET.01 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;03&quot; 
#&gt; TCGA.LN.A4A3.01 TCGA.L5.A4OH.11 TCGA.LN.A49X.01 TCGA.L5.A4OI.01 TCGA.LN.A7HV.01 TCGA.R6.A6DN.01 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A3YB.01 TCGA.IG.A3YC.01 TCGA.L5.A4OE.11 TCGA.L5.A4OG.01 TCGA.KH.A6WC.01 TCGA.L7.A56G.01 
#&gt;            &quot;05&quot;            &quot;01&quot;            &quot;03&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.IG.A51D.01 TCGA.VR.A8EP.01 TCGA.L5.A88T.01 TCGA.L5.A4ON.11 TCGA.L5.A43J.01 TCGA.L5.A43E.01 
#&gt;            &quot;05&quot;            &quot;01&quot;            &quot;03&quot;            &quot;03&quot;            &quot;05&quot;            &quot;02&quot; 
#&gt; TCGA.X8.AAAR.01 TCGA.JY.A6FE.01 TCGA.LN.A49N.01 TCGA.L5.A4ON.01 TCGA.V5.AASW.01 TCGA.L5.A43I.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OF.01 TCGA.L5.A4OQ.11 TCGA.IG.A3I8.01 TCGA.VR.AA7B.01 TCGA.L5.A4OJ.01 TCGA.IG.A3Y9.01 
#&gt;            &quot;02&quot;            &quot;03&quot;            &quot;05&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OM.01 TCGA.LN.A4A6.01 TCGA.LN.A49V.01 TCGA.L5.A4OH.01 TCGA.L5.A4OI.11 TCGA.LN.A49R.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;05&quot;            &quot;02&quot;            &quot;03&quot;            &quot;01&quot; 
#&gt; TCGA.LN.A49K.01 TCGA.IG.A4QT.01 TCGA.R6.A6L4.01 TCGA.L7.A6VZ.01 TCGA.LN.A49U.01 TCGA.L5.A4OF.11 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot;            &quot;03&quot; 
#&gt; TCGA.LN.A7HX.01 TCGA.L5.A4OO.01 TCGA.LN.A4A8.01 TCGA.JY.A6FG.01 TCGA.L5.A4OJ.11 TCGA.LN.A5U7.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;05&quot;            &quot;03&quot;            &quot;01&quot; 
#&gt; TCGA.V5.A7RC.06 TCGA.IG.A625.01 TCGA.L5.A4OP.01 TCGA.IG.A4P3.01 TCGA.LN.A49Y.01 TCGA.L5.A43C.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88W.01 TCGA.L5.A43H.01 TCGA.L5.A4OE.01 TCGA.IG.A50L.01 TCGA.LN.A7HY.01 TCGA.R6.A6KZ.01 
#&gt;            &quot;05&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A49P.01 TCGA.L5.A4OM.11 TCGA.LN.A4A1.01 TCGA.LN.A49O.01 TCGA.LN.A4A5.01 TCGA.LN.A49W.01 
#&gt;            &quot;01&quot;            &quot;03&quot;            &quot;01&quot;            &quot;01&quot;            &quot;05&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OR.01 TCGA.L5.A43M.01 TCGA.L5.A4OP.11 TCGA.V5.A7RE.01 TCGA.VR.AA7I.01 TCGA.IG.A3YA.01 
#&gt;            &quot;02&quot;            &quot;04&quot;            &quot;03&quot;            &quot;02&quot;            &quot;05&quot;            &quot;01&quot; 
#&gt; TCGA.V5.A7RE.11 TCGA.LN.A7HZ.01 TCGA.VR.AA7D.01 TCGA.V5.A7RB.01 TCGA.L5.A4OQ.01 TCGA.IG.A3QL.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;05&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A6DQ.01 TCGA.IG.A3I8.11 TCGA.LN.A4A2.01 TCGA.IC.A6RF.01 TCGA.LN.A49S.01 TCGA.IG.A4QS.01 
#&gt;            &quot;02&quot;            &quot;03&quot;            &quot;01&quot;            &quot;05&quot;            &quot;01&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A4OG.11 TCGA.L5.A88Y.01 TCGA.L5.A88V.01 TCGA.LN.A7HW.01 TCGA.IG.A8O2.01 TCGA.IG.A7DP.01 
#&gt;            &quot;03&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;03&quot; 
#&gt; TCGA.L5.A8NQ.01 TCGA.LN.A8I0.01 TCGA.JY.A93F.01 TCGA.M9.A5M8.01 TCGA.L5.A4OW.01 TCGA.2H.A9GK.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;05&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A8NW.01 TCGA.R6.A8W5.01 TCGA.L5.A8NH.01 TCGA.2H.A9GR.01 TCGA.L5.A8NV.01 TCGA.XP.A8T8.01 
#&gt;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A88Z.01 TCGA.IG.A5B8.01 TCGA.R6.A6XG.01 TCGA.L5.A8NN.01 TCGA.LN.A9FP.01 TCGA.LN.A4MR.01 
#&gt;            &quot;05&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;03&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A8NS.01 TCGA.LN.A4MQ.01 TCGA.LN.A4A9.01 TCGA.VR.A8EX.01 TCGA.JY.A938.01 TCGA.JY.A6FA.01 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A8WG.01 TCGA.VR.A8EO.01 TCGA.VR.A8EU.01 TCGA.R6.A6L6.01 TCGA.L5.A8NE.01 TCGA.V5.AASX.11 
#&gt;            &quot;02&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;04&quot;            &quot;02&quot; 
#&gt; TCGA.LN.A8I1.01 TCGA.L5.A893.01 TCGA.IC.A6RF.11 TCGA.L5.A8NU.01 TCGA.R6.A6XQ.01 TCGA.LN.A5U5.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;05&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.Z6.A8JD.01 TCGA.L5.A4OT.01 TCGA.ZR.A9CJ.01 TCGA.Z6.A8JE.01 TCGA.JY.A6FH.01 TCGA.XP.A8T6.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;05&quot;            &quot;04&quot;            &quot;01&quot; 
#&gt; TCGA.R6.A8W8.01 TCGA.JY.A93E.01 TCGA.2H.A9GI.01 TCGA.IG.A6QS.01 TCGA.VR.A8Q7.01 TCGA.R6.A6Y0.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;05&quot;            &quot;04&quot;            &quot;04&quot; 
#&gt; TCGA.VR.A8EZ.01 TCGA.2H.A9GL.01 TCGA.LN.A8HZ.01 TCGA.L5.A891.01 TCGA.L5.A8NM.01 TCGA.JY.A93D.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;01&quot;            &quot;04&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.XP.A8T7.01 TCGA.L5.A4OX.01 TCGA.R6.A6Y2.01 TCGA.2H.A9GF.01 TCGA.2H.A9GO.01 TCGA.L5.A8NR.01 
#&gt;            &quot;05&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.L5.A88S.01 TCGA.VR.A8EW.01 TCGA.VR.A8ER.01 TCGA.L5.A4OU.01 TCGA.JY.A93C.01 TCGA.V5.AASX.01 
#&gt;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;02&quot; 
#&gt; TCGA.IG.A97H.01 TCGA.L5.A8NT.01 TCGA.R6.A8WC.01 TCGA.2H.A9GJ.01 TCGA.VR.AA4G.01 TCGA.JY.A6FD.01 
#&gt;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.2H.A9GN.01 TCGA.VR.AA4D.01 TCGA.IG.A97I.01 TCGA.2H.A9GM.01 TCGA.L5.A8NG.01 TCGA.IG.A5S3.01 
#&gt;            &quot;04&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;01&quot; 
#&gt; TCGA.IC.A6RE.11 TCGA.IC.A6RE.01 TCGA.2H.A9GG.01 TCGA.LN.A5U6.01 TCGA.LN.A9FQ.01 TCGA.L5.A8NK.01 
#&gt;            &quot;03&quot;            &quot;02&quot;            &quot;04&quot;            &quot;01&quot;            &quot;01&quot;            &quot;01&quot; 
#&gt; TCGA.L5.A4OS.01 TCGA.RE.A7BO.01 TCGA.LN.A9FO.01 TCGA.L5.A8NJ.01 TCGA.JY.A939.01 TCGA.VR.A8EY.01 
#&gt;            &quot;03&quot;            &quot;02&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;05&quot; 
#&gt; TCGA.Z6.A9VB.01 TCGA.V5.AASV.01 TCGA.LN.A9FR.01 TCGA.JY.A6F8.01 TCGA.VR.A8EQ.01 TCGA.2H.A9GQ.01 
#&gt;            &quot;05&quot;            &quot;05&quot;            &quot;01&quot;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot; 
#&gt; TCGA.L5.A8NL.01 TCGA.2H.A9GH.01 TCGA.L5.A8NF.01 TCGA.L5.A8NI.01 
#&gt;            &quot;02&quot;            &quot;02&quot;            &quot;04&quot;            &quot;04&quot;
</code></pre>

<script>
$('#tab-get-classes-from-hierarchical-partition-14-a').parent().next().next().hide();
$('#tab-get-classes-from-hierarchical-partition-14-a').click(function(){
  $('#tab-get-classes-from-hierarchical-partition-14-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>



### Top rows heatmap

Heatmaps of the top rows:





```r
top_rows_heatmap(res_rh)
```

![plot of chunk top-rows-heatmap](figure_cola/top-rows-heatmap-1.png)

```
#> Error in h(simpleError(msg, call)) : 
#>   error in evaluating the argument 'object' in selecting a method for function 'draw': no applicable method for 'height' applied to an object of class "list"
```

Top rows on each node:


```r
top_rows_overlap(res_rh, method = "upset")
```

![plot of chunk top-rows-overlap](figure_cola/top-rows-overlap-1.png)


### UMAP plot

UMAP plot which shows how samples are separated.




<script>
$( function() {
	$( '#tabs-dimension-reduction-by-depth' ).tabs();
} );
</script>
<div id='tabs-dimension-reduction-by-depth'>
<ul>
<li><a href='#tab-dimension-reduction-by-depth-1'>n_signatures ≥ 1432</a></li>
<li><a href='#tab-dimension-reduction-by-depth-2'>n_signatures ≥ 1449</a></li>
<li><a href='#tab-dimension-reduction-by-depth-3'>n_signatures ≥ 2070</a></li>
<li><a href='#tab-dimension-reduction-by-depth-4'>n_signatures ≥ 3429</a></li>
<li><a href='#tab-dimension-reduction-by-depth-5'>n_signatures ≥ 3489</a></li>
<li><a href='#tab-dimension-reduction-by-depth-6'>n_signatures ≥ 4028</a></li>
<li><a href='#tab-dimension-reduction-by-depth-7'>n_signatures ≥ 9255</a></li>
<li><a href='#tab-dimension-reduction-by-depth-8'>n_signatures ≥ 10873</a></li>
<li><a href='#tab-dimension-reduction-by-depth-9'>n_signatures ≥ 13097</a></li>
<li><a href='#tab-dimension-reduction-by-depth-10'>n_signatures ≥ 16138</a></li>
<li><a href='#tab-dimension-reduction-by-depth-11'>n_signatures ≥ 18356</a></li>
<li><a href='#tab-dimension-reduction-by-depth-12'>n_signatures ≥ 34722</a></li>
<li><a href='#tab-dimension-reduction-by-depth-13'>n_signatures ≥ 37386</a></li>
<li><a href='#tab-dimension-reduction-by-depth-14'>n_signatures ≥ 67663</a></li>
</ul>
<div id='tab-dimension-reduction-by-depth-1'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 1432),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 1432),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-1-1.png" title="plot of chunk tab-dimension-reduction-by-depth-1" alt="plot of chunk tab-dimension-reduction-by-depth-1" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-2'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 1449),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 1449),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-2-1.png" title="plot of chunk tab-dimension-reduction-by-depth-2" alt="plot of chunk tab-dimension-reduction-by-depth-2" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-3'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 2070),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 2070),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-3-1.png" title="plot of chunk tab-dimension-reduction-by-depth-3" alt="plot of chunk tab-dimension-reduction-by-depth-3" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-4'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 3429),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 3429),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-4-1.png" title="plot of chunk tab-dimension-reduction-by-depth-4" alt="plot of chunk tab-dimension-reduction-by-depth-4" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-5'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 3489),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 3489),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-5-1.png" title="plot of chunk tab-dimension-reduction-by-depth-5" alt="plot of chunk tab-dimension-reduction-by-depth-5" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-6'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 4028),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 4028),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-6-1.png" title="plot of chunk tab-dimension-reduction-by-depth-6" alt="plot of chunk tab-dimension-reduction-by-depth-6" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-7'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 9255),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 9255),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-7-1.png" title="plot of chunk tab-dimension-reduction-by-depth-7" alt="plot of chunk tab-dimension-reduction-by-depth-7" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-8'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 10873),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 10873),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-8-1.png" title="plot of chunk tab-dimension-reduction-by-depth-8" alt="plot of chunk tab-dimension-reduction-by-depth-8" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-9'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 13097),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 13097),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-9-1.png" title="plot of chunk tab-dimension-reduction-by-depth-9" alt="plot of chunk tab-dimension-reduction-by-depth-9" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-10'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 16138),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 16138),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-10-1.png" title="plot of chunk tab-dimension-reduction-by-depth-10" alt="plot of chunk tab-dimension-reduction-by-depth-10" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-11'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 18356),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 18356),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-11-1.png" title="plot of chunk tab-dimension-reduction-by-depth-11" alt="plot of chunk tab-dimension-reduction-by-depth-11" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-12'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 34722),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 34722),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-12-1.png" title="plot of chunk tab-dimension-reduction-by-depth-12" alt="plot of chunk tab-dimension-reduction-by-depth-12" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-13'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 37386),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 37386),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-13-1.png" title="plot of chunk tab-dimension-reduction-by-depth-13" alt="plot of chunk tab-dimension-reduction-by-depth-13" width="100%" /></p>

</div>
<div id='tab-dimension-reduction-by-depth-14'>
<pre><code class="r">par(mfrow = c(1, 2))
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 67663),
    method = &quot;UMAP&quot;, top_value_method = &quot;SD&quot;, top_n = 40000, scale_rows = FALSE)
dimension_reduction(res_rh, merge_node = merge_node_param(min_n_signatures = 67663),
    method = &quot;UMAP&quot;, top_value_method = &quot;ATC&quot;, top_n = 40000, scale_rows = TRUE)
</code></pre>

<p><img src="figure_cola/tab-dimension-reduction-by-depth-14-1.png" title="plot of chunk tab-dimension-reduction-by-depth-14" alt="plot of chunk tab-dimension-reduction-by-depth-14" width="100%" /></p>

</div>
</div>




### Signature heatmap

Signatures on the heatmap are the union of all signatures found on every node
on the hierarchy. The number of k-means on rows are automatically selected by the function.




<script>
$( function() {
	$( '#tabs-get-signatures-from-hierarchical-partition' ).tabs();
} );
</script>
<div id='tabs-get-signatures-from-hierarchical-partition'>
<ul>
<li><a href='#tab-get-signatures-from-hierarchical-partition-1'>n_signatures ≥ 1432</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-2'>n_signatures ≥ 1449</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-3'>n_signatures ≥ 2070</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-4'>n_signatures ≥ 3429</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-5'>n_signatures ≥ 3489</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-6'>n_signatures ≥ 4028</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-7'>n_signatures ≥ 9255</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-8'>n_signatures ≥ 10873</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-9'>n_signatures ≥ 13097</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-10'>n_signatures ≥ 16138</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-11'>n_signatures ≥ 18356</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-12'>n_signatures ≥ 34722</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-13'>n_signatures ≥ 37386</a></li>
<li><a href='#tab-get-signatures-from-hierarchical-partition-14'>n_signatures ≥ 67663</a></li>
</ul>
<div id='tab-get-signatures-from-hierarchical-partition-1'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 1432))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-1-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-1"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-2'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 1449))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-2-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-2"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-3'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 2070))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-3-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-3"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-4'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 3429))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-4-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-4"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-5'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 3489))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-5-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-5"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-6'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 4028))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-6-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-6"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-7'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 9255))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-7-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-7"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-8'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 10873))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-8-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-8"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-9'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 13097))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-9-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-9"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-10'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 16138))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-10-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-10"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-11'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 18356))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-11-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-11"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-12'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 34722))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-12-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-12"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-13'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 37386))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-13-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-13"/></p>

</div>
<div id='tab-get-signatures-from-hierarchical-partition-14'>
<pre><code class="r">get_signatures(res_rh, merge_node = merge_node_param(min_n_signatures = 67663))
</code></pre>

<p><img src="figure_cola/tab-get-signatures-from-hierarchical-partition-14-1.png" alt="plot of chunk tab-get-signatures-from-hierarchical-partition-14"/></p>

</div>
</div>




Compare signatures from different nodes:


```r
compare_signatures(res_rh, verbose = FALSE)
```

![plot of chunk unnamed-chunk-24](figure_cola/unnamed-chunk-24-1.png)

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs. Note it only works on every node and the final signatures
are the union of all signatures of all nodes.


```r
# code only for demonstration
# e.g. to show the top 500 most significant rows on each node.
tb = get_signature(res_rh, top_signatures = 500)
```


## Results for each node


---------------------------------------------------




### Node0


Child nodes: 
                [Node01](#Node01)
        ,
                [Node02](#Node02)
        ,
                [Node03](#Node03)
        ,
                [Node04](#Node04)
        ,
                [Node05](#Node05)
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["0"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 202 columns.
#>   Top rows (1000) are extracted by 'SD' method.
#>   Subgroups are detected by 'skmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 5.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-0-collect-plots](figure_cola/node-0-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-0-select-partition-number](figure_cola/node-0-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           0.989       0.995         0.5017 0.499   0.499
#> 3 3 1.000           0.963       0.985         0.2052 0.875   0.755
#> 4 4 0.884           0.891       0.947         0.1071 0.922   0.805
#> 5 5 1.000           0.953       0.984         0.0647 0.941   0.824
#> 6 6 0.849           0.848       0.912         0.0748 0.934   0.773
#> 7 7 0.840           0.653       0.863         0.0321 0.985   0.937
#> 8 8 0.833           0.648       0.734         0.0277 0.911   0.640
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 5
#> attr(,"optional")
#> [1] 2 3
```

There is also optional best $k$ = 2 3 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-0-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-0-get-classes'>
<ul>
<li><a href='#tab-node-0-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-0-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-0-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-0-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-0-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-0-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-0-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-0-get-classes-1'>
<p><a id='tab-node-0-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2
#&gt; TCGA.JY.A6FB.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A49L.01     1   0.529      0.864 0.88 0.12
#&gt; TCGA.LN.A4A4.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49M.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.Q9.A6FW.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.Z6.AAPN.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.Q9.A6FU.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A43C.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.S8.A6BW.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.S8.A6BV.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.V5.A7RC.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8ET.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4A3.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OH.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49X.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OI.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A7HV.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6DN.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A3YB.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A3YC.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OE.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OG.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.KH.A6WC.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L7.A56G.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A51D.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8EP.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A88T.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4ON.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A43J.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A43E.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.X8.AAAR.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A6FE.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49N.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4ON.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.V5.AASW.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A43I.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OF.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OQ.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A3I8.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.AA7B.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OJ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A3Y9.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OM.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4A6.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49V.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OH.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OI.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49R.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49K.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A4QT.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6L4.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L7.A6VZ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A49U.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OF.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A7HX.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OO.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A4A8.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.JY.A6FG.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OJ.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A5U7.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.V5.A7RC.06     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A625.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OP.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A4P3.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49Y.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A43C.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A88W.01     2   0.680      0.779 0.18 0.82
#&gt; TCGA.L5.A43H.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OE.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A50L.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A7HY.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6KZ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A49P.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OM.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4A1.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49O.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4A5.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A49W.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OR.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A43M.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OP.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.V5.A7RE.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.VR.AA7I.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A3YA.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.V5.A7RE.11     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A7HZ.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.AA7D.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.V5.A7RB.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OQ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A3QL.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6DQ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A3I8.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4A2.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IC.A6RF.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A49S.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A4QS.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OG.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A88Y.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A88V.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A7HW.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A8O2.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A7DP.01     1   0.584      0.838 0.86 0.14
#&gt; TCGA.L5.A8NQ.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A8I0.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.JY.A93F.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.M9.A5M8.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A4OW.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GK.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NW.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.R6.A8W5.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NH.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GR.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NV.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.XP.A8T8.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A88Z.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IG.A5B8.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6XG.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NN.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A9FP.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4MR.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A8NS.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A4MQ.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A4A9.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8EX.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.JY.A938.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A6FA.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A8WG.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.VR.A8EO.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8EU.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6L6.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NE.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.V5.AASX.11     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A8I1.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A893.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IC.A6RF.11     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NU.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.R6.A6XQ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A5U5.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.Z6.A8JD.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OT.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.ZR.A9CJ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.Z6.A8JE.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A6FH.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.XP.A8T6.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A8W8.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A93E.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GI.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A6QS.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8Q7.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.R6.A6Y0.01     1   0.680      0.782 0.82 0.18
#&gt; TCGA.VR.A8EZ.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.2H.A9GL.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A8HZ.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A891.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NM.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A93D.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.XP.A8T7.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OX.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.R6.A6Y2.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GF.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GO.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NR.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A88S.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8EW.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.VR.A8ER.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OU.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A93C.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.V5.AASX.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A97H.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A8NT.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.R6.A8WC.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GJ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.VR.AA4G.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.JY.A6FD.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.2H.A9GN.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.VR.AA4D.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A97I.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.2H.A9GM.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NG.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.IG.A5S3.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IC.A6RE.11     1   0.000      0.996 1.00 0.00
#&gt; TCGA.IC.A6RE.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GG.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A5U6.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.LN.A9FQ.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A8NK.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A4OS.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.RE.A7BO.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A9FO.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.L5.A8NJ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.JY.A939.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.VR.A8EY.01     2   0.904      0.529 0.32 0.68
#&gt; TCGA.Z6.A9VB.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.V5.AASV.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.LN.A9FR.01     1   0.000      0.996 1.00 0.00
#&gt; TCGA.JY.A6F8.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.VR.A8EQ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GQ.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NL.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.2H.A9GH.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NF.01     2   0.000      0.995 0.00 1.00
#&gt; TCGA.L5.A8NI.01     2   0.000      0.995 0.00 1.00
</code></pre>

<script>
$('#tab-node-0-get-classes-1-a').parent().next().next().hide();
$('#tab-node-0-get-classes-1-a').click(function(){
  $('#tab-node-0-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0-get-classes-2'>
<p><a id='tab-node-0-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.JY.A6FB.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A49L.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A4A4.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49M.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.Z6.AAPN.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.Q9.A6FU.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A43C.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.S8.A6BW.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.S8.A6BV.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8ET.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A4A3.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OH.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A49X.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A3YB.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A3YC.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OE.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.L5.A4OG.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.KH.A6WC.01     1  0.0892      0.975 0.98 0.00 0.02
#&gt; TCGA.L7.A56G.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A51D.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8EP.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A88T.01     3  0.5835      0.490 0.34 0.00 0.66
#&gt; TCGA.L5.A4ON.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.L5.A43J.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A43E.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A43I.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OF.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OQ.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.IG.A3I8.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.AA7B.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A3Y9.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OM.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49V.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OI.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A49R.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49K.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A4QT.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.R6.A6L4.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L7.A6VZ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A49U.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OF.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A7HX.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A4A8.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.JY.A6FG.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OJ.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A5U7.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.V5.A7RC.06     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A625.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A4P3.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A43C.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A88W.01     1  0.4796      0.662 0.78 0.22 0.00
#&gt; TCGA.L5.A43H.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A50L.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A7HY.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A49P.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OM.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A4A1.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49O.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A49W.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A43M.01     3  0.2959      0.857 0.00 0.10 0.90
#&gt; TCGA.L5.A4OP.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.V5.A7RE.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.VR.AA7I.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A3YA.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.V5.A7RE.11     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.AA7D.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.V5.A7RB.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OQ.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.IG.A3QL.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A3I8.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A4A2.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A49S.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OG.11     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.L5.A88Y.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A7HW.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A8O2.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A7DP.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.L5.A8NQ.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.JY.A93F.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.M9.A5M8.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.R6.A8W5.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NH.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IG.A5B8.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NN.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A9FP.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.LN.A4MR.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A4A9.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.JY.A938.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.JY.A6FA.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A8WG.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.VR.A8EO.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8EU.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A6L6.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NE.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.11     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A8I1.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IC.A6RF.11     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NU.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.R6.A6XQ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A5U5.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.Z6.A8JD.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OT.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.ZR.A9CJ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.Z6.A8JE.01     2  0.5397      0.565 0.28 0.72 0.00
#&gt; TCGA.JY.A6FH.01     2  0.3686      0.831 0.00 0.86 0.14
#&gt; TCGA.XP.A8T6.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.R6.A8W8.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A6QS.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8Q7.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.R6.A6Y0.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.VR.A8EZ.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A891.01     2  0.6280      0.169 0.00 0.54 0.46
#&gt; TCGA.L5.A8NM.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.XP.A8T7.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OX.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.R6.A6Y2.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GO.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A88S.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8EW.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A97H.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GJ.01     2  0.5835      0.495 0.00 0.66 0.34
#&gt; TCGA.VR.AA4G.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.2H.A9GN.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.VR.AA4D.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A97I.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.IG.A5S3.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.IC.A6RE.11     3  0.6244      0.233 0.44 0.00 0.56
#&gt; TCGA.IC.A6RE.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GG.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A5U6.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A4OS.01     3  0.0000      0.954 0.00 0.00 1.00
#&gt; TCGA.RE.A7BO.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.JY.A939.01     2  0.5216      0.653 0.00 0.74 0.26
#&gt; TCGA.VR.A8EY.01     1  0.1529      0.943 0.96 0.04 0.00
#&gt; TCGA.Z6.A9VB.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.V5.AASV.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.LN.A9FR.01     1  0.0000      0.996 1.00 0.00 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GQ.01     3  0.4555      0.722 0.00 0.20 0.80
#&gt; TCGA.L5.A8NL.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.2H.A9GH.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NF.01     2  0.0000      0.981 0.00 1.00 0.00
#&gt; TCGA.L5.A8NI.01     2  0.2959      0.879 0.00 0.90 0.10
</code></pre>

<script>
$('#tab-node-0-get-classes-2-a').parent().next().next().hide();
$('#tab-node-0-get-classes-2-a').click(function(){
  $('#tab-node-0-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0-get-classes-3'>
<p><a id='tab-node-0-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49L.01     4  0.0000     0.6114 0.00 0.00 0.00 1.00
#&gt; TCGA.LN.A4A4.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49M.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.Q9.A6FW.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.Z6.AAPN.01     3  0.2647     0.7400 0.12 0.00 0.88 0.00
#&gt; TCGA.Q9.A6FU.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.S8.A6BW.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.S8.A6BV.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ET.01     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A3.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A49X.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3YB.01     4  0.3400     0.6703 0.00 0.18 0.00 0.82
#&gt; TCGA.IG.A3YC.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L7.A56G.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A51D.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.VR.A8EP.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88T.01     3  0.4790     0.3744 0.38 0.00 0.62 0.00
#&gt; TCGA.L5.A4ON.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A43J.01     1  0.4134     0.7101 0.74 0.00 0.00 0.26
#&gt; TCGA.L5.A43E.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OF.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A3I8.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.VR.AA7B.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3Y9.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49V.01     1  0.4855     0.4721 0.60 0.00 0.00 0.40
#&gt; TCGA.L5.A4OH.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OI.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A49R.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49K.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QT.01     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.R6.A6L4.01     2  0.4855     0.0944 0.00 0.60 0.00 0.40
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A7HX.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A8.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FG.01     4  0.3400     0.6703 0.00 0.18 0.00 0.82
#&gt; TCGA.L5.A4OJ.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RC.06     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A625.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     4  0.3853     0.5270 0.16 0.02 0.00 0.82
#&gt; TCGA.L5.A43H.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A50L.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HY.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49P.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A1.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49O.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.LN.A49W.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A43M.01     4  0.4277     0.5123 0.00 0.00 0.28 0.72
#&gt; TCGA.L5.A4OP.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.V5.A7RE.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.AA7I.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.IG.A3YA.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.11     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7D.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.V5.A7RB.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     4  0.4277     0.5123 0.00 0.00 0.28 0.72
#&gt; TCGA.IG.A3QL.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A2.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     2  0.4855     0.2092 0.00 0.60 0.00 0.40
#&gt; TCGA.LN.A49S.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OG.11     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A8O2.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A7DP.01     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NQ.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93F.01     4  0.4790     0.4611 0.00 0.38 0.00 0.62
#&gt; TCGA.M9.A5M8.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A8W5.01     4  0.4277     0.6737 0.00 0.28 0.00 0.72
#&gt; TCGA.L5.A8NH.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     1  0.3172     0.8189 0.84 0.00 0.00 0.16
#&gt; TCGA.IG.A5B8.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NN.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A9FP.01     3  0.1211     0.8600 0.04 0.00 0.96 0.00
#&gt; TCGA.LN.A4MR.01     1  0.1637     0.9104 0.94 0.00 0.00 0.06
#&gt; TCGA.L5.A8NS.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A9.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A938.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WG.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EU.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6L6.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NE.01     4  0.4277     0.6737 0.00 0.28 0.00 0.72
#&gt; TCGA.V5.AASX.11     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IC.A6RF.11     4  0.3400     0.6703 0.00 0.18 0.00 0.82
#&gt; TCGA.L5.A8NU.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6XQ.01     2  0.0707     0.9602 0.00 0.98 0.00 0.02
#&gt; TCGA.LN.A5U5.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.Z6.A8JD.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OT.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.ZR.A9CJ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.Z6.A8JE.01     4  0.4088     0.6536 0.04 0.14 0.00 0.82
#&gt; TCGA.JY.A6FH.01     4  0.5486     0.6794 0.00 0.20 0.08 0.72
#&gt; TCGA.XP.A8T6.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8W8.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A6QS.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.VR.A8Q7.01     3  0.2647     0.7892 0.00 0.00 0.88 0.12
#&gt; TCGA.R6.A6Y0.01     4  0.4277     0.5123 0.00 0.00 0.28 0.72
#&gt; TCGA.VR.A8EZ.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A891.01     4  0.5327     0.5949 0.00 0.06 0.22 0.72
#&gt; TCGA.L5.A8NM.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.XP.A8T7.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GO.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EW.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     4  0.5486     0.6145 0.00 0.08 0.20 0.72
#&gt; TCGA.VR.AA4G.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GN.01     4  0.4277     0.6737 0.00 0.28 0.00 0.72
#&gt; TCGA.VR.AA4D.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RE.11     3  0.4907     0.3290 0.42 0.00 0.58 0.00
#&gt; TCGA.IC.A6RE.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     4  0.4277     0.6737 0.00 0.28 0.00 0.72
#&gt; TCGA.LN.A5U6.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OS.01     3  0.0000     0.9075 0.00 0.00 1.00 0.00
#&gt; TCGA.RE.A7BO.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A939.01     2  0.4088     0.7296 0.00 0.82 0.14 0.04
#&gt; TCGA.VR.A8EY.01     4  0.3400     0.4975 0.18 0.00 0.00 0.82
#&gt; TCGA.Z6.A9VB.01     1  0.4277     0.6857 0.72 0.00 0.00 0.28
#&gt; TCGA.V5.AASV.01     4  0.3400     0.6703 0.00 0.18 0.00 0.82
#&gt; TCGA.LN.A9FR.01     1  0.0000     0.9577 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     4  0.4134     0.5299 0.00 0.00 0.26 0.74
#&gt; TCGA.L5.A8NL.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GH.01     2  0.0000     0.9838 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NF.01     4  0.4277     0.6737 0.00 0.28 0.00 0.72
#&gt; TCGA.L5.A8NI.01     4  0.5486     0.6795 0.00 0.20 0.08 0.72
</code></pre>

<script>
$('#tab-node-0-get-classes-3-a').parent().next().next().hide();
$('#tab-node-0-get-classes-3-a').click(function(){
  $('#tab-node-0-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0-get-classes-4'>
<p><a id='tab-node-0-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.JY.A6FB.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49L.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.LN.A4A4.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49M.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.Q9.A6FW.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.Z6.AAPN.01     3  0.4182      0.392 0.40 0.00 0.60 0.00 0.00
#&gt; TCGA.Q9.A6FU.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.S8.A6BW.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.S8.A6BV.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ET.01     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A3.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YB.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.IG.A3YC.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L7.A56G.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A51D.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.VR.A8EP.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88T.01     3  0.4126      0.415 0.38 0.00 0.62 0.00 0.00
#&gt; TCGA.L5.A4ON.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A43J.01     5  0.1410      0.860 0.06 0.00 0.00 0.00 0.94
#&gt; TCGA.L5.A43E.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.L5.A4OQ.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3I8.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.VR.AA7B.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3Y9.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49V.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A4OH.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49K.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QT.01     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6L4.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.L7.A6VZ.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A4A8.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FG.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A4OJ.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RC.06     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A625.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A43H.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A50L.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HY.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A49P.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49O.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.LN.A49W.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43M.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A4OP.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7I.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.IG.A3YA.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.11     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7D.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.V5.A7RB.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A3QL.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A2.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     5  0.3424      0.580 0.00 0.24 0.00 0.00 0.76
#&gt; TCGA.LN.A49S.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.11     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A8O2.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A7DP.01     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93F.01     5  0.3274      0.613 0.00 0.22 0.00 0.00 0.78
#&gt; TCGA.M9.A5M8.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8W5.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NH.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     5  0.3561      0.543 0.26 0.00 0.00 0.00 0.74
#&gt; TCGA.IG.A5B8.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NN.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A9FP.01     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4MR.01     1  0.3895      0.529 0.68 0.00 0.00 0.00 0.32
#&gt; TCGA.L5.A8NS.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A9.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0609      0.969 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.JY.A938.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WG.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EU.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6L6.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.L5.A8NE.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.11     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.11     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A8NU.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.R6.A6XQ.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A5U5.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Z6.A8JD.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OT.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.ZR.A9CJ.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.Z6.A8JE.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.JY.A6FH.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.XP.A8T6.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8W8.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A6QS.01     5  0.0609      0.913 0.02 0.00 0.00 0.00 0.98
#&gt; TCGA.VR.A8Q7.01     4  0.4262      0.239 0.00 0.00 0.44 0.56 0.00
#&gt; TCGA.R6.A6Y0.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A891.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T7.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A4OX.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GO.01     2  0.0609      0.982 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EW.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GN.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.AA4D.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RE.11     3  0.4227      0.339 0.42 0.00 0.58 0.00 0.00
#&gt; TCGA.IC.A6RE.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A5U6.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.3796      0.571 0.70 0.00 0.00 0.00 0.30
#&gt; TCGA.L5.A4OS.01     3  0.0000      0.889 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.RE.A7BO.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     2  0.1043      0.963 0.00 0.96 0.00 0.04 0.00
#&gt; TCGA.VR.A8EY.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.Z6.A9VB.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.V5.AASV.01     5  0.0000      0.936 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.LN.A9FR.01     1  0.0000      0.990 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GH.01     2  0.0000      0.997 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NF.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NI.01     4  0.0000      0.965 0.00 0.00 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-0-get-classes-4-a').parent().next().next().hide();
$('#tab-node-0-get-classes-4-a').click(function(){
  $('#tab-node-0-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0-get-classes-5'>
<p><a id='tab-node-0-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49L.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A4.01     1  0.0937     0.8166 0.96 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.LN.A49M.01     5  0.0547     0.9151 0.00 0.00 0.00 0.00 0.98 0.02
#&gt; TCGA.Q9.A6FW.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Z6.AAPN.01     6  0.2794     0.7668 0.08 0.00 0.06 0.00 0.00 0.86
#&gt; TCGA.Q9.A6FU.01     1  0.3499     0.5923 0.68 0.00 0.00 0.00 0.00 0.32
#&gt; TCGA.L5.A43C.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.S8.A6BW.01     1  0.2793     0.7090 0.80 0.00 0.00 0.00 0.00 0.20
#&gt; TCGA.S8.A6BV.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.0547     0.8267 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.VR.A8ET.01     3  0.3409     0.6826 0.00 0.00 0.70 0.00 0.00 0.30
#&gt; TCGA.LN.A4A3.01     6  0.3076     0.7889 0.24 0.00 0.00 0.00 0.00 0.76
#&gt; TCGA.L5.A4OH.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     6  0.2048     0.8033 0.12 0.00 0.00 0.00 0.00 0.88
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.2941     0.6791 0.78 0.00 0.00 0.00 0.00 0.22
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YB.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A3YC.01     6  0.2260     0.8097 0.14 0.00 0.00 0.00 0.00 0.86
#&gt; TCGA.L5.A4OE.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     6  0.2260     0.8097 0.14 0.00 0.00 0.00 0.00 0.86
#&gt; TCGA.L7.A56G.01     1  0.1267     0.8222 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.IG.A51D.01     5  0.0547     0.9151 0.00 0.00 0.00 0.00 0.98 0.02
#&gt; TCGA.VR.A8EP.01     1  0.1556     0.8140 0.92 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.L5.A88T.01     6  0.2728     0.7866 0.10 0.00 0.04 0.00 0.00 0.86
#&gt; TCGA.L5.A4ON.11     3  0.1267     0.9229 0.00 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.L5.A43J.01     5  0.4534     0.3598 0.04 0.00 0.00 0.00 0.58 0.38
#&gt; TCGA.L5.A43E.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.2793     0.7090 0.80 0.00 0.00 0.00 0.00 0.20
#&gt; TCGA.LN.A49N.01     6  0.3076     0.7465 0.24 0.00 0.00 0.00 0.00 0.76
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.L5.A4OQ.11     3  0.1267     0.9229 0.00 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.IG.A3I8.01     5  0.1807     0.8842 0.02 0.00 0.00 0.00 0.92 0.06
#&gt; TCGA.VR.AA7B.01     1  0.3309     0.6540 0.72 0.00 0.00 0.00 0.00 0.28
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3Y9.01     1  0.2793     0.7411 0.80 0.00 0.00 0.00 0.00 0.20
#&gt; TCGA.L5.A4OM.01     1  0.1556     0.8219 0.92 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.LN.A4A6.01     6  0.3198     0.7768 0.26 0.00 0.00 0.00 0.00 0.74
#&gt; TCGA.LN.A49V.01     5  0.1480     0.8961 0.02 0.00 0.00 0.00 0.94 0.04
#&gt; TCGA.L5.A4OH.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     1  0.1267     0.8171 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A49K.01     1  0.1267     0.8306 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.IG.A4QT.01     3  0.1267     0.9229 0.00 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.R6.A6L4.01     2  0.2190     0.9008 0.00 0.90 0.00 0.06 0.00 0.04
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     1  0.2260     0.7745 0.86 0.00 0.00 0.00 0.00 0.14
#&gt; TCGA.L5.A4OF.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     1  0.1814     0.8055 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.L5.A4OO.01     2  0.3073     0.8487 0.00 0.84 0.00 0.08 0.00 0.08
#&gt; TCGA.LN.A4A8.01     6  0.3309     0.7563 0.28 0.00 0.00 0.00 0.00 0.72
#&gt; TCGA.JY.A6FG.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A4OJ.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.2048     0.8173 0.88 0.00 0.00 0.00 0.00 0.12
#&gt; TCGA.V5.A7RC.06     1  0.0547     0.8267 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.IG.A625.01     1  0.2631     0.7335 0.82 0.00 0.00 0.00 0.00 0.18
#&gt; TCGA.L5.A4OP.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     1  0.3647     0.4210 0.64 0.00 0.00 0.00 0.00 0.36
#&gt; TCGA.LN.A49Y.01     1  0.3828     0.0974 0.56 0.00 0.00 0.00 0.00 0.44
#&gt; TCGA.L5.A43C.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A43H.01     1  0.0937     0.8296 0.96 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A4OE.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A50L.01     1  0.0547     0.8267 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.LN.A7HY.01     6  0.2631     0.8044 0.18 0.00 0.00 0.00 0.00 0.82
#&gt; TCGA.R6.A6KZ.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.LN.A49P.01     6  0.3309     0.7121 0.28 0.00 0.00 0.00 0.00 0.72
#&gt; TCGA.L5.A4OM.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     1  0.2793     0.7105 0.80 0.00 0.00 0.00 0.00 0.20
#&gt; TCGA.LN.A49O.01     1  0.2260     0.7946 0.86 0.00 0.00 0.00 0.00 0.14
#&gt; TCGA.LN.A4A5.01     6  0.4144     0.2101 0.02 0.00 0.00 0.00 0.36 0.62
#&gt; TCGA.LN.A49W.01     6  0.2631     0.8044 0.18 0.00 0.00 0.00 0.00 0.82
#&gt; TCGA.L5.A4OR.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43M.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OP.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7I.01     5  0.0547     0.9151 0.00 0.00 0.00 0.00 0.98 0.02
#&gt; TCGA.IG.A3YA.01     6  0.2260     0.8097 0.14 0.00 0.00 0.00 0.00 0.86
#&gt; TCGA.V5.A7RE.11     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.0937     0.8257 0.96 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.VR.AA7D.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.V5.A7RB.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3QL.01     1  0.2631     0.7524 0.82 0.00 0.00 0.00 0.00 0.18
#&gt; TCGA.R6.A6DQ.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     3  0.0937     0.9301 0.00 0.00 0.96 0.00 0.00 0.04
#&gt; TCGA.LN.A4A2.01     1  0.1814     0.8028 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.IC.A6RF.01     5  0.1267     0.8465 0.00 0.06 0.00 0.00 0.94 0.00
#&gt; TCGA.LN.A49S.01     6  0.3198     0.7755 0.26 0.00 0.00 0.00 0.00 0.74
#&gt; TCGA.IG.A4QS.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.11     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     1  0.0547     0.8267 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.IG.A8O2.01     1  0.3869     0.0507 0.50 0.00 0.00 0.00 0.00 0.50
#&gt; TCGA.IG.A7DP.01     3  0.3076     0.7889 0.00 0.00 0.76 0.00 0.00 0.24
#&gt; TCGA.L5.A8NQ.01     6  0.2260     0.8097 0.14 0.00 0.00 0.00 0.00 0.86
#&gt; TCGA.LN.A8I0.01     1  0.1814     0.8023 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.JY.A93F.01     5  0.0937     0.8750 0.00 0.04 0.00 0.00 0.96 0.00
#&gt; TCGA.M9.A5M8.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8W5.01     4  0.0937     0.9664 0.00 0.00 0.00 0.96 0.00 0.04
#&gt; TCGA.L5.A8NH.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.1814     0.8028 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.L5.A88Z.01     1  0.4926     0.4884 0.64 0.00 0.00 0.00 0.24 0.12
#&gt; TCGA.IG.A5B8.01     6  0.3309     0.7563 0.28 0.00 0.00 0.00 0.00 0.72
#&gt; TCGA.R6.A6XG.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NN.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.LN.A9FP.01     3  0.2793     0.8100 0.00 0.00 0.80 0.00 0.00 0.20
#&gt; TCGA.LN.A4MR.01     6  0.3045     0.7683 0.10 0.00 0.00 0.00 0.06 0.84
#&gt; TCGA.L5.A8NS.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.0547     0.8314 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.LN.A4A9.01     1  0.2454     0.7553 0.84 0.00 0.00 0.00 0.00 0.16
#&gt; TCGA.VR.A8EX.01     6  0.2793     0.7550 0.20 0.00 0.00 0.00 0.00 0.80
#&gt; TCGA.JY.A938.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     1  0.1267     0.8171 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.R6.A8WG.01     2  0.1556     0.9199 0.00 0.92 0.00 0.00 0.00 0.08
#&gt; TCGA.VR.A8EO.01     1  0.1267     0.8278 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.VR.A8EU.01     1  0.0937     0.8296 0.96 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.R6.A6L6.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.L5.A8NE.01     4  0.0547     0.9834 0.00 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.V5.AASX.11     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     1  0.0547     0.8314 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A893.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.11     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NU.01     2  0.3073     0.8487 0.00 0.84 0.00 0.08 0.00 0.08
#&gt; TCGA.R6.A6XQ.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.LN.A5U5.01     1  0.1267     0.8301 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.Z6.A8JD.01     6  0.2260     0.8097 0.14 0.00 0.00 0.00 0.00 0.86
#&gt; TCGA.L5.A4OT.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.ZR.A9CJ.01     2  0.1556     0.9199 0.00 0.92 0.00 0.00 0.00 0.08
#&gt; TCGA.Z6.A8JE.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.JY.A6FH.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     6  0.3797     0.2976 0.42 0.00 0.00 0.00 0.00 0.58
#&gt; TCGA.R6.A8W8.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A6QS.01     5  0.4328     0.2219 0.02 0.00 0.00 0.00 0.52 0.46
#&gt; TCGA.VR.A8Q7.01     6  0.5575    -0.0923 0.00 0.00 0.14 0.40 0.00 0.46
#&gt; TCGA.R6.A6Y0.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.1267     0.8171 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000     0.8280 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A891.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.1556     0.9199 0.00 0.92 0.00 0.00 0.00 0.08
#&gt; TCGA.XP.A8T7.01     5  0.1807     0.8842 0.02 0.00 0.00 0.00 0.92 0.06
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GO.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.L5.A8NR.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     6  0.2793     0.7987 0.20 0.00 0.00 0.00 0.00 0.80
#&gt; TCGA.VR.A8EW.01     1  0.3499     0.5007 0.68 0.00 0.00 0.00 0.00 0.32
#&gt; TCGA.VR.A8ER.01     1  0.0547     0.8314 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A4OU.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     1  0.0547     0.8267 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NT.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.2941     0.7130 0.78 0.00 0.00 0.00 0.00 0.22
#&gt; TCGA.JY.A6FD.01     6  0.3828     0.2171 0.44 0.00 0.00 0.00 0.00 0.56
#&gt; TCGA.2H.A9GN.01     4  0.0547     0.9834 0.00 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.VR.AA4D.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     1  0.1814     0.8047 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.2H.A9GM.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     1  0.3198     0.6607 0.74 0.00 0.00 0.00 0.00 0.26
#&gt; TCGA.IC.A6RE.11     6  0.2956     0.7877 0.12 0.00 0.04 0.00 0.00 0.84
#&gt; TCGA.IC.A6RE.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A5U6.01     1  0.0937     0.8296 0.96 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.LN.A9FQ.01     1  0.0547     0.8314 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NK.01     6  0.5265     0.2319 0.40 0.00 0.00 0.00 0.10 0.50
#&gt; TCGA.L5.A4OS.01     3  0.0000     0.9406 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.RE.A7BO.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     6  0.3499     0.6886 0.32 0.00 0.00 0.00 0.00 0.68
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     2  0.3321     0.8278 0.00 0.82 0.00 0.10 0.00 0.08
#&gt; TCGA.VR.A8EY.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.Z6.A9VB.01     5  0.1480     0.8961 0.02 0.00 0.00 0.00 0.94 0.04
#&gt; TCGA.V5.AASV.01     5  0.0000     0.9181 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A9FR.01     1  0.3706     0.4049 0.62 0.00 0.00 0.00 0.00 0.38
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GH.01     2  0.0000     0.9753 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NF.01     4  0.0547     0.9834 0.00 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.L5.A8NI.01     4  0.0000     0.9919 0.00 0.00 0.00 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-0-get-classes-5-a').parent().next().next().hide();
$('#tab-node-0-get-classes-5-a').click(function(){
  $('#tab-node-0-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0-get-classes-6'>
<p><a id='tab-node-0-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49L.01     5  0.0504     0.8313 0.00 0.00 0.00 0.00 0.98 0.02 0.00
#&gt; TCGA.LN.A4A4.01     1  0.1928     0.5235 0.90 0.00 0.00 0.00 0.00 0.02 0.08
#&gt; TCGA.LN.A49M.01     5  0.1664     0.8211 0.00 0.00 0.00 0.00 0.92 0.02 0.06
#&gt; TCGA.Q9.A6FW.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Z6.AAPN.01     6  0.0863     0.6578 0.00 0.00 0.04 0.00 0.00 0.96 0.00
#&gt; TCGA.Q9.A6FU.01     1  0.5073     0.0291 0.54 0.00 0.00 0.00 0.00 0.16 0.30
#&gt; TCGA.L5.A43C.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.S8.A6BW.01     1  0.4698    -0.1928 0.62 0.00 0.00 0.00 0.00 0.14 0.24
#&gt; TCGA.S8.A6BV.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.0504     0.5774 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.VR.A8ET.01     6  0.3413    -0.0311 0.00 0.00 0.38 0.00 0.00 0.62 0.00
#&gt; TCGA.LN.A4A3.01     6  0.4630     0.2718 0.12 0.00 0.00 0.00 0.00 0.62 0.26
#&gt; TCGA.L5.A4OH.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.4714    -0.2511 0.60 0.00 0.00 0.00 0.00 0.12 0.28
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YB.01     5  0.0504     0.8289 0.00 0.00 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.IG.A3YC.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.L5.A4OE.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.L7.A56G.01     1  0.3086     0.3711 0.80 0.00 0.00 0.00 0.00 0.04 0.16
#&gt; TCGA.IG.A51D.01     5  0.2278     0.8099 0.00 0.00 0.00 0.00 0.88 0.04 0.08
#&gt; TCGA.VR.A8EP.01     1  0.3417     0.1752 0.72 0.00 0.00 0.00 0.00 0.02 0.26
#&gt; TCGA.L5.A88T.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.L5.A4ON.11     3  0.2708     0.7865 0.00 0.00 0.78 0.00 0.00 0.22 0.00
#&gt; TCGA.L5.A43J.01     5  0.6450     0.2823 0.12 0.00 0.00 0.00 0.46 0.26 0.16
#&gt; TCGA.L5.A43E.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.4338    -0.0829 0.64 0.00 0.00 0.00 0.00 0.08 0.28
#&gt; TCGA.LN.A49N.01     6  0.4993     0.3395 0.24 0.00 0.00 0.00 0.02 0.62 0.12
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.01     2  0.4191     0.6140 0.00 0.64 0.00 0.06 0.00 0.00 0.30
#&gt; TCGA.L5.A4OQ.11     3  0.2708     0.7865 0.00 0.00 0.78 0.00 0.00 0.22 0.00
#&gt; TCGA.IG.A3I8.01     5  0.3047     0.7213 0.00 0.00 0.00 0.00 0.72 0.00 0.28
#&gt; TCGA.VR.AA7B.01     1  0.4649     0.1726 0.62 0.00 0.00 0.00 0.02 0.06 0.30
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3Y9.01     1  0.2572     0.3353 0.80 0.00 0.00 0.00 0.00 0.20 0.00
#&gt; TCGA.L5.A4OM.01     1  0.2832     0.3693 0.76 0.00 0.00 0.00 0.00 0.00 0.24
#&gt; TCGA.LN.A4A6.01     6  0.4714     0.2364 0.12 0.00 0.00 0.00 0.00 0.60 0.28
#&gt; TCGA.LN.A49V.01     5  0.3315     0.7688 0.08 0.00 0.00 0.00 0.82 0.02 0.08
#&gt; TCGA.L5.A4OH.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49K.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QT.01     3  0.2945     0.7499 0.00 0.00 0.74 0.00 0.00 0.26 0.00
#&gt; TCGA.R6.A6L4.01     2  0.2803     0.8231 0.00 0.84 0.00 0.06 0.00 0.00 0.10
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     1  0.4108    -0.0219 0.66 0.00 0.00 0.00 0.00 0.06 0.28
#&gt; TCGA.L5.A4OF.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     1  0.3841     0.0529 0.68 0.00 0.00 0.00 0.00 0.04 0.28
#&gt; TCGA.L5.A4OO.01     2  0.3927     0.6412 0.00 0.66 0.00 0.04 0.00 0.00 0.30
#&gt; TCGA.LN.A4A8.01     6  0.4714     0.2364 0.12 0.00 0.00 0.00 0.00 0.60 0.28
#&gt; TCGA.JY.A6FG.01     5  0.1886     0.8119 0.00 0.00 0.00 0.00 0.88 0.00 0.12
#&gt; TCGA.L5.A4OJ.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.2512     0.4954 0.86 0.00 0.00 0.00 0.00 0.04 0.10
#&gt; TCGA.V5.A7RC.06     1  0.0504     0.5774 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.IG.A625.01     1  0.4338    -0.0829 0.64 0.00 0.00 0.00 0.00 0.08 0.28
#&gt; TCGA.L5.A4OP.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     1  0.3358    -0.0682 0.64 0.00 0.00 0.00 0.00 0.36 0.00
#&gt; TCGA.LN.A49Y.01     7  0.5829     0.0000 0.38 0.00 0.00 0.00 0.02 0.20 0.40
#&gt; TCGA.L5.A43C.01     2  0.0504     0.9315 0.00 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A88W.01     5  0.1886     0.8119 0.00 0.00 0.00 0.00 0.88 0.00 0.12
#&gt; TCGA.L5.A43H.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A50L.01     1  0.1166     0.5557 0.94 0.00 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A7HY.01     6  0.3315     0.6209 0.08 0.00 0.00 0.00 0.02 0.82 0.08
#&gt; TCGA.R6.A6KZ.01     2  0.4191     0.6140 0.00 0.64 0.00 0.06 0.00 0.00 0.30
#&gt; TCGA.LN.A49P.01     6  0.4908     0.3387 0.26 0.00 0.00 0.00 0.02 0.62 0.10
#&gt; TCGA.L5.A4OM.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     1  0.4714    -0.2511 0.60 0.00 0.00 0.00 0.00 0.12 0.28
#&gt; TCGA.LN.A49O.01     1  0.1718     0.5359 0.92 0.00 0.00 0.00 0.00 0.04 0.04
#&gt; TCGA.LN.A4A5.01     6  0.4699     0.4758 0.06 0.00 0.00 0.00 0.24 0.66 0.04
#&gt; TCGA.LN.A49W.01     6  0.2769     0.6470 0.04 0.00 0.00 0.00 0.02 0.86 0.08
#&gt; TCGA.L5.A4OR.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43M.01     4  0.1433     0.9315 0.00 0.00 0.00 0.92 0.00 0.00 0.08
#&gt; TCGA.L5.A4OP.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7I.01     5  0.2572     0.7953 0.00 0.00 0.00 0.00 0.86 0.08 0.06
#&gt; TCGA.IG.A3YA.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.V5.A7RE.11     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.2376     0.4747 0.86 0.00 0.00 0.00 0.00 0.02 0.12
#&gt; TCGA.VR.AA7D.01     5  0.0000     0.8319 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.A7RB.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3QL.01     1  0.3566     0.3707 0.78 0.00 0.00 0.00 0.02 0.04 0.16
#&gt; TCGA.R6.A6DQ.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     3  0.2081     0.8323 0.00 0.00 0.86 0.00 0.00 0.14 0.00
#&gt; TCGA.LN.A4A2.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     5  0.2722     0.7827 0.00 0.04 0.00 0.00 0.84 0.00 0.12
#&gt; TCGA.LN.A49S.01     6  0.4630     0.2836 0.12 0.00 0.00 0.00 0.00 0.62 0.26
#&gt; TCGA.IG.A4QS.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.11     3  0.0000     0.8779 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     1  0.1886     0.4963 0.88 0.00 0.00 0.00 0.00 0.00 0.12
#&gt; TCGA.IG.A8O2.01     1  0.6084    -0.4021 0.52 0.00 0.00 0.00 0.08 0.22 0.18
#&gt; TCGA.IG.A7DP.01     3  0.5375     0.4696 0.00 0.00 0.46 0.00 0.00 0.34 0.20
#&gt; TCGA.L5.A8NQ.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.LN.A8I0.01     1  0.3637     0.1744 0.72 0.00 0.00 0.00 0.00 0.04 0.24
#&gt; TCGA.JY.A93F.01     5  0.2722     0.7827 0.00 0.04 0.00 0.00 0.84 0.00 0.12
#&gt; TCGA.M9.A5M8.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8W5.01     4  0.1166     0.9533 0.00 0.00 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.L5.A8NH.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.0863     0.5623 0.96 0.00 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A88Z.01     1  0.5402    -0.0235 0.48 0.00 0.00 0.00 0.24 0.00 0.28
#&gt; TCGA.IG.A5B8.01     6  0.4714     0.2364 0.12 0.00 0.00 0.00 0.00 0.60 0.28
#&gt; TCGA.R6.A6XG.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NN.01     2  0.4615     0.5497 0.00 0.60 0.00 0.10 0.00 0.00 0.30
#&gt; TCGA.LN.A9FP.01     3  0.3558     0.3569 0.00 0.00 0.52 0.00 0.00 0.48 0.00
#&gt; TCGA.LN.A4MR.01     6  0.5130     0.4864 0.04 0.00 0.00 0.00 0.14 0.64 0.18
#&gt; TCGA.L5.A8NS.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A9.01     1  0.4714    -0.2497 0.60 0.00 0.00 0.00 0.00 0.12 0.28
#&gt; TCGA.VR.A8EX.01     6  0.5455     0.4412 0.18 0.00 0.00 0.00 0.08 0.62 0.12
#&gt; TCGA.JY.A938.01     2  0.0504     0.9315 0.00 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.JY.A6FA.01     1  0.0863     0.5677 0.96 0.00 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.R6.A8WG.01     2  0.3139     0.6899 0.00 0.70 0.00 0.00 0.00 0.00 0.30
#&gt; TCGA.VR.A8EO.01     1  0.2163     0.5218 0.88 0.00 0.00 0.00 0.00 0.02 0.10
#&gt; TCGA.VR.A8EU.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6L6.01     2  0.4418     0.5834 0.00 0.62 0.00 0.08 0.00 0.00 0.30
#&gt; TCGA.L5.A8NE.01     4  0.0863     0.9649 0.00 0.00 0.00 0.96 0.00 0.00 0.04
#&gt; TCGA.V5.AASX.11     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     1  0.0504     0.5774 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A893.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.11     5  0.1886     0.8119 0.00 0.00 0.00 0.00 0.88 0.00 0.12
#&gt; TCGA.L5.A8NU.01     2  0.4191     0.6140 0.00 0.64 0.00 0.06 0.00 0.00 0.30
#&gt; TCGA.R6.A6XQ.01     2  0.4348     0.6479 0.00 0.68 0.00 0.14 0.00 0.00 0.18
#&gt; TCGA.LN.A5U5.01     1  0.0863     0.5695 0.96 0.00 0.00 0.00 0.00 0.00 0.04
#&gt; TCGA.Z6.A8JD.01     6  0.0504     0.6785 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.L5.A4OT.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.ZR.A9CJ.01     2  0.3047     0.7116 0.00 0.72 0.00 0.00 0.00 0.00 0.28
#&gt; TCGA.Z6.A8JE.01     5  0.0000     0.8319 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A6FH.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     1  0.5438    -0.2810 0.44 0.00 0.00 0.00 0.02 0.42 0.12
#&gt; TCGA.R6.A8W8.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A6QS.01     5  0.5606     0.1593 0.06 0.00 0.00 0.00 0.48 0.38 0.08
#&gt; TCGA.VR.A8Q7.01     6  0.5451     0.1749 0.00 0.00 0.16 0.28 0.00 0.54 0.02
#&gt; TCGA.R6.A6Y0.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.1433     0.5440 0.92 0.00 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.L5.A891.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.3047     0.7116 0.00 0.72 0.00 0.00 0.00 0.00 0.28
#&gt; TCGA.XP.A8T7.01     5  0.3841     0.6870 0.00 0.00 0.00 0.00 0.68 0.04 0.28
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GO.01     2  0.4418     0.5834 0.00 0.62 0.00 0.08 0.00 0.00 0.30
#&gt; TCGA.L5.A8NR.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     6  0.3985     0.5095 0.10 0.00 0.00 0.00 0.00 0.72 0.18
#&gt; TCGA.VR.A8EW.01     1  0.5164    -0.4992 0.54 0.00 0.00 0.00 0.00 0.20 0.26
#&gt; TCGA.VR.A8ER.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.0504     0.9315 0.00 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.JY.A93C.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     1  0.1433     0.5440 0.92 0.00 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.L5.A8NT.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.4870     0.1179 0.58 0.00 0.00 0.00 0.00 0.14 0.28
#&gt; TCGA.JY.A6FD.01     1  0.6022    -0.2516 0.36 0.00 0.00 0.00 0.02 0.30 0.32
#&gt; TCGA.2H.A9GN.01     4  0.0863     0.9649 0.00 0.00 0.00 0.96 0.00 0.00 0.04
#&gt; TCGA.VR.AA4D.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     1  0.1363     0.5480 0.94 0.00 0.00 0.00 0.00 0.02 0.04
#&gt; TCGA.2H.A9GM.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     1  0.5377     0.0700 0.56 0.00 0.00 0.00 0.02 0.16 0.26
#&gt; TCGA.IC.A6RE.11     6  0.1505     0.6628 0.02 0.00 0.02 0.00 0.00 0.94 0.02
#&gt; TCGA.IC.A6RE.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U6.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     1  0.0000     0.5822 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.6957    -0.1521 0.34 0.00 0.00 0.00 0.20 0.18 0.28
#&gt; TCGA.L5.A4OS.01     3  0.1166     0.8641 0.00 0.00 0.94 0.00 0.00 0.06 0.00
#&gt; TCGA.RE.A7BO.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     6  0.5410    -0.3595 0.26 0.00 0.00 0.00 0.00 0.48 0.26
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     2  0.4191     0.6140 0.00 0.64 0.00 0.06 0.00 0.00 0.30
#&gt; TCGA.VR.A8EY.01     5  0.1433     0.8208 0.00 0.00 0.00 0.00 0.92 0.00 0.08
#&gt; TCGA.Z6.A9VB.01     5  0.3396     0.7719 0.02 0.00 0.00 0.00 0.80 0.04 0.14
#&gt; TCGA.V5.AASV.01     5  0.1886     0.8119 0.00 0.00 0.00 0.00 0.88 0.00 0.12
#&gt; TCGA.LN.A9FR.01     1  0.3685    -0.0330 0.66 0.00 0.00 0.00 0.00 0.32 0.02
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0504     0.9315 0.00 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.2H.A9GH.01     2  0.0000     0.9440 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NF.01     4  0.1166     0.9533 0.00 0.00 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.L5.A8NI.01     4  0.0000     0.9772 0.00 0.00 0.00 1.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-0-get-classes-6-a').parent().next().next().hide();
$('#tab-node-0-get-classes-6-a').click(function(){
  $('#tab-node-0-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0-get-classes-7'>
<p><a id='tab-node-0-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.JY.A6FB.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49L.01     5  0.0941    0.71329 0.00 0.00 0.00 0.00 0.96 0.00 0.02 0.02
#&gt; TCGA.LN.A4A4.01     1  0.3272   -0.07108 0.58 0.00 0.00 0.00 0.00 0.00 0.42 0.00
#&gt; TCGA.LN.A49M.01     5  0.1275    0.70207 0.00 0.00 0.00 0.00 0.94 0.00 0.04 0.02
#&gt; TCGA.Q9.A6FW.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Z6.AAPN.01     6  0.0941    0.70553 0.02 0.00 0.02 0.00 0.00 0.96 0.00 0.00
#&gt; TCGA.Q9.A6FU.01     7  0.5563    0.26949 0.18 0.00 0.00 0.00 0.00 0.10 0.56 0.16
#&gt; TCGA.L5.A43C.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.S8.A6BW.01     1  0.2818    0.40099 0.82 0.00 0.00 0.00 0.00 0.06 0.12 0.00
#&gt; TCGA.S8.A6BV.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.3714   -0.13323 0.54 0.00 0.00 0.00 0.00 0.00 0.44 0.02
#&gt; TCGA.VR.A8ET.01     6  0.2267    0.54206 0.00 0.00 0.18 0.00 0.00 0.82 0.00 0.00
#&gt; TCGA.LN.A4A3.01     1  0.3237    0.01434 0.60 0.00 0.00 0.00 0.00 0.40 0.00 0.00
#&gt; TCGA.L5.A4OH.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.1091    0.43928 0.94 0.00 0.00 0.00 0.00 0.06 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YB.01     5  0.1275    0.71559 0.00 0.00 0.00 0.00 0.94 0.02 0.00 0.04
#&gt; TCGA.IG.A3YC.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.L5.A4OE.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.L7.A56G.01     1  0.3880    0.12087 0.64 0.00 0.00 0.00 0.00 0.02 0.32 0.02
#&gt; TCGA.IG.A51D.01     5  0.1091    0.70362 0.00 0.00 0.00 0.00 0.94 0.00 0.06 0.00
#&gt; TCGA.VR.A8EP.01     1  0.2981    0.29631 0.76 0.00 0.00 0.00 0.00 0.02 0.22 0.00
#&gt; TCGA.L5.A88T.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.L5.A4ON.11     3  0.2756    0.72521 0.00 0.00 0.74 0.00 0.00 0.26 0.00 0.00
#&gt; TCGA.L5.A43J.01     5  0.5751    0.26199 0.00 0.00 0.00 0.00 0.46 0.18 0.30 0.06
#&gt; TCGA.L5.A43E.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.1275    0.44164 0.94 0.00 0.00 0.00 0.00 0.04 0.02 0.00
#&gt; TCGA.LN.A49N.01     6  0.6637    0.39853 0.12 0.00 0.00 0.00 0.16 0.44 0.24 0.04
#&gt; TCGA.L5.A4ON.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.L5.A4OQ.11     3  0.2756    0.72521 0.00 0.00 0.74 0.00 0.00 0.26 0.00 0.00
#&gt; TCGA.IG.A3I8.01     5  0.4693    0.42480 0.00 0.00 0.00 0.00 0.46 0.00 0.42 0.12
#&gt; TCGA.VR.AA7B.01     7  0.4337    0.36078 0.10 0.00 0.00 0.00 0.00 0.04 0.70 0.16
#&gt; TCGA.L5.A4OJ.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3Y9.01     7  0.4554    0.18465 0.42 0.00 0.00 0.00 0.00 0.10 0.48 0.00
#&gt; TCGA.L5.A4OM.01     7  0.3934    0.36406 0.16 0.00 0.00 0.00 0.00 0.00 0.70 0.14
#&gt; TCGA.LN.A4A6.01     1  0.3658   -0.03875 0.58 0.00 0.00 0.00 0.00 0.40 0.00 0.02
#&gt; TCGA.LN.A49V.01     5  0.3808    0.54839 0.00 0.00 0.00 0.00 0.62 0.00 0.34 0.04
#&gt; TCGA.L5.A4OH.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     7  0.3333    0.17204 0.50 0.00 0.00 0.00 0.00 0.00 0.50 0.00
#&gt; TCGA.LN.A49K.01     7  0.3737    0.21348 0.48 0.00 0.00 0.00 0.00 0.02 0.50 0.00
#&gt; TCGA.IG.A4QT.01     3  0.3142    0.57010 0.00 0.00 0.64 0.00 0.00 0.36 0.00 0.00
#&gt; TCGA.R6.A6L4.01     2  0.3660    0.08266 0.00 0.70 0.00 0.06 0.00 0.00 0.00 0.24
#&gt; TCGA.L7.A6VZ.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     1  0.0471    0.44417 0.98 0.00 0.00 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A4OF.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     1  0.0471    0.43133 0.98 0.00 0.00 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A4OO.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.LN.A4A8.01     1  0.3237    0.01434 0.60 0.00 0.00 0.00 0.00 0.40 0.00 0.00
#&gt; TCGA.JY.A6FG.01     5  0.3913    0.68700 0.00 0.00 0.00 0.00 0.74 0.04 0.06 0.16
#&gt; TCGA.L5.A4OJ.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     7  0.4770    0.28241 0.40 0.00 0.00 0.00 0.04 0.02 0.52 0.02
#&gt; TCGA.V5.A7RC.06     1  0.3714   -0.13323 0.54 0.00 0.00 0.00 0.00 0.00 0.44 0.02
#&gt; TCGA.IG.A625.01     1  0.1275    0.43802 0.94 0.00 0.00 0.00 0.00 0.02 0.04 0.00
#&gt; TCGA.L5.A4OP.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     1  0.5270    0.00575 0.36 0.00 0.00 0.00 0.00 0.30 0.34 0.00
#&gt; TCGA.LN.A49Y.01     1  0.4134    0.35207 0.76 0.00 0.00 0.00 0.02 0.08 0.08 0.06
#&gt; TCGA.L5.A43C.01     2  0.0471    0.95868 0.00 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A88W.01     5  0.3913    0.68700 0.00 0.00 0.00 0.00 0.74 0.04 0.06 0.16
#&gt; TCGA.L5.A43H.01     7  0.3318    0.25158 0.46 0.00 0.00 0.00 0.00 0.00 0.54 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A50L.01     1  0.3299   -0.07977 0.56 0.00 0.00 0.00 0.00 0.00 0.44 0.00
#&gt; TCGA.LN.A7HY.01     6  0.5241    0.59282 0.10 0.00 0.00 0.00 0.08 0.66 0.12 0.04
#&gt; TCGA.R6.A6KZ.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.LN.A49P.01     6  0.6347    0.34505 0.06 0.00 0.00 0.00 0.16 0.42 0.32 0.04
#&gt; TCGA.L5.A4OM.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     1  0.0941    0.44310 0.96 0.00 0.00 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.LN.A49O.01     7  0.4702    0.34104 0.36 0.00 0.00 0.00 0.04 0.02 0.56 0.02
#&gt; TCGA.LN.A4A5.01     6  0.4779    0.40737 0.00 0.00 0.00 0.00 0.28 0.60 0.08 0.04
#&gt; TCGA.LN.A49W.01     6  0.4428    0.63146 0.14 0.00 0.00 0.00 0.02 0.72 0.08 0.04
#&gt; TCGA.L5.A4OR.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43M.01     4  0.1765    0.89119 0.00 0.00 0.00 0.88 0.00 0.00 0.00 0.12
#&gt; TCGA.L5.A4OP.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7I.01     5  0.3421    0.61744 0.00 0.00 0.00 0.00 0.80 0.08 0.08 0.04
#&gt; TCGA.IG.A3YA.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.V5.A7RE.11     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.2938    0.18790 0.70 0.00 0.00 0.00 0.00 0.00 0.30 0.00
#&gt; TCGA.VR.AA7D.01     5  0.0808    0.70756 0.00 0.00 0.00 0.00 0.96 0.00 0.04 0.00
#&gt; TCGA.V5.A7RB.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     4  0.0471    0.95932 0.00 0.00 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.IG.A3QL.01     7  0.4684    0.38654 0.14 0.00 0.00 0.00 0.06 0.02 0.70 0.08
#&gt; TCGA.R6.A6DQ.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     3  0.2114    0.81799 0.00 0.00 0.84 0.00 0.00 0.16 0.00 0.00
#&gt; TCGA.LN.A4A2.01     7  0.3880    0.37255 0.32 0.00 0.00 0.00 0.02 0.00 0.64 0.02
#&gt; TCGA.IC.A6RF.01     5  0.4661    0.65717 0.00 0.04 0.00 0.00 0.70 0.04 0.06 0.16
#&gt; TCGA.LN.A49S.01     1  0.3237    0.01434 0.60 0.00 0.00 0.00 0.00 0.40 0.00 0.00
#&gt; TCGA.IG.A4QS.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.11     3  0.0000    0.90923 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     1  0.3193    0.03671 0.62 0.00 0.00 0.00 0.00 0.00 0.38 0.00
#&gt; TCGA.IG.A8O2.01     1  0.6950   -0.08190 0.36 0.00 0.00 0.00 0.20 0.10 0.28 0.06
#&gt; TCGA.IG.A7DP.01     6  0.4998    0.09681 0.00 0.00 0.24 0.00 0.00 0.50 0.00 0.26
#&gt; TCGA.L5.A8NQ.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0808    0.43165 0.96 0.00 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.JY.A93F.01     5  0.4355    0.67457 0.00 0.02 0.00 0.00 0.72 0.04 0.06 0.16
#&gt; TCGA.M9.A5M8.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8W5.01     4  0.1341    0.93238 0.00 0.00 0.00 0.92 0.00 0.00 0.00 0.08
#&gt; TCGA.L5.A8NH.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T8.01     7  0.3514    0.36589 0.34 0.00 0.00 0.00 0.00 0.00 0.64 0.02
#&gt; TCGA.L5.A88Z.01     7  0.3314    0.34479 0.02 0.00 0.00 0.00 0.10 0.00 0.80 0.08
#&gt; TCGA.IG.A5B8.01     1  0.3237    0.01434 0.60 0.00 0.00 0.00 0.00 0.40 0.00 0.00
#&gt; TCGA.R6.A6XG.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NN.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.LN.A9FP.01     6  0.3299   -0.09868 0.00 0.00 0.44 0.00 0.00 0.56 0.00 0.00
#&gt; TCGA.LN.A4MR.01     6  0.6929    0.28283 0.18 0.00 0.00 0.00 0.24 0.38 0.16 0.04
#&gt; TCGA.L5.A8NS.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4MQ.01     7  0.3329    0.22452 0.48 0.00 0.00 0.00 0.00 0.00 0.52 0.00
#&gt; TCGA.LN.A4A9.01     1  0.0471    0.44417 0.98 0.00 0.00 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.VR.A8EX.01     6  0.6675    0.26168 0.08 0.00 0.00 0.00 0.22 0.38 0.28 0.04
#&gt; TCGA.JY.A938.01     2  0.0471    0.95850 0.00 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.JY.A6FA.01     1  0.3329   -0.19186 0.52 0.00 0.00 0.00 0.00 0.00 0.48 0.00
#&gt; TCGA.R6.A8WG.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.VR.A8EO.01     1  0.4358   -0.10063 0.54 0.00 0.00 0.00 0.00 0.02 0.40 0.04
#&gt; TCGA.VR.A8EU.01     7  0.3329    0.22452 0.48 0.00 0.00 0.00 0.00 0.00 0.52 0.00
#&gt; TCGA.R6.A6L6.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.L5.A8NE.01     4  0.1091    0.94458 0.00 0.00 0.00 0.94 0.00 0.00 0.00 0.06
#&gt; TCGA.V5.AASX.11     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     7  0.3329    0.22452 0.48 0.00 0.00 0.00 0.00 0.00 0.52 0.00
#&gt; TCGA.L5.A893.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.11     5  0.3913    0.68700 0.00 0.00 0.00 0.00 0.74 0.04 0.06 0.16
#&gt; TCGA.L5.A8NU.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.R6.A6XQ.01     8  0.4008    0.78275 0.00 0.48 0.00 0.04 0.00 0.00 0.00 0.48
#&gt; TCGA.LN.A5U5.01     1  0.3299   -0.08515 0.56 0.00 0.00 0.00 0.00 0.00 0.44 0.00
#&gt; TCGA.Z6.A8JD.01     6  0.0941    0.72067 0.02 0.00 0.00 0.00 0.00 0.96 0.02 0.00
#&gt; TCGA.L5.A4OT.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.ZR.A9CJ.01     8  0.3237    0.95463 0.00 0.40 0.00 0.00 0.00 0.00 0.00 0.60
#&gt; TCGA.Z6.A8JE.01     5  0.1804    0.71609 0.00 0.00 0.00 0.00 0.90 0.00 0.02 0.08
#&gt; TCGA.JY.A6FH.01     4  0.0471    0.95932 0.00 0.00 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.XP.A8T6.01     7  0.6523    0.22102 0.22 0.00 0.00 0.00 0.14 0.18 0.44 0.02
#&gt; TCGA.R6.A8W8.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A6QS.01     5  0.5727    0.05848 0.00 0.00 0.00 0.00 0.42 0.32 0.22 0.04
#&gt; TCGA.VR.A8Q7.01     6  0.4074    0.45824 0.00 0.00 0.02 0.26 0.00 0.68 0.02 0.02
#&gt; TCGA.R6.A6Y0.01     4  0.0471    0.95932 0.00 0.00 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.VR.A8EZ.01     7  0.3329    0.22452 0.48 0.00 0.00 0.00 0.00 0.00 0.52 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.3318   -0.12418 0.54 0.00 0.00 0.00 0.00 0.00 0.46 0.00
#&gt; TCGA.L5.A891.01     4  0.0471    0.95932 0.00 0.00 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     8  0.3237    0.95463 0.00 0.40 0.00 0.00 0.00 0.00 0.00 0.60
#&gt; TCGA.XP.A8T7.01     5  0.4554    0.44315 0.00 0.00 0.00 0.00 0.48 0.00 0.42 0.10
#&gt; TCGA.L5.A4OX.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GO.01     8  0.3193    0.97401 0.00 0.38 0.00 0.00 0.00 0.00 0.00 0.62
#&gt; TCGA.L5.A8NR.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     6  0.4350    0.44082 0.30 0.00 0.00 0.00 0.00 0.62 0.06 0.02
#&gt; TCGA.VR.A8EW.01     1  0.2224    0.42966 0.86 0.00 0.00 0.00 0.00 0.12 0.02 0.00
#&gt; TCGA.VR.A8ER.01     1  0.3333   -0.21563 0.50 0.00 0.00 0.00 0.00 0.00 0.50 0.00
#&gt; TCGA.L5.A4OU.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     1  0.3272   -0.04254 0.58 0.00 0.00 0.00 0.00 0.00 0.42 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     4  0.0471    0.95932 0.00 0.00 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.VR.AA4G.01     7  0.4808    0.34620 0.08 0.00 0.00 0.00 0.00 0.10 0.66 0.16
#&gt; TCGA.JY.A6FD.01     7  0.5948    0.09875 0.20 0.00 0.00 0.00 0.00 0.14 0.50 0.16
#&gt; TCGA.2H.A9GN.01     4  0.1091    0.94458 0.00 0.00 0.00 0.94 0.00 0.00 0.00 0.06
#&gt; TCGA.VR.AA4D.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     7  0.3514    0.35687 0.34 0.00 0.00 0.00 0.00 0.02 0.64 0.00
#&gt; TCGA.2H.A9GM.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     7  0.4764    0.32651 0.06 0.00 0.00 0.00 0.00 0.12 0.66 0.16
#&gt; TCGA.IC.A6RE.11     6  0.0941    0.70553 0.02 0.00 0.02 0.00 0.00 0.96 0.00 0.00
#&gt; TCGA.IC.A6RE.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     4  0.0000    0.95841 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U6.01     7  0.3329    0.22452 0.48 0.00 0.00 0.00 0.00 0.00 0.52 0.00
#&gt; TCGA.LN.A9FQ.01     7  0.3329    0.22452 0.48 0.00 0.00 0.00 0.00 0.00 0.52 0.00
#&gt; TCGA.L5.A8NK.01     7  0.6077   -0.07453 0.02 0.00 0.00 0.00 0.20 0.10 0.52 0.16
#&gt; TCGA.L5.A4OS.01     3  0.1091    0.88258 0.00 0.00 0.94 0.00 0.00 0.06 0.00 0.00
#&gt; TCGA.RE.A7BO.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.2938    0.24403 0.70 0.00 0.00 0.00 0.00 0.30 0.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     8  0.3570    0.94522 0.00 0.36 0.00 0.02 0.00 0.00 0.00 0.62
#&gt; TCGA.VR.A8EY.01     5  0.3758    0.69164 0.00 0.00 0.00 0.00 0.76 0.04 0.06 0.14
#&gt; TCGA.Z6.A9VB.01     5  0.3594    0.57115 0.00 0.00 0.00 0.00 0.68 0.00 0.28 0.04
#&gt; TCGA.V5.AASV.01     5  0.3913    0.68700 0.00 0.00 0.00 0.00 0.74 0.04 0.06 0.16
#&gt; TCGA.LN.A9FR.01     1  0.5305    0.09938 0.50 0.00 0.00 0.00 0.00 0.20 0.28 0.02
#&gt; TCGA.JY.A6F8.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     4  0.0941    0.95461 0.00 0.00 0.00 0.96 0.00 0.00 0.02 0.02
#&gt; TCGA.L5.A8NL.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GH.01     2  0.0000    0.99107 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NF.01     4  0.1091    0.94458 0.00 0.00 0.00 0.94 0.00 0.00 0.00 0.06
#&gt; TCGA.L5.A8NI.01     4  0.0000    0.95841 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-0-get-classes-7-a').parent().next().next().hide();
$('#tab-node-0-get-classes-7-a').click(function(){
  $('#tab-node-0-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-0-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-0-consensus-heatmap'>
<ul>
<li><a href='#tab-node-0-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-0-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-0-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-0-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-0-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-0-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-0-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-0-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-0-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-0-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-0-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-0-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-0-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-0-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-0-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-0-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-0-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-0-membership-heatmap'>
<ul>
<li><a href='#tab-node-0-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-0-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-0-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-0-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-0-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-0-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-0-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-0-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-1-1.png" alt="plot of chunk tab-node-0-membership-heatmap-1"/></p>

</div>
<div id='tab-node-0-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-2-1.png" alt="plot of chunk tab-node-0-membership-heatmap-2"/></p>

</div>
<div id='tab-node-0-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-3-1.png" alt="plot of chunk tab-node-0-membership-heatmap-3"/></p>

</div>
<div id='tab-node-0-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-4-1.png" alt="plot of chunk tab-node-0-membership-heatmap-4"/></p>

</div>
<div id='tab-node-0-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-5-1.png" alt="plot of chunk tab-node-0-membership-heatmap-5"/></p>

</div>
<div id='tab-node-0-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-6-1.png" alt="plot of chunk tab-node-0-membership-heatmap-6"/></p>

</div>
<div id='tab-node-0-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-0-membership-heatmap-7-1.png" alt="plot of chunk tab-node-0-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-0-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-0-get-signatures'>
<ul>
<li><a href='#tab-node-0-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-0-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-0-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-0-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-0-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-0-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-0-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-0-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-1-1.png" alt="plot of chunk tab-node-0-get-signatures-1"/></p>

</div>
<div id='tab-node-0-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-2-1.png" alt="plot of chunk tab-node-0-get-signatures-2"/></p>

</div>
<div id='tab-node-0-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-3-1.png" alt="plot of chunk tab-node-0-get-signatures-3"/></p>

</div>
<div id='tab-node-0-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-4-1.png" alt="plot of chunk tab-node-0-get-signatures-4"/></p>

</div>
<div id='tab-node-0-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-5-1.png" alt="plot of chunk tab-node-0-get-signatures-5"/></p>

</div>
<div id='tab-node-0-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-6-1.png" alt="plot of chunk tab-node-0-get-signatures-6"/></p>

</div>
<div id='tab-node-0-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-0-get-signatures-7-1.png" alt="plot of chunk tab-node-0-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-0-signature_compare](figure_cola/node-0-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-0-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-0-dimension-reduction'>
<ul>
<li><a href='#tab-node-0-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-0-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-0-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-0-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-0-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-0-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-0-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-0-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-1-1.png" alt="plot of chunk tab-node-0-dimension-reduction-1"/></p>

</div>
<div id='tab-node-0-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-2-1.png" alt="plot of chunk tab-node-0-dimension-reduction-2"/></p>

</div>
<div id='tab-node-0-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-3-1.png" alt="plot of chunk tab-node-0-dimension-reduction-3"/></p>

</div>
<div id='tab-node-0-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-4-1.png" alt="plot of chunk tab-node-0-dimension-reduction-4"/></p>

</div>
<div id='tab-node-0-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-5-1.png" alt="plot of chunk tab-node-0-dimension-reduction-5"/></p>

</div>
<div id='tab-node-0-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-6-1.png" alt="plot of chunk tab-node-0-dimension-reduction-6"/></p>

</div>
<div id='tab-node-0-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0-dimension-reduction-7-1.png" alt="plot of chunk tab-node-0-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-0-collect-classes](figure_cola/node-0-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node01


Parent node: [Node0](#Node0).
Child nodes: 
                [Node011](#Node011)
        ,
                [Node012](#Node012)
        ,
                [Node013](#Node013)
        ,
                [Node021](#Node021)
        ,
                [Node022](#Node022)
        ,
                [Node023](#Node023)
        ,
                Node031-leaf
        ,
                Node032-leaf
        ,
                Node033-leaf
        ,
                Node034-leaf
        ,
                Node035-leaf
        ,
                Node041-leaf
        ,
                Node042-leaf
        ,
                Node043-leaf
        ,
                Node051-leaf
        ,
                Node052-leaf
        ,
                Node053-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["01"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 71 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-01-collect-plots](figure_cola/node-01-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-01-select-partition-number](figure_cola/node-01-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           1.000       1.000         0.4231 0.577   0.577
#> 3 3 1.000           0.960       0.981         0.5791 0.731   0.543
#> 4 4 0.727           0.724       0.830         0.1015 0.930   0.796
#> 5 5 0.738           0.835       0.860         0.0647 0.864   0.565
#> 6 6 0.778           0.790       0.854         0.0426 0.953   0.773
#> 7 7 0.870           0.820       0.879         0.0307 0.992   0.953
#> 8 8 0.836           0.735       0.852         0.0198 0.981   0.887
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-01-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-01-get-classes'>
<ul>
<li><a href='#tab-node-01-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-01-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-01-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-01-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-01-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-01-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-01-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-01-get-classes-1'>
<p><a id='tab-node-01-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2
#&gt; TCGA.LN.A4A4.01     2       0          1  0  1
#&gt; TCGA.Q9.A6FU.01     1       0          1  1  0
#&gt; TCGA.S8.A6BW.01     1       0          1  1  0
#&gt; TCGA.V5.A7RC.01     1       0          1  1  0
#&gt; TCGA.LN.A4A3.01     2       0          1  0  1
#&gt; TCGA.LN.A49X.01     1       0          1  1  0
#&gt; TCGA.LN.A7HV.01     2       0          1  0  1
#&gt; TCGA.IG.A3YC.01     1       0          1  1  0
#&gt; TCGA.KH.A6WC.01     1       0          1  1  0
#&gt; TCGA.L7.A56G.01     1       0          1  1  0
#&gt; TCGA.VR.A8EP.01     2       0          1  0  1
#&gt; TCGA.JY.A6FE.01     2       0          1  0  1
#&gt; TCGA.LN.A49N.01     1       0          1  1  0
#&gt; TCGA.VR.AA7B.01     1       0          1  1  0
#&gt; TCGA.IG.A3Y9.01     1       0          1  1  0
#&gt; TCGA.L5.A4OM.01     2       0          1  0  1
#&gt; TCGA.LN.A4A6.01     2       0          1  0  1
#&gt; TCGA.LN.A49R.01     2       0          1  0  1
#&gt; TCGA.LN.A49K.01     1       0          1  1  0
#&gt; TCGA.LN.A49U.01     2       0          1  0  1
#&gt; TCGA.LN.A7HX.01     2       0          1  0  1
#&gt; TCGA.LN.A4A8.01     2       0          1  0  1
#&gt; TCGA.LN.A5U7.01     1       0          1  1  0
#&gt; TCGA.V5.A7RC.06     1       0          1  1  0
#&gt; TCGA.IG.A625.01     1       0          1  1  0
#&gt; TCGA.IG.A4P3.01     1       0          1  1  0
#&gt; TCGA.LN.A49Y.01     2       0          1  0  1
#&gt; TCGA.L5.A43H.01     1       0          1  1  0
#&gt; TCGA.IG.A50L.01     1       0          1  1  0
#&gt; TCGA.LN.A7HY.01     1       0          1  1  0
#&gt; TCGA.LN.A49P.01     1       0          1  1  0
#&gt; TCGA.LN.A4A1.01     2       0          1  0  1
#&gt; TCGA.LN.A49O.01     1       0          1  1  0
#&gt; TCGA.LN.A49W.01     1       0          1  1  0
#&gt; TCGA.IG.A3YA.01     1       0          1  1  0
#&gt; TCGA.LN.A7HZ.01     1       0          1  1  0
#&gt; TCGA.IG.A3QL.01     1       0          1  1  0
#&gt; TCGA.LN.A4A2.01     1       0          1  1  0
#&gt; TCGA.LN.A49S.01     2       0          1  0  1
#&gt; TCGA.LN.A7HW.01     1       0          1  1  0
#&gt; TCGA.IG.A8O2.01     2       0          1  0  1
#&gt; TCGA.L5.A8NQ.01     1       0          1  1  0
#&gt; TCGA.LN.A8I0.01     1       0          1  1  0
#&gt; TCGA.XP.A8T8.01     1       0          1  1  0
#&gt; TCGA.IG.A5B8.01     2       0          1  0  1
#&gt; TCGA.LN.A4MR.01     2       0          1  0  1
#&gt; TCGA.LN.A4MQ.01     1       0          1  1  0
#&gt; TCGA.LN.A4A9.01     2       0          1  0  1
#&gt; TCGA.VR.A8EX.01     1       0          1  1  0
#&gt; TCGA.JY.A6FA.01     2       0          1  0  1
#&gt; TCGA.VR.A8EO.01     2       0          1  0  1
#&gt; TCGA.VR.A8EU.01     1       0          1  1  0
#&gt; TCGA.LN.A8I1.01     1       0          1  1  0
#&gt; TCGA.LN.A5U5.01     1       0          1  1  0
#&gt; TCGA.Z6.A8JD.01     1       0          1  1  0
#&gt; TCGA.XP.A8T6.01     2       0          1  0  1
#&gt; TCGA.VR.A8EZ.01     1       0          1  1  0
#&gt; TCGA.LN.A8HZ.01     1       0          1  1  0
#&gt; TCGA.L5.A88S.01     1       0          1  1  0
#&gt; TCGA.VR.A8EW.01     1       0          1  1  0
#&gt; TCGA.VR.A8ER.01     1       0          1  1  0
#&gt; TCGA.IG.A97H.01     1       0          1  1  0
#&gt; TCGA.VR.AA4G.01     1       0          1  1  0
#&gt; TCGA.JY.A6FD.01     1       0          1  1  0
#&gt; TCGA.IG.A97I.01     1       0          1  1  0
#&gt; TCGA.IG.A5S3.01     1       0          1  1  0
#&gt; TCGA.LN.A5U6.01     1       0          1  1  0
#&gt; TCGA.LN.A9FQ.01     1       0          1  1  0
#&gt; TCGA.L5.A8NK.01     1       0          1  1  0
#&gt; TCGA.LN.A9FO.01     1       0          1  1  0
#&gt; TCGA.LN.A9FR.01     1       0          1  1  0
</code></pre>

<script>
$('#tab-node-01-get-classes-1-a').parent().next().next().hide();
$('#tab-node-01-get-classes-1-a').click(function(){
  $('#tab-node-01-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-01-get-classes-2'>
<p><a id='tab-node-01-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.LN.A4A4.01     2  0.2537      0.939 0.08 0.92 0.00
#&gt; TCGA.Q9.A6FU.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.S8.A6BW.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.V5.A7RC.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A4A3.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.IG.A3YC.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.L7.A56G.01     3  0.2066      0.935 0.06 0.00 0.94
#&gt; TCGA.VR.A8EP.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.JY.A6FE.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A49N.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.VR.AA7B.01     1  0.6244      0.225 0.56 0.00 0.44
#&gt; TCGA.IG.A3Y9.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.L5.A4OM.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A4A6.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A49R.01     2  0.2537      0.939 0.08 0.92 0.00
#&gt; TCGA.LN.A49K.01     3  0.2959      0.889 0.10 0.00 0.90
#&gt; TCGA.LN.A49U.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A7HX.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A4A8.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.V5.A7RC.06     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.IG.A625.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A49Y.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.L5.A43H.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.IG.A50L.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A7HY.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A49P.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A4A1.01     2  0.2537      0.939 0.08 0.92 0.00
#&gt; TCGA.LN.A49O.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A49W.01     3  0.0892      0.974 0.02 0.00 0.98
#&gt; TCGA.IG.A3YA.01     1  0.1529      0.944 0.96 0.00 0.04
#&gt; TCGA.LN.A7HZ.01     1  0.2959      0.882 0.90 0.00 0.10
#&gt; TCGA.IG.A3QL.01     1  0.1529      0.944 0.96 0.00 0.04
#&gt; TCGA.LN.A4A2.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A49S.01     2  0.2537      0.939 0.08 0.92 0.00
#&gt; TCGA.LN.A7HW.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.IG.A8O2.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.L5.A8NQ.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.IG.A5B8.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A4MR.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.LN.A4MQ.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A4A9.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     2  0.0000      0.974 0.00 1.00 0.00
#&gt; TCGA.VR.A8EO.01     2  0.2537      0.939 0.08 0.92 0.00
#&gt; TCGA.VR.A8EU.01     1  0.1529      0.944 0.96 0.00 0.04
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A5U5.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.Z6.A8JD.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     2  0.2537      0.939 0.08 0.92 0.00
#&gt; TCGA.VR.A8EZ.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.VR.A8EW.01     1  0.1529      0.944 0.96 0.00 0.04
#&gt; TCGA.VR.A8ER.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.IG.A97H.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.VR.AA4G.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.IG.A5S3.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A5U6.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.LN.A9FQ.01     3  0.0000      0.991 0.00 0.00 1.00
#&gt; TCGA.L5.A8NK.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.0000      0.972 1.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     3  0.0000      0.991 0.00 0.00 1.00
</code></pre>

<script>
$('#tab-node-01-get-classes-2-a').parent().next().next().hide();
$('#tab-node-01-get-classes-2-a').click(function(){
  $('#tab-node-01-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-01-get-classes-3'>
<p><a id='tab-node-01-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.LN.A4A4.01     4  0.4855      0.845 0.00 0.40 0.00 0.60
#&gt; TCGA.Q9.A6FU.01     1  0.0707      0.801 0.98 0.00 0.00 0.02
#&gt; TCGA.S8.A6BW.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.V5.A7RC.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A3.01     4  0.4855      0.187 0.40 0.00 0.00 0.60
#&gt; TCGA.LN.A49X.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3YC.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     3  0.2921      0.783 0.00 0.00 0.86 0.14
#&gt; TCGA.L7.A56G.01     3  0.7768      0.360 0.24 0.00 0.40 0.36
#&gt; TCGA.VR.A8EP.01     2  0.4790     -0.117 0.00 0.62 0.00 0.38
#&gt; TCGA.JY.A6FE.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7B.01     1  0.6714      0.440 0.54 0.00 0.10 0.36
#&gt; TCGA.IG.A3Y9.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     4  0.4790      0.822 0.00 0.38 0.00 0.62
#&gt; TCGA.LN.A49K.01     1  0.7699      0.122 0.40 0.00 0.22 0.38
#&gt; TCGA.LN.A49U.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A8.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.1211      0.798 0.96 0.00 0.00 0.04
#&gt; TCGA.V5.A7RC.06     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A625.01     1  0.3975      0.667 0.76 0.00 0.00 0.24
#&gt; TCGA.IG.A4P3.01     3  0.7310      0.510 0.16 0.00 0.48 0.36
#&gt; TCGA.LN.A49Y.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A43H.01     3  0.4713      0.677 0.00 0.00 0.64 0.36
#&gt; TCGA.IG.A50L.01     1  0.1211      0.798 0.96 0.00 0.00 0.04
#&gt; TCGA.LN.A7HY.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A49P.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A1.01     4  0.4855      0.845 0.00 0.40 0.00 0.60
#&gt; TCGA.LN.A49O.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49W.01     3  0.7581      0.446 0.20 0.00 0.44 0.36
#&gt; TCGA.IG.A3YA.01     1  0.4713      0.591 0.64 0.00 0.00 0.36
#&gt; TCGA.LN.A7HZ.01     1  0.5428      0.566 0.60 0.00 0.02 0.38
#&gt; TCGA.IG.A3QL.01     1  0.4790      0.588 0.62 0.00 0.00 0.38
#&gt; TCGA.LN.A4A2.01     1  0.1211      0.798 0.96 0.00 0.00 0.04
#&gt; TCGA.LN.A49S.01     4  0.4855      0.845 0.00 0.40 0.00 0.60
#&gt; TCGA.LN.A7HW.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A8O2.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0707      0.801 0.98 0.00 0.00 0.02
#&gt; TCGA.XP.A8T8.01     1  0.1211      0.798 0.96 0.00 0.00 0.04
#&gt; TCGA.IG.A5B8.01     4  0.4855      0.845 0.00 0.40 0.00 0.60
#&gt; TCGA.LN.A4MR.01     2  0.4790     -0.117 0.00 0.62 0.00 0.38
#&gt; TCGA.LN.A4MQ.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A9.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.3610      0.673 0.80 0.00 0.00 0.20
#&gt; TCGA.JY.A6FA.01     2  0.0000      0.899 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     4  0.4855      0.845 0.00 0.40 0.00 0.60
#&gt; TCGA.VR.A8EU.01     1  0.4790      0.588 0.62 0.00 0.00 0.38
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A5U5.01     3  0.4713      0.677 0.00 0.00 0.64 0.36
#&gt; TCGA.Z6.A8JD.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     4  0.4855      0.845 0.00 0.40 0.00 0.60
#&gt; TCGA.VR.A8EZ.01     3  0.4713      0.677 0.00 0.00 0.64 0.36
#&gt; TCGA.LN.A8HZ.01     1  0.3975      0.667 0.76 0.00 0.00 0.24
#&gt; TCGA.L5.A88S.01     1  0.3801      0.654 0.78 0.00 0.00 0.22
#&gt; TCGA.VR.A8EW.01     1  0.4790      0.588 0.62 0.00 0.00 0.38
#&gt; TCGA.VR.A8ER.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A97H.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.3801      0.654 0.78 0.00 0.00 0.22
#&gt; TCGA.JY.A6FD.01     1  0.3801      0.654 0.78 0.00 0.00 0.22
#&gt; TCGA.IG.A97I.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A5S3.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A5U6.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A9FQ.01     3  0.0000      0.837 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.3610      0.673 0.80 0.00 0.00 0.20
#&gt; TCGA.LN.A9FO.01     1  0.0000      0.802 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     3  0.7310      0.510 0.16 0.00 0.48 0.36
</code></pre>

<script>
$('#tab-node-01-get-classes-3-a').parent().next().next().hide();
$('#tab-node-01-get-classes-3-a').click(function(){
  $('#tab-node-01-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-01-get-classes-4'>
<p><a id='tab-node-01-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.LN.A4A4.01     4  0.4373      0.897 0.00 0.16 0.00 0.76 0.08
#&gt; TCGA.Q9.A6FU.01     1  0.4373      0.787 0.76 0.00 0.00 0.08 0.16
#&gt; TCGA.S8.A6BW.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.A7RC.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A3.01     4  0.2929      0.737 0.18 0.00 0.00 0.82 0.00
#&gt; TCGA.LN.A49X.01     1  0.2020      0.792 0.90 0.00 0.00 0.00 0.10
#&gt; TCGA.LN.A7HV.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YC.01     1  0.2020      0.792 0.90 0.00 0.00 0.00 0.10
#&gt; TCGA.KH.A6WC.01     3  0.3895      0.317 0.00 0.00 0.68 0.00 0.32
#&gt; TCGA.L7.A56G.01     5  0.5355      0.735 0.12 0.00 0.22 0.00 0.66
#&gt; TCGA.VR.A8EP.01     4  0.3424      0.865 0.00 0.24 0.00 0.76 0.00
#&gt; TCGA.JY.A6FE.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     1  0.0609      0.834 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.VR.AA7B.01     5  0.6543      0.677 0.24 0.00 0.08 0.08 0.60
#&gt; TCGA.IG.A3Y9.01     1  0.0609      0.834 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A4OM.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     4  0.4872      0.884 0.00 0.16 0.00 0.72 0.12
#&gt; TCGA.LN.A49K.01     5  0.3946      0.732 0.12 0.00 0.08 0.00 0.80
#&gt; TCGA.LN.A49U.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A8.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.4637      0.779 0.74 0.00 0.00 0.10 0.16
#&gt; TCGA.V5.A7RC.06     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A625.01     1  0.5263      0.739 0.66 0.00 0.00 0.10 0.24
#&gt; TCGA.IG.A4P3.01     5  0.5136      0.707 0.08 0.00 0.26 0.00 0.66
#&gt; TCGA.LN.A49Y.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43H.01     5  0.4798      0.431 0.00 0.00 0.44 0.02 0.54
#&gt; TCGA.IG.A50L.01     1  0.4637      0.779 0.74 0.00 0.00 0.10 0.16
#&gt; TCGA.LN.A7HY.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49P.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     4  0.2732      0.909 0.00 0.16 0.00 0.84 0.00
#&gt; TCGA.LN.A49O.01     1  0.3037      0.808 0.86 0.00 0.00 0.10 0.04
#&gt; TCGA.LN.A49W.01     5  0.5355      0.735 0.12 0.00 0.22 0.00 0.66
#&gt; TCGA.IG.A3YA.01     5  0.3983      0.607 0.34 0.00 0.00 0.00 0.66
#&gt; TCGA.LN.A7HZ.01     5  0.3109      0.674 0.20 0.00 0.00 0.00 0.80
#&gt; TCGA.IG.A3QL.01     5  0.3109      0.674 0.20 0.00 0.00 0.00 0.80
#&gt; TCGA.LN.A4A2.01     1  0.4373      0.787 0.76 0.00 0.00 0.08 0.16
#&gt; TCGA.LN.A49S.01     4  0.3291      0.884 0.04 0.12 0.00 0.84 0.00
#&gt; TCGA.LN.A7HW.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A8O2.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     1  0.0000      0.836 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.4373      0.787 0.76 0.00 0.00 0.08 0.16
#&gt; TCGA.XP.A8T8.01     1  0.4637      0.779 0.74 0.00 0.00 0.10 0.16
#&gt; TCGA.IG.A5B8.01     4  0.2732      0.909 0.00 0.16 0.00 0.84 0.00
#&gt; TCGA.LN.A4MR.01     4  0.3424      0.865 0.00 0.24 0.00 0.76 0.00
#&gt; TCGA.LN.A4MQ.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A9.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.1732      0.822 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.JY.A6FA.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     4  0.5083      0.878 0.00 0.16 0.00 0.70 0.14
#&gt; TCGA.VR.A8EU.01     5  0.3274      0.672 0.22 0.00 0.00 0.00 0.78
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     5  0.4798      0.431 0.00 0.00 0.44 0.02 0.54
#&gt; TCGA.Z6.A8JD.01     1  0.2020      0.792 0.90 0.00 0.00 0.00 0.10
#&gt; TCGA.XP.A8T6.01     4  0.2732      0.909 0.00 0.16 0.00 0.84 0.00
#&gt; TCGA.VR.A8EZ.01     5  0.4798      0.431 0.00 0.00 0.44 0.02 0.54
#&gt; TCGA.LN.A8HZ.01     1  0.5263      0.739 0.66 0.00 0.00 0.10 0.24
#&gt; TCGA.L5.A88S.01     1  0.1732      0.822 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.VR.A8EW.01     5  0.3109      0.674 0.20 0.00 0.00 0.00 0.80
#&gt; TCGA.VR.A8ER.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.1732      0.822 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.JY.A6FD.01     1  0.1732      0.822 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.IG.A97I.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A5U6.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.1732      0.822 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.LN.A9FO.01     1  0.1043      0.833 0.96 0.00 0.00 0.04 0.00
#&gt; TCGA.LN.A9FR.01     5  0.4967      0.686 0.06 0.00 0.28 0.00 0.66
</code></pre>

<script>
$('#tab-node-01-get-classes-4-a').parent().next().next().hide();
$('#tab-node-01-get-classes-4-a').click(function(){
  $('#tab-node-01-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-01-get-classes-5'>
<p><a id='tab-node-01-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.LN.A4A4.01     4  0.4155      0.857 0.02 0.10 0.00 0.80 0.04 0.04
#&gt; TCGA.Q9.A6FU.01     1  0.4348      0.206 0.64 0.00 0.00 0.00 0.04 0.32
#&gt; TCGA.S8.A6BW.01     3  0.1092      0.962 0.00 0.00 0.96 0.00 0.02 0.02
#&gt; TCGA.V5.A7RC.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A3.01     4  0.3756      0.519 0.40 0.00 0.00 0.60 0.00 0.00
#&gt; TCGA.LN.A49X.01     1  0.3073      0.726 0.84 0.00 0.00 0.00 0.08 0.08
#&gt; TCGA.LN.A7HV.01     2  0.1092      0.957 0.00 0.96 0.00 0.02 0.00 0.02
#&gt; TCGA.IG.A3YC.01     1  0.3073      0.726 0.84 0.00 0.00 0.00 0.08 0.08
#&gt; TCGA.KH.A6WC.01     5  0.3869      0.159 0.00 0.00 0.50 0.00 0.50 0.00
#&gt; TCGA.L7.A56G.01     5  0.2629      0.831 0.02 0.00 0.08 0.02 0.88 0.00
#&gt; TCGA.VR.A8EP.01     4  0.2048      0.867 0.00 0.12 0.00 0.88 0.00 0.00
#&gt; TCGA.JY.A6FE.01     2  0.2725      0.934 0.00 0.88 0.00 0.02 0.04 0.06
#&gt; TCGA.LN.A49N.01     1  0.3073      0.726 0.84 0.00 0.00 0.00 0.08 0.08
#&gt; TCGA.VR.AA7B.01     5  0.4530      0.782 0.08 0.00 0.02 0.06 0.78 0.06
#&gt; TCGA.IG.A3Y9.01     1  0.3073      0.726 0.84 0.00 0.00 0.00 0.08 0.08
#&gt; TCGA.L5.A4OM.01     2  0.1480      0.949 0.00 0.94 0.00 0.00 0.02 0.04
#&gt; TCGA.LN.A4A6.01     2  0.1092      0.957 0.00 0.96 0.00 0.02 0.00 0.02
#&gt; TCGA.LN.A49R.01     4  0.5197      0.731 0.02 0.04 0.00 0.68 0.04 0.22
#&gt; TCGA.LN.A49K.01     5  0.2725      0.820 0.02 0.00 0.04 0.00 0.88 0.06
#&gt; TCGA.LN.A49U.01     2  0.0000      0.961 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HX.01     2  0.0000      0.961 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A8.01     2  0.0000      0.961 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U7.01     6  0.3916      0.740 0.30 0.00 0.00 0.00 0.02 0.68
#&gt; TCGA.V5.A7RC.06     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A625.01     6  0.4144      0.638 0.36 0.00 0.00 0.02 0.00 0.62
#&gt; TCGA.IG.A4P3.01     5  0.1814      0.828 0.00 0.00 0.10 0.00 0.90 0.00
#&gt; TCGA.LN.A49Y.01     2  0.0000      0.961 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43H.01     5  0.4042      0.765 0.00 0.00 0.18 0.04 0.76 0.02
#&gt; TCGA.IG.A50L.01     6  0.4534      0.746 0.38 0.00 0.00 0.00 0.04 0.58
#&gt; TCGA.LN.A7HY.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49P.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     4  0.3321      0.882 0.08 0.10 0.00 0.82 0.00 0.00
#&gt; TCGA.LN.A49O.01     1  0.4282     -0.214 0.56 0.00 0.00 0.02 0.00 0.42
#&gt; TCGA.LN.A49W.01     5  0.2629      0.831 0.02 0.00 0.08 0.02 0.88 0.00
#&gt; TCGA.IG.A3YA.01     5  0.3572      0.761 0.10 0.00 0.00 0.02 0.82 0.06
#&gt; TCGA.LN.A7HZ.01     5  0.2512      0.797 0.06 0.00 0.00 0.00 0.88 0.06
#&gt; TCGA.IG.A3QL.01     5  0.4851      0.695 0.06 0.00 0.00 0.04 0.70 0.20
#&gt; TCGA.LN.A4A2.01     6  0.4246      0.734 0.40 0.00 0.00 0.00 0.02 0.58
#&gt; TCGA.LN.A49S.01     4  0.3321      0.874 0.10 0.08 0.00 0.82 0.00 0.00
#&gt; TCGA.LN.A7HW.01     3  0.1480      0.948 0.00 0.00 0.94 0.04 0.00 0.02
#&gt; TCGA.IG.A8O2.01     2  0.2345      0.942 0.00 0.90 0.00 0.02 0.02 0.06
#&gt; TCGA.L5.A8NQ.01     1  0.1556      0.730 0.92 0.00 0.00 0.00 0.08 0.00
#&gt; TCGA.LN.A8I0.01     1  0.4609     -0.344 0.54 0.00 0.00 0.00 0.04 0.42
#&gt; TCGA.XP.A8T8.01     6  0.4482      0.754 0.36 0.00 0.00 0.00 0.04 0.60
#&gt; TCGA.IG.A5B8.01     4  0.3045      0.879 0.06 0.10 0.00 0.84 0.00 0.00
#&gt; TCGA.LN.A4MR.01     4  0.2981      0.834 0.00 0.16 0.00 0.82 0.00 0.02
#&gt; TCGA.LN.A4MQ.01     3  0.1480      0.948 0.00 0.00 0.94 0.04 0.00 0.02
#&gt; TCGA.LN.A4A9.01     2  0.0000      0.961 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0000      0.728 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     2  0.2725      0.934 0.00 0.88 0.00 0.02 0.04 0.06
#&gt; TCGA.VR.A8EO.01     4  0.3785      0.867 0.02 0.10 0.00 0.82 0.02 0.04
#&gt; TCGA.VR.A8EU.01     5  0.3795      0.759 0.06 0.00 0.00 0.02 0.80 0.12
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     5  0.4195      0.747 0.00 0.00 0.20 0.04 0.74 0.02
#&gt; TCGA.Z6.A8JD.01     1  0.3073      0.726 0.84 0.00 0.00 0.00 0.08 0.08
#&gt; TCGA.XP.A8T6.01     4  0.3321      0.882 0.08 0.10 0.00 0.82 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     5  0.4195      0.747 0.00 0.00 0.20 0.04 0.74 0.02
#&gt; TCGA.LN.A8HZ.01     6  0.4282      0.668 0.42 0.00 0.00 0.02 0.00 0.56
#&gt; TCGA.L5.A88S.01     1  0.0000      0.728 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EW.01     5  0.3997      0.748 0.06 0.00 0.00 0.02 0.78 0.14
#&gt; TCGA.VR.A8ER.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.0000      0.728 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     1  0.0000      0.728 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97I.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     3  0.0547      0.972 0.00 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A5U6.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     3  0.0000      0.986 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.0000      0.728 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.1267      0.723 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A9FR.01     5  0.1814      0.828 0.00 0.00 0.10 0.00 0.90 0.00
</code></pre>

<script>
$('#tab-node-01-get-classes-5-a').parent().next().next().hide();
$('#tab-node-01-get-classes-5-a').click(function(){
  $('#tab-node-01-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-01-get-classes-6'>
<p><a id='tab-node-01-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.LN.A4A4.01     4  0.3047      0.766 0.00 0.00 0.00 0.72 0.00 0.28 0.00
#&gt; TCGA.Q9.A6FU.01     1  0.4283     -0.493 0.48 0.00 0.00 0.00 0.00 0.04 0.48
#&gt; TCGA.S8.A6BW.01     3  0.1928      0.915 0.00 0.00 0.90 0.00 0.02 0.08 0.00
#&gt; TCGA.V5.A7RC.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A3.01     4  0.3606      0.574 0.30 0.00 0.00 0.68 0.00 0.02 0.00
#&gt; TCGA.LN.A49X.01     1  0.3061      0.766 0.84 0.00 0.00 0.00 0.08 0.02 0.06
#&gt; TCGA.LN.A7HV.01     2  0.0504      0.978 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.IG.A3YC.01     1  0.3061      0.766 0.84 0.00 0.00 0.00 0.08 0.02 0.06
#&gt; TCGA.KH.A6WC.01     5  0.4426      0.341 0.00 0.00 0.38 0.00 0.56 0.06 0.00
#&gt; TCGA.L7.A56G.01     5  0.0000      0.854 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EP.01     4  0.1886      0.825 0.00 0.00 0.00 0.88 0.00 0.12 0.00
#&gt; TCGA.JY.A6FE.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A49N.01     1  0.2509      0.780 0.88 0.00 0.00 0.00 0.04 0.02 0.06
#&gt; TCGA.VR.AA7B.01     5  0.3815      0.682 0.00 0.00 0.00 0.00 0.62 0.36 0.02
#&gt; TCGA.IG.A3Y9.01     1  0.2509      0.780 0.88 0.00 0.00 0.00 0.04 0.02 0.06
#&gt; TCGA.L5.A4OM.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A4A6.01     2  0.0504      0.978 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A49R.01     4  0.4418      0.704 0.00 0.00 0.00 0.62 0.00 0.30 0.08
#&gt; TCGA.LN.A49K.01     5  0.2572      0.842 0.00 0.00 0.00 0.00 0.86 0.08 0.06
#&gt; TCGA.LN.A49U.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A7HX.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A4A8.01     2  0.0504      0.978 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A5U7.01     7  0.2259      0.769 0.16 0.00 0.00 0.00 0.00 0.00 0.84
#&gt; TCGA.V5.A7RC.06     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A625.01     7  0.3517      0.787 0.28 0.00 0.00 0.00 0.00 0.02 0.70
#&gt; TCGA.IG.A4P3.01     5  0.0000      0.854 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A43H.01     5  0.3863      0.778 0.00 0.00 0.04 0.00 0.74 0.20 0.02
#&gt; TCGA.IG.A50L.01     7  0.3047      0.821 0.28 0.00 0.00 0.00 0.00 0.00 0.72
#&gt; TCGA.LN.A7HY.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49P.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     4  0.0863      0.847 0.04 0.00 0.00 0.96 0.00 0.00 0.00
#&gt; TCGA.LN.A49O.01     1  0.5083      0.270 0.56 0.00 0.00 0.00 0.00 0.24 0.20
#&gt; TCGA.LN.A49W.01     5  0.0000      0.854 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3YA.01     5  0.1006      0.849 0.00 0.00 0.00 0.00 0.96 0.02 0.02
#&gt; TCGA.LN.A7HZ.01     5  0.1166      0.847 0.00 0.00 0.00 0.00 0.94 0.00 0.06
#&gt; TCGA.IG.A3QL.01     5  0.3370      0.783 0.00 0.00 0.00 0.00 0.78 0.06 0.16
#&gt; TCGA.LN.A4A2.01     7  0.3221      0.796 0.32 0.00 0.00 0.00 0.00 0.00 0.68
#&gt; TCGA.LN.A49S.01     4  0.0863      0.847 0.04 0.00 0.00 0.96 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     3  0.2081      0.886 0.00 0.00 0.86 0.00 0.00 0.14 0.00
#&gt; TCGA.IG.A8O2.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A8NQ.01     1  0.1363      0.800 0.94 0.00 0.00 0.00 0.04 0.02 0.00
#&gt; TCGA.LN.A8I0.01     7  0.3525      0.599 0.44 0.00 0.00 0.00 0.00 0.00 0.56
#&gt; TCGA.XP.A8T8.01     7  0.2708      0.812 0.22 0.00 0.00 0.00 0.00 0.00 0.78
#&gt; TCGA.IG.A5B8.01     4  0.0863      0.847 0.04 0.00 0.00 0.96 0.00 0.00 0.00
#&gt; TCGA.LN.A4MR.01     4  0.1664      0.822 0.00 0.06 0.00 0.92 0.00 0.02 0.00
#&gt; TCGA.LN.A4MQ.01     3  0.2081      0.886 0.00 0.00 0.86 0.00 0.00 0.14 0.00
#&gt; TCGA.LN.A4A9.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0504      0.801 0.98 0.00 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.JY.A6FA.01     2  0.0504      0.981 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.VR.A8EO.01     4  0.4264      0.702 0.00 0.00 0.00 0.62 0.00 0.32 0.06
#&gt; TCGA.VR.A8EU.01     5  0.2769      0.810 0.02 0.00 0.00 0.00 0.86 0.04 0.08
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     5  0.3863      0.778 0.00 0.00 0.04 0.00 0.74 0.20 0.02
#&gt; TCGA.Z6.A8JD.01     1  0.3061      0.766 0.84 0.00 0.00 0.00 0.08 0.02 0.06
#&gt; TCGA.XP.A8T6.01     4  0.0863      0.847 0.04 0.00 0.00 0.96 0.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     5  0.3863      0.778 0.00 0.00 0.04 0.00 0.74 0.20 0.02
#&gt; TCGA.LN.A8HZ.01     7  0.3517      0.787 0.28 0.00 0.00 0.00 0.00 0.02 0.70
#&gt; TCGA.L5.A88S.01     1  0.1006      0.794 0.96 0.00 0.00 0.02 0.00 0.02 0.00
#&gt; TCGA.VR.A8EW.01     5  0.2278      0.830 0.00 0.00 0.00 0.00 0.88 0.04 0.08
#&gt; TCGA.VR.A8ER.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.1006      0.794 0.96 0.00 0.00 0.02 0.00 0.02 0.00
#&gt; TCGA.JY.A6FD.01     1  0.1006      0.794 0.96 0.00 0.00 0.02 0.00 0.02 0.00
#&gt; TCGA.IG.A97I.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     3  0.1363      0.939 0.00 0.00 0.94 0.00 0.02 0.04 0.00
#&gt; TCGA.LN.A5U6.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     3  0.0000      0.969 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.0504      0.801 0.98 0.00 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A9FO.01     1  0.0000      0.803 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     5  0.0000      0.854 0.00 0.00 0.00 0.00 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-01-get-classes-6-a').parent().next().next().hide();
$('#tab-node-01-get-classes-6-a').click(function(){
  $('#tab-node-01-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-01-get-classes-7'>
<p><a id='tab-node-01-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.LN.A4A4.01     4  0.2534      0.773 0.00 0.00 0.00 0.78 0.00 0.00 0.22 0.00
#&gt; TCGA.Q9.A6FU.01     6  0.4174      0.362 0.40 0.00 0.00 0.00 0.00 0.54 0.06 0.00
#&gt; TCGA.S8.A6BW.01     3  0.3895      0.726 0.00 0.00 0.74 0.00 0.12 0.02 0.00 0.12
#&gt; TCGA.V5.A7RC.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A3.01     4  0.3272      0.298 0.42 0.00 0.00 0.58 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     1  0.3102      0.824 0.82 0.00 0.00 0.00 0.00 0.08 0.08 0.02
#&gt; TCGA.LN.A7HV.01     2  0.0941      0.934 0.00 0.96 0.00 0.00 0.00 0.00 0.02 0.02
#&gt; TCGA.IG.A3YC.01     1  0.3102      0.824 0.82 0.00 0.00 0.00 0.00 0.08 0.08 0.02
#&gt; TCGA.KH.A6WC.01     5  0.4503      0.424 0.00 0.00 0.18 0.00 0.66 0.02 0.00 0.14
#&gt; TCGA.L7.A56G.01     5  0.3528      0.547 0.00 0.00 0.00 0.00 0.74 0.00 0.08 0.18
#&gt; TCGA.VR.A8EP.01     4  0.2025      0.815 0.00 0.00 0.00 0.88 0.00 0.00 0.10 0.02
#&gt; TCGA.JY.A6FE.01     2  0.2132      0.906 0.00 0.88 0.00 0.00 0.00 0.00 0.08 0.04
#&gt; TCGA.LN.A49N.01     1  0.3102      0.824 0.82 0.00 0.00 0.00 0.00 0.08 0.08 0.02
#&gt; TCGA.VR.AA7B.01     8  0.3808     -0.353 0.00 0.00 0.00 0.00 0.34 0.00 0.04 0.62
#&gt; TCGA.IG.A3Y9.01     1  0.3102      0.824 0.82 0.00 0.00 0.00 0.00 0.08 0.08 0.02
#&gt; TCGA.L5.A4OM.01     2  0.1557      0.926 0.00 0.92 0.00 0.00 0.00 0.00 0.02 0.06
#&gt; TCGA.LN.A4A6.01     2  0.0941      0.934 0.00 0.96 0.00 0.00 0.00 0.00 0.02 0.02
#&gt; TCGA.LN.A49R.01     4  0.3845      0.693 0.00 0.00 0.00 0.66 0.00 0.06 0.28 0.00
#&gt; TCGA.LN.A49K.01     5  0.1557      0.634 0.00 0.00 0.00 0.00 0.92 0.02 0.00 0.06
#&gt; TCGA.LN.A49U.01     2  0.0808      0.945 0.00 0.96 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.LN.A7HX.01     2  0.0808      0.945 0.00 0.96 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.LN.A4A8.01     2  0.0471      0.945 0.00 0.98 0.00 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A5U7.01     6  0.1804      0.803 0.08 0.00 0.00 0.00 0.00 0.90 0.00 0.02
#&gt; TCGA.V5.A7RC.06     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A625.01     6  0.2818      0.711 0.12 0.00 0.00 0.00 0.00 0.82 0.06 0.00
#&gt; TCGA.IG.A4P3.01     5  0.1765      0.632 0.00 0.00 0.00 0.00 0.88 0.00 0.00 0.12
#&gt; TCGA.LN.A49Y.01     2  0.0808      0.945 0.00 0.96 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.L5.A43H.01     5  0.3992      0.349 0.00 0.00 0.04 0.00 0.52 0.00 0.00 0.44
#&gt; TCGA.IG.A50L.01     6  0.1765      0.811 0.12 0.00 0.00 0.00 0.00 0.88 0.00 0.00
#&gt; TCGA.LN.A7HY.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49P.01     3  0.0471      0.916 0.00 0.00 0.98 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.LN.A4A1.01     4  0.0000      0.833 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49O.01     8  0.5973     -0.129 0.28 0.00 0.00 0.00 0.00 0.26 0.06 0.40
#&gt; TCGA.LN.A49W.01     5  0.1563      0.631 0.00 0.00 0.00 0.00 0.90 0.00 0.00 0.10
#&gt; TCGA.IG.A3YA.01     5  0.3131      0.546 0.04 0.00 0.00 0.00 0.84 0.04 0.06 0.02
#&gt; TCGA.LN.A7HZ.01     5  0.1557      0.634 0.00 0.00 0.00 0.00 0.92 0.02 0.00 0.06
#&gt; TCGA.IG.A3QL.01     5  0.5862      0.287 0.04 0.00 0.00 0.00 0.56 0.10 0.22 0.08
#&gt; TCGA.LN.A4A2.01     6  0.2025      0.813 0.10 0.00 0.00 0.00 0.00 0.88 0.00 0.02
#&gt; TCGA.LN.A49S.01     4  0.0000      0.833 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     3  0.3021      0.804 0.00 0.00 0.80 0.00 0.02 0.02 0.00 0.16
#&gt; TCGA.IG.A8O2.01     2  0.1275      0.932 0.00 0.94 0.00 0.00 0.00 0.00 0.02 0.04
#&gt; TCGA.L5.A8NQ.01     1  0.0471      0.857 0.98 0.00 0.00 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A8I0.01     6  0.2756      0.694 0.26 0.00 0.00 0.00 0.00 0.74 0.00 0.00
#&gt; TCGA.XP.A8T8.01     6  0.1341      0.806 0.08 0.00 0.00 0.00 0.00 0.92 0.00 0.00
#&gt; TCGA.IG.A5B8.01     4  0.0000      0.833 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4MR.01     4  0.1741      0.811 0.00 0.04 0.00 0.92 0.00 0.00 0.02 0.02
#&gt; TCGA.LN.A4MQ.01     3  0.3021      0.804 0.00 0.00 0.80 0.00 0.02 0.02 0.00 0.16
#&gt; TCGA.LN.A4A9.01     2  0.0808      0.945 0.00 0.96 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.VR.A8EX.01     1  0.0471      0.854 0.98 0.00 0.00 0.02 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     2  0.2407      0.893 0.00 0.86 0.00 0.00 0.00 0.00 0.08 0.06
#&gt; TCGA.VR.A8EO.01     4  0.3862      0.624 0.00 0.00 0.00 0.60 0.00 0.00 0.36 0.04
#&gt; TCGA.VR.A8EU.01     5  0.4571      0.475 0.04 0.00 0.00 0.00 0.72 0.12 0.08 0.04
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     5  0.3992      0.349 0.00 0.00 0.04 0.00 0.52 0.00 0.00 0.44
#&gt; TCGA.Z6.A8JD.01     1  0.3102      0.824 0.82 0.00 0.00 0.00 0.00 0.08 0.08 0.02
#&gt; TCGA.XP.A8T6.01     4  0.0000      0.833 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     5  0.3992      0.349 0.00 0.00 0.04 0.00 0.52 0.00 0.00 0.44
#&gt; TCGA.LN.A8HZ.01     6  0.2569      0.773 0.16 0.00 0.00 0.00 0.00 0.82 0.02 0.00
#&gt; TCGA.L5.A88S.01     1  0.0808      0.847 0.96 0.00 0.00 0.04 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EW.01     5  0.4185      0.515 0.04 0.00 0.00 0.00 0.76 0.08 0.08 0.04
#&gt; TCGA.VR.A8ER.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4G.01     1  0.0808      0.847 0.96 0.00 0.00 0.04 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     1  0.1607      0.821 0.92 0.00 0.00 0.04 0.00 0.00 0.00 0.04
#&gt; TCGA.IG.A97I.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     3  0.4427      0.648 0.00 0.00 0.68 0.00 0.02 0.02 0.06 0.22
#&gt; TCGA.LN.A5U6.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FQ.01     3  0.0000      0.925 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     1  0.0808      0.847 0.96 0.00 0.00 0.04 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     1  0.1275      0.845 0.94 0.00 0.00 0.00 0.00 0.02 0.00 0.04
#&gt; TCGA.LN.A9FR.01     5  0.1765      0.632 0.00 0.00 0.00 0.00 0.88 0.00 0.00 0.12
</code></pre>

<script>
$('#tab-node-01-get-classes-7-a').parent().next().next().hide();
$('#tab-node-01-get-classes-7-a').click(function(){
  $('#tab-node-01-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-01-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-01-consensus-heatmap'>
<ul>
<li><a href='#tab-node-01-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-01-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-01-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-01-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-01-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-01-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-01-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-01-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-01-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-01-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-01-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-01-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-01-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-01-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-01-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-01-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-01-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-01-membership-heatmap'>
<ul>
<li><a href='#tab-node-01-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-01-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-01-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-01-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-01-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-01-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-01-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-01-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-1-1.png" alt="plot of chunk tab-node-01-membership-heatmap-1"/></p>

</div>
<div id='tab-node-01-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-2-1.png" alt="plot of chunk tab-node-01-membership-heatmap-2"/></p>

</div>
<div id='tab-node-01-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-3-1.png" alt="plot of chunk tab-node-01-membership-heatmap-3"/></p>

</div>
<div id='tab-node-01-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-4-1.png" alt="plot of chunk tab-node-01-membership-heatmap-4"/></p>

</div>
<div id='tab-node-01-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-5-1.png" alt="plot of chunk tab-node-01-membership-heatmap-5"/></p>

</div>
<div id='tab-node-01-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-6-1.png" alt="plot of chunk tab-node-01-membership-heatmap-6"/></p>

</div>
<div id='tab-node-01-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-01-membership-heatmap-7-1.png" alt="plot of chunk tab-node-01-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-01-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-01-get-signatures'>
<ul>
<li><a href='#tab-node-01-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-01-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-01-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-01-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-01-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-01-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-01-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-01-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-1-1.png" alt="plot of chunk tab-node-01-get-signatures-1"/></p>

</div>
<div id='tab-node-01-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-2-1.png" alt="plot of chunk tab-node-01-get-signatures-2"/></p>

</div>
<div id='tab-node-01-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-3-1.png" alt="plot of chunk tab-node-01-get-signatures-3"/></p>

</div>
<div id='tab-node-01-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-4-1.png" alt="plot of chunk tab-node-01-get-signatures-4"/></p>

</div>
<div id='tab-node-01-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-5-1.png" alt="plot of chunk tab-node-01-get-signatures-5"/></p>

</div>
<div id='tab-node-01-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-6-1.png" alt="plot of chunk tab-node-01-get-signatures-6"/></p>

</div>
<div id='tab-node-01-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-01-get-signatures-7-1.png" alt="plot of chunk tab-node-01-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-01-signature_compare](figure_cola/node-01-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-01-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-01-dimension-reduction'>
<ul>
<li><a href='#tab-node-01-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-01-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-01-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-01-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-01-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-01-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-01-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-01-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-1-1.png" alt="plot of chunk tab-node-01-dimension-reduction-1"/></p>

</div>
<div id='tab-node-01-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-2-1.png" alt="plot of chunk tab-node-01-dimension-reduction-2"/></p>

</div>
<div id='tab-node-01-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-3-1.png" alt="plot of chunk tab-node-01-dimension-reduction-3"/></p>

</div>
<div id='tab-node-01-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-4-1.png" alt="plot of chunk tab-node-01-dimension-reduction-4"/></p>

</div>
<div id='tab-node-01-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-5-1.png" alt="plot of chunk tab-node-01-dimension-reduction-5"/></p>

</div>
<div id='tab-node-01-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-6-1.png" alt="plot of chunk tab-node-01-dimension-reduction-6"/></p>

</div>
<div id='tab-node-01-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-01-dimension-reduction-7-1.png" alt="plot of chunk tab-node-01-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-01-collect-classes](figure_cola/node-01-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node011


Parent node: [Node01](#Node01).
Child nodes: 
                Node0111-leaf
        ,
                Node0112-leaf
        ,
                Node0113-leaf
        ,
                Node0121-leaf
        ,
                Node0122-leaf
        ,
                Node0123-leaf
        ,
                Node0131-leaf
        ,
                Node0132-leaf
        ,
                Node0133-leaf
        ,
                Node0211-leaf
        ,
                Node0212-leaf
        ,
                Node0221-leaf
        ,
                [Node0222](#Node0222)
        ,
                Node0223-leaf
        ,
                Node0231-leaf
        ,
                Node0232-leaf
        ,
                Node0233-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["011"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 28 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 5.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-011-collect-plots](figure_cola/node-011-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-011-select-partition-number](figure_cola/node-011-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           0.984       0.993         0.4577 0.548   0.548
#> 3 3 1.000           0.982       0.986         0.4932 0.767   0.575
#> 4 4 0.883           0.910       0.894         0.0849 0.937   0.798
#> 5 5 0.902           0.924       0.911         0.0592 0.968   0.874
#> 6 6 0.858           0.862       0.896         0.0307 1.000   1.000
#> 7 7 0.862           0.857       0.883         0.0410 0.947   0.759
#> 8 8 0.837           0.747       0.836         0.0209 0.987   0.921
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 5
#> attr(,"optional")
#> [1] 2 3
```

There is also optional best $k$ = 2 3 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-011-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-011-get-classes'>
<ul>
<li><a href='#tab-node-011-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-011-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-011-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-011-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-011-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-011-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-011-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-011-get-classes-1'>
<p><a id='tab-node-011-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette  p1  p2
#&gt; TCGA.Q9.A6FU.01     2   0.722      0.750 0.2 0.8
#&gt; TCGA.LN.A4A3.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A49X.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.IG.A3YC.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A49N.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.VR.AA7B.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.IG.A3Y9.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A5U7.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.IG.A625.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.IG.A50L.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A49O.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.IG.A3YA.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A7HZ.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.IG.A3QL.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.LN.A4A2.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.L5.A8NQ.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A8I0.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.XP.A8T8.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.VR.A8EX.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.VR.A8EU.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.Z6.A8JD.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A8HZ.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.L5.A88S.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.VR.A8EW.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.VR.AA4G.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.JY.A6FD.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.L5.A8NK.01     2   0.000      0.989 0.0 1.0
#&gt; TCGA.LN.A9FO.01     2   0.000      0.989 0.0 1.0
</code></pre>

<script>
$('#tab-node-011-get-classes-1-a').parent().next().next().hide();
$('#tab-node-011-get-classes-1-a').click(function(){
  $('#tab-node-011-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-011-get-classes-2'>
<p><a id='tab-node-011-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1   p2   p3
#&gt; TCGA.Q9.A6FU.01     2   0.000      0.958  0 1.00 0.00
#&gt; TCGA.LN.A4A3.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A49X.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.IG.A3YC.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A49N.01     2   0.000      0.958  0 1.00 0.00
#&gt; TCGA.VR.AA7B.01     2   0.000      0.958  0 1.00 0.00
#&gt; TCGA.IG.A3Y9.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A5U7.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.IG.A625.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.IG.A50L.01     2   0.000      0.958  0 1.00 0.00
#&gt; TCGA.LN.A49O.01     2   0.000      0.958  0 1.00 0.00
#&gt; TCGA.IG.A3YA.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A7HZ.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.IG.A3QL.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.LN.A4A2.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A8I0.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.VR.A8EX.01     2   0.254      0.948  0 0.92 0.08
#&gt; TCGA.VR.A8EU.01     2   0.000      0.958  0 1.00 0.00
#&gt; TCGA.Z6.A8JD.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A8HZ.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.L5.A88S.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.VR.A8EW.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.VR.AA4G.01     2   0.254      0.948  0 0.92 0.08
#&gt; TCGA.JY.A6FD.01     2   0.254      0.948  0 0.92 0.08
#&gt; TCGA.L5.A8NK.01     2   0.254      0.948  0 0.92 0.08
#&gt; TCGA.LN.A9FO.01     2   0.254      0.948  0 0.92 0.08
</code></pre>

<script>
$('#tab-node-011-get-classes-2-a').parent().next().next().hide();
$('#tab-node-011-get-classes-2-a').click(function(){
  $('#tab-node-011-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-011-get-classes-3'>
<p><a id='tab-node-011-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.Q9.A6FU.01     2  0.3975      0.664 0.00 0.76 0.00 0.24
#&gt; TCGA.LN.A4A3.01     3  0.0707      0.991 0.00 0.02 0.98 0.00
#&gt; TCGA.LN.A49X.01     3  0.0707      0.991 0.00 0.02 0.98 0.00
#&gt; TCGA.IG.A3YC.01     3  0.0707      0.991 0.00 0.02 0.98 0.00
#&gt; TCGA.LN.A49N.01     2  0.4948      0.803 0.00 0.56 0.00 0.44
#&gt; TCGA.VR.AA7B.01     2  0.4134      0.686 0.00 0.74 0.00 0.26
#&gt; TCGA.IG.A3Y9.01     3  0.0000      0.991 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A5U7.01     1  0.3801      0.873 0.78 0.22 0.00 0.00
#&gt; TCGA.IG.A625.01     1  0.3400      0.883 0.82 0.18 0.00 0.00
#&gt; TCGA.IG.A50L.01     4  0.0000      1.000 0.00 0.00 0.00 1.00
#&gt; TCGA.LN.A49O.01     4  0.0000      1.000 0.00 0.00 0.00 1.00
#&gt; TCGA.IG.A3YA.01     3  0.0707      0.991 0.00 0.02 0.98 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.3801      0.873 0.78 0.22 0.00 0.00
#&gt; TCGA.IG.A3QL.01     1  0.3801      0.873 0.78 0.22 0.00 0.00
#&gt; TCGA.LN.A4A2.01     1  0.0000      0.905 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     3  0.0000      0.991 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A8I0.01     1  0.0707      0.898 0.98 0.02 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.0000      0.905 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     2  0.6212      0.875 0.00 0.56 0.06 0.38
#&gt; TCGA.VR.A8EU.01     4  0.0000      1.000 0.00 0.00 0.00 1.00
#&gt; TCGA.Z6.A8JD.01     3  0.0000      0.991 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000      0.905 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     3  0.0000      0.991 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.A8EW.01     1  0.0707      0.898 0.98 0.02 0.00 0.00
#&gt; TCGA.VR.AA4G.01     2  0.6212      0.875 0.00 0.56 0.06 0.38
#&gt; TCGA.JY.A6FD.01     2  0.6212      0.875 0.00 0.56 0.06 0.38
#&gt; TCGA.L5.A8NK.01     2  0.6212      0.875 0.00 0.56 0.06 0.38
#&gt; TCGA.LN.A9FO.01     2  0.6212      0.875 0.00 0.56 0.06 0.38
</code></pre>

<script>
$('#tab-node-011-get-classes-3-a').parent().next().next().hide();
$('#tab-node-011-get-classes-3-a').click(function(){
  $('#tab-node-011-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-011-get-classes-4'>
<p><a id='tab-node-011-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.Q9.A6FU.01     5  0.4613      0.928 0.00 0.36 0.00 0.02 0.62
#&gt; TCGA.LN.A4A3.01     3  0.0000      0.981 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     3  0.0609      0.975 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.IG.A3YC.01     3  0.0000      0.981 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     2  0.0609      0.947 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.VR.AA7B.01     5  0.4726      0.924 0.00 0.40 0.00 0.02 0.58
#&gt; TCGA.IG.A3Y9.01     3  0.1216      0.975 0.00 0.00 0.96 0.02 0.02
#&gt; TCGA.LN.A5U7.01     1  0.4252      0.801 0.70 0.00 0.00 0.02 0.28
#&gt; TCGA.IG.A625.01     1  0.3521      0.841 0.82 0.00 0.00 0.04 0.14
#&gt; TCGA.IG.A50L.01     4  0.1410      0.970 0.00 0.06 0.00 0.94 0.00
#&gt; TCGA.LN.A49O.01     4  0.1732      0.985 0.00 0.08 0.00 0.92 0.00
#&gt; TCGA.IG.A3YA.01     3  0.0609      0.975 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.LN.A7HZ.01     1  0.4252      0.801 0.70 0.00 0.00 0.02 0.28
#&gt; TCGA.IG.A3QL.01     1  0.4252      0.801 0.70 0.00 0.00 0.02 0.28
#&gt; TCGA.LN.A4A2.01     1  0.0609      0.857 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A8NQ.01     3  0.0609      0.981 0.00 0.00 0.98 0.02 0.00
#&gt; TCGA.LN.A8I0.01     1  0.1648      0.840 0.94 0.00 0.00 0.02 0.04
#&gt; TCGA.XP.A8T8.01     1  0.0000      0.862 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     2  0.0000      0.973 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EU.01     4  0.1732      0.985 0.00 0.08 0.00 0.92 0.00
#&gt; TCGA.Z6.A8JD.01     3  0.0609      0.981 0.00 0.00 0.98 0.02 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.0000      0.862 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88S.01     3  0.1216      0.975 0.00 0.00 0.96 0.02 0.02
#&gt; TCGA.VR.A8EW.01     1  0.1648      0.849 0.94 0.00 0.00 0.02 0.04
#&gt; TCGA.VR.AA4G.01     2  0.0000      0.973 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     2  0.0000      0.973 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     2  0.0000      0.973 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     2  0.1410      0.898 0.00 0.94 0.00 0.00 0.06
</code></pre>

<script>
$('#tab-node-011-get-classes-4-a').parent().next().next().hide();
$('#tab-node-011-get-classes-4-a').click(function(){
  $('#tab-node-011-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-011-get-classes-5'>
<p><a id='tab-node-011-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.Q9.A6FU.01     6  0.0937      0.911 0.00 0.04 0.00 0.00 0.00 0.96
#&gt; TCGA.LN.A4A3.01     3  0.0000      0.958 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     3  0.0000      0.958 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YC.01     3  0.0547      0.956 0.00 0.02 0.98 0.00 0.00 0.00
#&gt; TCGA.LN.A49N.01     2  0.2094      0.873 0.00 0.90 0.00 0.00 0.08 0.02
#&gt; TCGA.VR.AA7B.01     6  0.2350      0.911 0.00 0.10 0.00 0.00 0.02 0.88
#&gt; TCGA.IG.A3Y9.01     3  0.2581      0.903 0.00 0.02 0.86 0.00 0.12 0.00
#&gt; TCGA.LN.A5U7.01     1  0.1807      0.753 0.92 0.00 0.00 0.00 0.06 0.02
#&gt; TCGA.IG.A625.01     1  0.0547      0.779 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.IG.A50L.01     4  0.4632      0.883 0.00 0.04 0.00 0.52 0.44 0.00
#&gt; TCGA.LN.A49O.01     4  0.3950      0.875 0.00 0.04 0.00 0.72 0.24 0.00
#&gt; TCGA.IG.A3YA.01     3  0.0547      0.956 0.00 0.02 0.98 0.00 0.00 0.00
#&gt; TCGA.LN.A7HZ.01     1  0.1807      0.753 0.92 0.00 0.00 0.00 0.06 0.02
#&gt; TCGA.IG.A3QL.01     1  0.1807      0.753 0.92 0.00 0.00 0.00 0.06 0.02
#&gt; TCGA.LN.A4A2.01     1  0.3309      0.812 0.72 0.00 0.00 0.28 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     3  0.0547      0.958 0.00 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A8I0.01     1  0.4462      0.782 0.66 0.00 0.00 0.28 0.00 0.06
#&gt; TCGA.XP.A8T8.01     1  0.3309      0.812 0.72 0.00 0.00 0.28 0.00 0.00
#&gt; TCGA.VR.A8EX.01     2  0.1556      0.873 0.00 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.VR.A8EU.01     4  0.4482      0.909 0.00 0.04 0.00 0.60 0.36 0.00
#&gt; TCGA.Z6.A8JD.01     3  0.0547      0.958 0.00 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.LN.A8HZ.01     1  0.3309      0.812 0.72 0.00 0.00 0.28 0.00 0.00
#&gt; TCGA.L5.A88S.01     3  0.2048      0.908 0.00 0.00 0.88 0.00 0.12 0.00
#&gt; TCGA.VR.A8EW.01     1  0.5236      0.776 0.66 0.00 0.00 0.22 0.04 0.08
#&gt; TCGA.VR.AA4G.01     2  0.0547      0.892 0.00 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.JY.A6FD.01     2  0.0000      0.893 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     2  0.0547      0.893 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.LN.A9FO.01     2  0.3499      0.630 0.00 0.68 0.00 0.00 0.32 0.00
</code></pre>

<script>
$('#tab-node-011-get-classes-5-a').parent().next().next().hide();
$('#tab-node-011-get-classes-5-a').click(function(){
  $('#tab-node-011-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-011-get-classes-6'>
<p><a id='tab-node-011-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.Q9.A6FU.01     6  0.0504      0.959 0.00 0.02 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.LN.A4A3.01     3  0.0000      0.893 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     3  0.0504      0.894 0.02 0.00 0.98 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YC.01     3  0.0863      0.888 0.00 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.LN.A49N.01     2  0.2569      0.821 0.02 0.84 0.00 0.00 0.00 0.00 0.14
#&gt; TCGA.VR.AA7B.01     6  0.1860      0.959 0.04 0.02 0.00 0.00 0.00 0.92 0.02
#&gt; TCGA.IG.A3Y9.01     3  0.3294      0.727 0.00 0.00 0.66 0.00 0.00 0.00 0.34
#&gt; TCGA.LN.A5U7.01     5  0.0504      0.908 0.00 0.00 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.IG.A625.01     5  0.2259      0.695 0.16 0.00 0.00 0.00 0.84 0.00 0.00
#&gt; TCGA.IG.A50L.01     4  0.2569      0.817 0.02 0.00 0.00 0.84 0.00 0.00 0.14
#&gt; TCGA.LN.A49O.01     4  0.1363      0.880 0.04 0.00 0.00 0.94 0.00 0.00 0.02
#&gt; TCGA.IG.A3YA.01     3  0.0863      0.888 0.00 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.LN.A7HZ.01     5  0.0000      0.904 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3QL.01     5  0.0504      0.908 0.00 0.00 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.LN.A4A2.01     1  0.2832      0.929 0.76 0.00 0.00 0.00 0.24 0.00 0.00
#&gt; TCGA.L5.A8NQ.01     3  0.1505      0.891 0.02 0.00 0.94 0.00 0.00 0.02 0.02
#&gt; TCGA.LN.A8I0.01     1  0.2832      0.929 0.76 0.00 0.00 0.00 0.24 0.00 0.00
#&gt; TCGA.XP.A8T8.01     1  0.2945      0.930 0.74 0.00 0.00 0.00 0.26 0.00 0.00
#&gt; TCGA.VR.A8EX.01     2  0.2569      0.821 0.02 0.84 0.00 0.00 0.00 0.00 0.14
#&gt; TCGA.VR.A8EU.01     4  0.0000      0.891 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.Z6.A8JD.01     3  0.1505      0.891 0.02 0.00 0.94 0.00 0.00 0.02 0.02
#&gt; TCGA.LN.A8HZ.01     1  0.2945      0.930 0.74 0.00 0.00 0.00 0.26 0.00 0.00
#&gt; TCGA.L5.A88S.01     3  0.3139      0.739 0.00 0.00 0.70 0.00 0.00 0.00 0.30
#&gt; TCGA.VR.A8EW.01     1  0.5164      0.748 0.54 0.00 0.00 0.00 0.26 0.00 0.20
#&gt; TCGA.VR.AA4G.01     2  0.0000      0.864 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     2  0.0000      0.864 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     2  0.0000      0.864 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     2  0.4630      0.555 0.12 0.62 0.00 0.00 0.00 0.00 0.26
</code></pre>

<script>
$('#tab-node-011-get-classes-6-a').parent().next().next().hide();
$('#tab-node-011-get-classes-6-a').click(function(){
  $('#tab-node-011-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-011-get-classes-7'>
<p><a id='tab-node-011-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.Q9.A6FU.01     6  0.0000      0.824 0.00 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A3.01     3  0.0000      0.800 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49X.01     3  0.0808      0.799 0.00 0.00 0.96 0.04 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3YC.01     3  0.0471      0.798 0.00 0.00 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.LN.A49N.01     2  0.2650      0.690 0.00 0.76 0.00 0.00 0.00 0.00 0.24 0.00
#&gt; TCGA.VR.AA7B.01     6  0.3503      0.823 0.00 0.02 0.00 0.12 0.00 0.78 0.00 0.08
#&gt; TCGA.IG.A3Y9.01     3  0.6271      0.459 0.00 0.00 0.42 0.14 0.20 0.00 0.00 0.24
#&gt; TCGA.LN.A5U7.01     5  0.2534      0.916 0.22 0.00 0.00 0.00 0.78 0.00 0.00 0.00
#&gt; TCGA.IG.A625.01     5  0.4887      0.770 0.32 0.00 0.00 0.04 0.58 0.00 0.02 0.04
#&gt; TCGA.IG.A50L.01     7  0.0471      0.676 0.00 0.02 0.00 0.00 0.00 0.00 0.98 0.00
#&gt; TCGA.LN.A49O.01     7  0.3618      0.757 0.00 0.02 0.00 0.38 0.00 0.00 0.60 0.00
#&gt; TCGA.IG.A3YA.01     3  0.0471      0.798 0.00 0.00 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.LN.A7HZ.01     5  0.3095      0.909 0.24 0.00 0.00 0.00 0.74 0.00 0.00 0.02
#&gt; TCGA.IG.A3QL.01     5  0.2534      0.916 0.22 0.00 0.00 0.00 0.78 0.00 0.00 0.00
#&gt; TCGA.LN.A4A2.01     1  0.0471      0.883 0.98 0.00 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NQ.01     3  0.2407      0.790 0.00 0.00 0.86 0.08 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A8I0.01     1  0.0941      0.876 0.96 0.00 0.00 0.00 0.00 0.02 0.00 0.02
#&gt; TCGA.XP.A8T8.01     1  0.0000      0.883 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EX.01     2  0.2650      0.690 0.00 0.76 0.00 0.00 0.00 0.00 0.24 0.00
#&gt; TCGA.VR.A8EU.01     7  0.3426      0.793 0.00 0.02 0.00 0.22 0.02 0.00 0.74 0.00
#&gt; TCGA.Z6.A8JD.01     3  0.2407      0.790 0.00 0.00 0.86 0.08 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A8HZ.01     1  0.0471      0.874 0.98 0.00 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A88S.01     3  0.6211      0.465 0.00 0.00 0.44 0.14 0.20 0.00 0.00 0.22
#&gt; TCGA.VR.A8EW.01     1  0.3880      0.579 0.64 0.00 0.00 0.32 0.00 0.02 0.00 0.02
#&gt; TCGA.VR.AA4G.01     2  0.0000      0.783 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FD.01     2  0.0000      0.783 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NK.01     2  0.0000      0.783 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FO.01     8  0.3237      0.000 0.00 0.40 0.00 0.00 0.00 0.00 0.00 0.60
</code></pre>

<script>
$('#tab-node-011-get-classes-7-a').parent().next().next().hide();
$('#tab-node-011-get-classes-7-a').click(function(){
  $('#tab-node-011-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-011-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-011-consensus-heatmap'>
<ul>
<li><a href='#tab-node-011-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-011-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-011-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-011-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-011-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-011-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-011-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-011-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-011-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-011-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-011-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-011-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-011-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-011-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-011-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-011-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-011-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-011-membership-heatmap'>
<ul>
<li><a href='#tab-node-011-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-011-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-011-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-011-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-011-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-011-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-011-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-011-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-1-1.png" alt="plot of chunk tab-node-011-membership-heatmap-1"/></p>

</div>
<div id='tab-node-011-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-2-1.png" alt="plot of chunk tab-node-011-membership-heatmap-2"/></p>

</div>
<div id='tab-node-011-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-3-1.png" alt="plot of chunk tab-node-011-membership-heatmap-3"/></p>

</div>
<div id='tab-node-011-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-4-1.png" alt="plot of chunk tab-node-011-membership-heatmap-4"/></p>

</div>
<div id='tab-node-011-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-5-1.png" alt="plot of chunk tab-node-011-membership-heatmap-5"/></p>

</div>
<div id='tab-node-011-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-6-1.png" alt="plot of chunk tab-node-011-membership-heatmap-6"/></p>

</div>
<div id='tab-node-011-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-011-membership-heatmap-7-1.png" alt="plot of chunk tab-node-011-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-011-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-011-get-signatures'>
<ul>
<li><a href='#tab-node-011-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-011-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-011-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-011-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-011-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-011-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-011-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-011-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-1-1.png" alt="plot of chunk tab-node-011-get-signatures-1"/></p>

</div>
<div id='tab-node-011-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-2-1.png" alt="plot of chunk tab-node-011-get-signatures-2"/></p>

</div>
<div id='tab-node-011-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-3-1.png" alt="plot of chunk tab-node-011-get-signatures-3"/></p>

</div>
<div id='tab-node-011-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-4-1.png" alt="plot of chunk tab-node-011-get-signatures-4"/></p>

</div>
<div id='tab-node-011-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-5-1.png" alt="plot of chunk tab-node-011-get-signatures-5"/></p>

</div>
<div id='tab-node-011-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-6-1.png" alt="plot of chunk tab-node-011-get-signatures-6"/></p>

</div>
<div id='tab-node-011-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-011-get-signatures-7-1.png" alt="plot of chunk tab-node-011-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-011-signature_compare](figure_cola/node-011-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-011-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-011-dimension-reduction'>
<ul>
<li><a href='#tab-node-011-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-011-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-011-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-011-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-011-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-011-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-011-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-011-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-1-1.png" alt="plot of chunk tab-node-011-dimension-reduction-1"/></p>

</div>
<div id='tab-node-011-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-2-1.png" alt="plot of chunk tab-node-011-dimension-reduction-2"/></p>

</div>
<div id='tab-node-011-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-3-1.png" alt="plot of chunk tab-node-011-dimension-reduction-3"/></p>

</div>
<div id='tab-node-011-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-4-1.png" alt="plot of chunk tab-node-011-dimension-reduction-4"/></p>

</div>
<div id='tab-node-011-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-5-1.png" alt="plot of chunk tab-node-011-dimension-reduction-5"/></p>

</div>
<div id='tab-node-011-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-6-1.png" alt="plot of chunk tab-node-011-dimension-reduction-6"/></p>

</div>
<div id='tab-node-011-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-011-dimension-reduction-7-1.png" alt="plot of chunk tab-node-011-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-011-collect-classes](figure_cola/node-011-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node012


Parent node: [Node01](#Node01).
Child nodes: 
                Node0111-leaf
        ,
                Node0112-leaf
        ,
                Node0113-leaf
        ,
                Node0121-leaf
        ,
                Node0122-leaf
        ,
                Node0123-leaf
        ,
                Node0131-leaf
        ,
                Node0132-leaf
        ,
                Node0133-leaf
        ,
                Node0211-leaf
        ,
                Node0212-leaf
        ,
                Node0221-leaf
        ,
                [Node0222](#Node0222)
        ,
                Node0223-leaf
        ,
                Node0231-leaf
        ,
                Node0232-leaf
        ,
                Node0233-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["012"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 20 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-012-collect-plots](figure_cola/node-012-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-012-select-partition-number](figure_cola/node-012-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           0.998       0.999         0.4788 0.521   0.521
#> 3 3 1.000           0.987       0.990         0.3729 0.758   0.562
#> 4 4 0.742           0.900       0.908         0.1458 0.889   0.677
#> 5 5 0.821           0.610       0.811         0.0577 0.953   0.800
#> 6 6 0.863           0.740       0.830         0.0421 0.942   0.725
#> 7 7 0.826           0.544       0.755         0.0283 0.937   0.657
#> 8 8 0.832           0.675       0.868         0.0258 0.979   0.852
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-012-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-012-get-classes'>
<ul>
<li><a href='#tab-node-012-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-012-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-012-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-012-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-012-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-012-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-012-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-012-get-classes-1'>
<p><a id='tab-node-012-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2
#&gt; TCGA.LN.A4A4.01     2   0.000      0.997 0.00 1.00
#&gt; TCGA.LN.A7HV.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.VR.A8EP.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.JY.A6FE.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OM.01     2   0.000      0.997 0.00 1.00
#&gt; TCGA.LN.A4A6.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A49R.01     2   0.000      0.997 0.00 1.00
#&gt; TCGA.LN.A49U.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A7HX.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A4A8.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A49Y.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A4A1.01     2   0.141      0.980 0.02 0.98
#&gt; TCGA.LN.A49S.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.IG.A8O2.01     2   0.000      0.997 0.00 1.00
#&gt; TCGA.IG.A5B8.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A4MR.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.LN.A4A9.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.JY.A6FA.01     2   0.000      0.997 0.00 1.00
#&gt; TCGA.VR.A8EO.01     2   0.000      0.997 0.00 1.00
#&gt; TCGA.XP.A8T6.01     1   0.000      1.000 1.00 0.00
</code></pre>

<script>
$('#tab-node-012-get-classes-1-a').parent().next().next().hide();
$('#tab-node-012-get-classes-1-a').click(function(){
  $('#tab-node-012-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-012-get-classes-2'>
<p><a id='tab-node-012-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.LN.A4A4.01     2  0.0000      0.990 0.00 1.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.0892      0.991 0.98 0.00 0.02
#&gt; TCGA.VR.A8EP.01     1  0.0892      0.991 0.98 0.00 0.02
#&gt; TCGA.JY.A6FE.01     1  0.0892      0.991 0.98 0.00 0.02
#&gt; TCGA.L5.A4OM.01     2  0.0892      0.985 0.00 0.98 0.02
#&gt; TCGA.LN.A4A6.01     1  0.0000      0.987 1.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     2  0.0000      0.990 0.00 1.00 0.00
#&gt; TCGA.LN.A49U.01     3  0.0892      0.969 0.02 0.00 0.98
#&gt; TCGA.LN.A7HX.01     3  0.0000      0.987 0.00 0.00 1.00
#&gt; TCGA.LN.A4A8.01     1  0.0000      0.987 1.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     1  0.0000      0.987 1.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     3  0.0000      0.987 0.00 0.00 1.00
#&gt; TCGA.LN.A49S.01     1  0.0892      0.991 0.98 0.00 0.02
#&gt; TCGA.IG.A8O2.01     3  0.0892      0.969 0.00 0.02 0.98
#&gt; TCGA.IG.A5B8.01     1  0.0892      0.991 0.98 0.00 0.02
#&gt; TCGA.LN.A4MR.01     1  0.0000      0.987 1.00 0.00 0.00
#&gt; TCGA.LN.A4A9.01     1  0.0892      0.991 0.98 0.00 0.02
#&gt; TCGA.JY.A6FA.01     2  0.0000      0.990 0.00 1.00 0.00
#&gt; TCGA.VR.A8EO.01     2  0.0892      0.985 0.00 0.98 0.02
#&gt; TCGA.XP.A8T6.01     3  0.0000      0.987 0.00 0.00 1.00
</code></pre>

<script>
$('#tab-node-012-get-classes-2-a').parent().next().next().hide();
$('#tab-node-012-get-classes-2-a').click(function(){
  $('#tab-node-012-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-012-get-classes-3'>
<p><a id='tab-node-012-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.LN.A4A4.01     2  0.0000      0.911 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A7HV.01     1  0.2647      0.887 0.88 0.00 0.00 0.12
#&gt; TCGA.VR.A8EP.01     1  0.0707      0.848 0.98 0.00 0.02 0.00
#&gt; TCGA.JY.A6FE.01     1  0.0000      0.867 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.01     2  0.4553      0.863 0.00 0.78 0.04 0.18
#&gt; TCGA.LN.A4A6.01     4  0.3610      1.000 0.20 0.00 0.00 0.80
#&gt; TCGA.LN.A49R.01     2  0.0000      0.911 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     3  0.3801      0.748 0.22 0.00 0.78 0.00
#&gt; TCGA.LN.A7HX.01     3  0.0000      0.939 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A4A8.01     4  0.3610      1.000 0.20 0.00 0.00 0.80
#&gt; TCGA.LN.A49Y.01     4  0.3610      1.000 0.20 0.00 0.00 0.80
#&gt; TCGA.LN.A4A1.01     3  0.0000      0.939 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A49S.01     1  0.2647      0.887 0.88 0.00 0.00 0.12
#&gt; TCGA.IG.A8O2.01     3  0.0707      0.930 0.00 0.00 0.98 0.02
#&gt; TCGA.IG.A5B8.01     1  0.2647      0.887 0.88 0.00 0.00 0.12
#&gt; TCGA.LN.A4MR.01     1  0.3400      0.813 0.82 0.00 0.00 0.18
#&gt; TCGA.LN.A4A9.01     1  0.0000      0.867 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FA.01     2  0.0000      0.911 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     2  0.4553      0.863 0.00 0.78 0.04 0.18
#&gt; TCGA.XP.A8T6.01     3  0.0000      0.939 0.00 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-012-get-classes-3-a').parent().next().next().hide();
$('#tab-node-012-get-classes-3-a').click(function(){
  $('#tab-node-012-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-012-get-classes-4'>
<p><a id='tab-node-012-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1  p2   p3   p4   p5
#&gt; TCGA.LN.A4A4.01     2  0.4307      0.426 0.00 0.5 0.00 0.00 0.50
#&gt; TCGA.LN.A7HV.01     1  0.1410      0.945 0.94 0.0 0.00 0.06 0.00
#&gt; TCGA.VR.A8EP.01     1  0.1410      0.895 0.94 0.0 0.06 0.00 0.00
#&gt; TCGA.JY.A6FE.01     1  0.0609      0.932 0.98 0.0 0.00 0.00 0.02
#&gt; TCGA.L5.A4OM.01     2  0.0000      0.582 0.00 1.0 0.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     4  0.1043      1.000 0.04 0.0 0.00 0.96 0.00
#&gt; TCGA.LN.A49R.01     5  0.4307     -0.785 0.00 0.5 0.00 0.00 0.50
#&gt; TCGA.LN.A49U.01     3  0.2280      0.436 0.12 0.0 0.88 0.00 0.00
#&gt; TCGA.LN.A7HX.01     3  0.3109      0.619 0.00 0.0 0.80 0.00 0.20
#&gt; TCGA.LN.A4A8.01     4  0.1043      1.000 0.04 0.0 0.00 0.96 0.00
#&gt; TCGA.LN.A49Y.01     4  0.1043      1.000 0.04 0.0 0.00 0.96 0.00
#&gt; TCGA.LN.A4A1.01     3  0.4262      0.598 0.00 0.0 0.56 0.00 0.44
#&gt; TCGA.LN.A49S.01     1  0.1410      0.945 0.94 0.0 0.00 0.06 0.00
#&gt; TCGA.IG.A8O2.01     5  0.5178     -0.795 0.00 0.0 0.48 0.04 0.48
#&gt; TCGA.IG.A5B8.01     1  0.1410      0.945 0.94 0.0 0.00 0.06 0.00
#&gt; TCGA.LN.A4MR.01     1  0.2331      0.923 0.90 0.0 0.00 0.08 0.02
#&gt; TCGA.LN.A4A9.01     1  0.0609      0.924 0.98 0.0 0.02 0.00 0.00
#&gt; TCGA.JY.A6FA.01     2  0.4307      0.426 0.00 0.5 0.00 0.00 0.50
#&gt; TCGA.VR.A8EO.01     2  0.0000      0.582 0.00 1.0 0.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     3  0.4227      0.607 0.00 0.0 0.58 0.00 0.42
</code></pre>

<script>
$('#tab-node-012-get-classes-4-a').parent().next().next().hide();
$('#tab-node-012-get-classes-4-a').click(function(){
  $('#tab-node-012-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-012-get-classes-5'>
<p><a id='tab-node-012-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.LN.A4A4.01     5  0.3706      1.000 0.00 0.38 0.00 0.00 0.62 0.00
#&gt; TCGA.LN.A7HV.01     1  0.0547      0.913 0.98 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.VR.A8EP.01     1  0.1480      0.881 0.94 0.00 0.00 0.00 0.02 0.04
#&gt; TCGA.JY.A6FE.01     1  0.3309      0.752 0.72 0.00 0.00 0.00 0.28 0.00
#&gt; TCGA.L5.A4OM.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A6.01     4  0.0000      1.000 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     5  0.3706      1.000 0.00 0.38 0.00 0.00 0.62 0.00
#&gt; TCGA.LN.A49U.01     3  0.4420      0.284 0.02 0.00 0.66 0.00 0.02 0.30
#&gt; TCGA.LN.A7HX.01     3  0.0000      0.226 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A8.01     4  0.0000      1.000 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     4  0.0000      1.000 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     3  0.3864     -0.769 0.00 0.00 0.52 0.00 0.00 0.48
#&gt; TCGA.LN.A49S.01     1  0.0547      0.913 0.98 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.IG.A8O2.01     6  0.4552      0.534 0.00 0.00 0.30 0.00 0.06 0.64
#&gt; TCGA.IG.A5B8.01     1  0.0547      0.913 0.98 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.LN.A4MR.01     1  0.1092      0.909 0.96 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.LN.A4A9.01     1  0.2631      0.824 0.82 0.00 0.00 0.00 0.18 0.00
#&gt; TCGA.JY.A6FA.01     5  0.3706      1.000 0.00 0.38 0.00 0.00 0.62 0.00
#&gt; TCGA.VR.A8EO.01     2  0.0000      1.000 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     6  0.3864      0.414 0.00 0.00 0.48 0.00 0.00 0.52
</code></pre>

<script>
$('#tab-node-012-get-classes-5-a').parent().next().next().hide();
$('#tab-node-012-get-classes-5-a').click(function(){
  $('#tab-node-012-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-012-get-classes-6'>
<p><a id='tab-node-012-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.LN.A4A4.01     5  0.2906      0.768 0.00 0.00 0.00 0.02 0.80 0.00 0.18
#&gt; TCGA.LN.A7HV.01     1  0.1006      0.773 0.96 0.00 0.00 0.02 0.00 0.00 0.02
#&gt; TCGA.VR.A8EP.01     1  0.1860      0.683 0.92 0.02 0.02 0.00 0.00 0.00 0.04
#&gt; TCGA.JY.A6FE.01     7  0.3496      0.000 0.42 0.00 0.00 0.00 0.00 0.00 0.58
#&gt; TCGA.L5.A4OM.01     2  0.2945      1.000 0.00 0.74 0.00 0.00 0.26 0.00 0.00
#&gt; TCGA.LN.A4A6.01     4  0.0504      1.000 0.02 0.00 0.00 0.98 0.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     5  0.0000      0.890 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49U.01     3  0.2803      0.293 0.00 0.10 0.84 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A7HX.01     3  0.2572      0.275 0.00 0.00 0.80 0.00 0.00 0.20 0.00
#&gt; TCGA.LN.A4A8.01     4  0.0504      1.000 0.02 0.00 0.00 0.98 0.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     4  0.0504      1.000 0.02 0.00 0.00 0.98 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     6  0.6147     -0.288 0.00 0.06 0.38 0.00 0.00 0.40 0.16
#&gt; TCGA.LN.A49S.01     1  0.0504      0.779 0.98 0.00 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.IG.A8O2.01     6  0.0000      0.153 0.00 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A5B8.01     1  0.0504      0.779 0.98 0.00 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.LN.A4MR.01     1  0.2509      0.695 0.88 0.06 0.00 0.02 0.00 0.00 0.04
#&gt; TCGA.LN.A4A9.01     1  0.3755     -0.402 0.64 0.02 0.00 0.00 0.00 0.00 0.34
#&gt; TCGA.JY.A6FA.01     5  0.0000      0.890 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     2  0.2945      1.000 0.00 0.74 0.00 0.00 0.26 0.00 0.00
#&gt; TCGA.XP.A8T6.01     3  0.6698     -0.401 0.02 0.06 0.38 0.00 0.00 0.34 0.20
</code></pre>

<script>
$('#tab-node-012-get-classes-6-a').parent().next().next().hide();
$('#tab-node-012-get-classes-6-a').click(function(){
  $('#tab-node-012-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-012-get-classes-7'>
<p><a id='tab-node-012-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.LN.A4A4.01     5  0.3528     0.7255 0.00 0.00 0.00 0.00 0.74 0.00 0.18 0.08
#&gt; TCGA.LN.A7HV.01     1  0.0000     0.7941 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EP.01     1  0.2132     0.7229 0.88 0.04 0.00 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.JY.A6FE.01     7  0.2406     0.0000 0.20 0.00 0.00 0.00 0.00 0.00 0.80 0.00
#&gt; TCGA.L5.A4OM.01     2  0.2719     0.9793 0.00 0.80 0.00 0.00 0.18 0.00 0.02 0.00
#&gt; TCGA.LN.A4A6.01     4  0.0000     0.9831 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49R.01     5  0.0471     0.8633 0.00 0.00 0.00 0.00 0.98 0.00 0.00 0.02
#&gt; TCGA.LN.A49U.01     3  0.1091     0.4351 0.00 0.00 0.94 0.00 0.00 0.06 0.00 0.00
#&gt; TCGA.LN.A7HX.01     3  0.3737     0.1916 0.00 0.00 0.50 0.00 0.00 0.48 0.02 0.00
#&gt; TCGA.LN.A4A8.01     4  0.0000     0.9831 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49Y.01     4  0.0808     0.9659 0.00 0.04 0.00 0.96 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A1.01     6  0.0000     0.8917 0.00 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A49S.01     1  0.0000     0.7941 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A8O2.01     8  0.3142     0.0000 0.00 0.00 0.00 0.00 0.00 0.36 0.00 0.64
#&gt; TCGA.IG.A5B8.01     1  0.0000     0.7941 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4MR.01     1  0.3913     0.5582 0.74 0.04 0.06 0.00 0.00 0.00 0.00 0.16
#&gt; TCGA.LN.A4A9.01     1  0.4415     0.0869 0.60 0.06 0.00 0.00 0.00 0.00 0.32 0.02
#&gt; TCGA.JY.A6FA.01     5  0.0000     0.8633 0.00 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EO.01     2  0.2267     0.9794 0.00 0.82 0.00 0.00 0.18 0.00 0.00 0.00
#&gt; TCGA.XP.A8T6.01     6  0.1275     0.8918 0.00 0.04 0.00 0.00 0.00 0.94 0.00 0.02
</code></pre>

<script>
$('#tab-node-012-get-classes-7-a').parent().next().next().hide();
$('#tab-node-012-get-classes-7-a').click(function(){
  $('#tab-node-012-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-012-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-012-consensus-heatmap'>
<ul>
<li><a href='#tab-node-012-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-012-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-012-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-012-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-012-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-012-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-012-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-012-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-012-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-012-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-012-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-012-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-012-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-012-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-012-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-012-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-012-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-012-membership-heatmap'>
<ul>
<li><a href='#tab-node-012-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-012-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-012-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-012-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-012-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-012-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-012-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-012-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-1-1.png" alt="plot of chunk tab-node-012-membership-heatmap-1"/></p>

</div>
<div id='tab-node-012-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-2-1.png" alt="plot of chunk tab-node-012-membership-heatmap-2"/></p>

</div>
<div id='tab-node-012-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-3-1.png" alt="plot of chunk tab-node-012-membership-heatmap-3"/></p>

</div>
<div id='tab-node-012-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-4-1.png" alt="plot of chunk tab-node-012-membership-heatmap-4"/></p>

</div>
<div id='tab-node-012-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-5-1.png" alt="plot of chunk tab-node-012-membership-heatmap-5"/></p>

</div>
<div id='tab-node-012-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-6-1.png" alt="plot of chunk tab-node-012-membership-heatmap-6"/></p>

</div>
<div id='tab-node-012-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-012-membership-heatmap-7-1.png" alt="plot of chunk tab-node-012-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-012-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-012-get-signatures'>
<ul>
<li><a href='#tab-node-012-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-012-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-012-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-012-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-012-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-012-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-012-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-012-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-1-1.png" alt="plot of chunk tab-node-012-get-signatures-1"/></p>

</div>
<div id='tab-node-012-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-2-1.png" alt="plot of chunk tab-node-012-get-signatures-2"/></p>

</div>
<div id='tab-node-012-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-3-1.png" alt="plot of chunk tab-node-012-get-signatures-3"/></p>

</div>
<div id='tab-node-012-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-4-1.png" alt="plot of chunk tab-node-012-get-signatures-4"/></p>

</div>
<div id='tab-node-012-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-5-1.png" alt="plot of chunk tab-node-012-get-signatures-5"/></p>

</div>
<div id='tab-node-012-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-6-1.png" alt="plot of chunk tab-node-012-get-signatures-6"/></p>

</div>
<div id='tab-node-012-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-012-get-signatures-7-1.png" alt="plot of chunk tab-node-012-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-012-signature_compare](figure_cola/node-012-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-012-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-012-dimension-reduction'>
<ul>
<li><a href='#tab-node-012-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-012-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-012-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-012-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-012-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-012-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-012-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-012-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-1-1.png" alt="plot of chunk tab-node-012-dimension-reduction-1"/></p>

</div>
<div id='tab-node-012-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-2-1.png" alt="plot of chunk tab-node-012-dimension-reduction-2"/></p>

</div>
<div id='tab-node-012-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-3-1.png" alt="plot of chunk tab-node-012-dimension-reduction-3"/></p>

</div>
<div id='tab-node-012-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-4-1.png" alt="plot of chunk tab-node-012-dimension-reduction-4"/></p>

</div>
<div id='tab-node-012-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-5-1.png" alt="plot of chunk tab-node-012-dimension-reduction-5"/></p>

</div>
<div id='tab-node-012-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-6-1.png" alt="plot of chunk tab-node-012-dimension-reduction-6"/></p>

</div>
<div id='tab-node-012-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-012-dimension-reduction-7-1.png" alt="plot of chunk tab-node-012-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-012-collect-classes](figure_cola/node-012-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node013


Parent node: [Node01](#Node01).
Child nodes: 
                Node0111-leaf
        ,
                Node0112-leaf
        ,
                Node0113-leaf
        ,
                Node0121-leaf
        ,
                Node0122-leaf
        ,
                Node0123-leaf
        ,
                Node0131-leaf
        ,
                Node0132-leaf
        ,
                Node0133-leaf
        ,
                Node0211-leaf
        ,
                Node0212-leaf
        ,
                Node0221-leaf
        ,
                [Node0222](#Node0222)
        ,
                Node0223-leaf
        ,
                Node0231-leaf
        ,
                Node0232-leaf
        ,
                Node0233-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["013"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 23 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-013-collect-plots](figure_cola/node-013-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-013-select-partition-number](figure_cola/node-013-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           0.939       0.979         0.5181 0.486   0.486
#> 3 3 1.000           0.953       0.983         0.3372 0.723   0.481
#> 4 4 0.775           0.811       0.890         0.1044 0.877   0.627
#> 5 5 0.844           0.888       0.920         0.0620 0.913   0.645
#> 6 6 0.852           0.829       0.890         0.0281 1.000   1.000
#> 7 7 0.814           0.708       0.846         0.0263 0.988   0.932
#> 8 8 0.843           0.506       0.677         0.0160 0.897   0.480
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-013-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-013-get-classes'>
<ul>
<li><a href='#tab-node-013-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-013-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-013-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-013-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-013-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-013-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-013-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-013-get-classes-1'>
<p><a id='tab-node-013-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2
#&gt; TCGA.S8.A6BW.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.V5.A7RC.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.KH.A6WC.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.L7.A56G.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.LN.A49K.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.V5.A7RC.06     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.IG.A4P3.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.L5.A43H.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.LN.A7HY.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.LN.A49P.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.LN.A49W.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.LN.A7HW.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.LN.A4MQ.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.LN.A8I1.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.LN.A5U5.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.VR.A8EZ.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.VR.A8ER.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.IG.A97H.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.IG.A97I.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.IG.A5S3.01     2   0.000     0.9591 0.00 1.00
#&gt; TCGA.LN.A5U6.01     2   0.999     0.0769 0.48 0.52
#&gt; TCGA.LN.A9FQ.01     1   0.000     1.0000 1.00 0.00
#&gt; TCGA.LN.A9FR.01     2   0.000     0.9591 0.00 1.00
</code></pre>

<script>
$('#tab-node-013-get-classes-1-a').parent().next().next().hide();
$('#tab-node-013-get-classes-1-a').click(function(){
  $('#tab-node-013-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-013-get-classes-2'>
<p><a id='tab-node-013-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1  p2  p3
#&gt; TCGA.S8.A6BW.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.V5.A7RC.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.KH.A6WC.01     2   0.000      0.931  0 1.0 0.0
#&gt; TCGA.L7.A56G.01     2   0.000      0.931  0 1.0 0.0
#&gt; TCGA.LN.A49K.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.V5.A7RC.06     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.IG.A4P3.01     2   0.000      0.931  0 1.0 0.0
#&gt; TCGA.L5.A43H.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.LN.A7HY.01     2   0.000      0.931  0 1.0 0.0
#&gt; TCGA.LN.A49P.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.LN.A49W.01     2   0.000      0.931  0 1.0 0.0
#&gt; TCGA.LN.A7HW.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.LN.A4MQ.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.LN.A8I1.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.LN.A5U5.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.VR.A8EZ.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.VR.A8ER.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.IG.A97H.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.IG.A97I.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.IG.A5S3.01     2   0.000      0.931  0 1.0 0.0
#&gt; TCGA.LN.A5U6.01     3   0.000      1.000  0 0.0 1.0
#&gt; TCGA.LN.A9FQ.01     1   0.000      1.000  1 0.0 0.0
#&gt; TCGA.LN.A9FR.01     2   0.613      0.333  0 0.6 0.4
</code></pre>

<script>
$('#tab-node-013-get-classes-2-a').parent().next().next().hide();
$('#tab-node-013-get-classes-2-a').click(function(){
  $('#tab-node-013-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-013-get-classes-3'>
<p><a id='tab-node-013-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette  p1   p2   p3   p4
#&gt; TCGA.S8.A6BW.01     4   0.000      0.855 0.0 0.00 0.00 1.00
#&gt; TCGA.V5.A7RC.01     1   0.000      0.917 1.0 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     2   0.340      0.876 0.0 0.82 0.00 0.18
#&gt; TCGA.L7.A56G.01     2   0.000      0.832 0.0 1.00 0.00 0.00
#&gt; TCGA.LN.A49K.01     1   0.441      0.705 0.7 0.00 0.30 0.00
#&gt; TCGA.V5.A7RC.06     1   0.000      0.917 1.0 0.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     4   0.452      0.367 0.0 0.32 0.00 0.68
#&gt; TCGA.L5.A43H.01     3   0.121      0.698 0.0 0.00 0.96 0.04
#&gt; TCGA.LN.A7HY.01     2   0.340      0.876 0.0 0.82 0.00 0.18
#&gt; TCGA.LN.A49P.01     4   0.000      0.855 0.0 0.00 0.00 1.00
#&gt; TCGA.LN.A49W.01     2   0.340      0.876 0.0 0.82 0.00 0.18
#&gt; TCGA.LN.A7HW.01     1   0.441      0.705 0.7 0.00 0.30 0.00
#&gt; TCGA.LN.A4MQ.01     1   0.000      0.917 1.0 0.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     3   0.441      0.763 0.0 0.00 0.70 0.30
#&gt; TCGA.LN.A5U5.01     3   0.441      0.763 0.0 0.00 0.70 0.30
#&gt; TCGA.VR.A8EZ.01     1   0.000      0.917 1.0 0.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1   0.000      0.917 1.0 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     3   0.121      0.698 0.0 0.00 0.96 0.04
#&gt; TCGA.IG.A97I.01     4   0.121      0.840 0.0 0.00 0.04 0.96
#&gt; TCGA.IG.A5S3.01     2   0.000      0.832 0.0 1.00 0.00 0.00
#&gt; TCGA.LN.A5U6.01     3   0.441      0.763 0.0 0.00 0.70 0.30
#&gt; TCGA.LN.A9FQ.01     1   0.000      0.917 1.0 0.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     4   0.121      0.850 0.0 0.04 0.00 0.96
</code></pre>

<script>
$('#tab-node-013-get-classes-3-a').parent().next().next().hide();
$('#tab-node-013-get-classes-3-a').click(function(){
  $('#tab-node-013-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-013-get-classes-4'>
<p><a id='tab-node-013-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.S8.A6BW.01     4  0.2516      0.870 0.00 0.00 0.00 0.86 0.14
#&gt; TCGA.V5.A7RC.01     1  0.0609      0.987 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.KH.A6WC.01     2  0.2516      0.893 0.00 0.86 0.00 0.14 0.00
#&gt; TCGA.L7.A56G.01     2  0.1410      0.843 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.LN.A49K.01     5  0.3274      0.698 0.22 0.00 0.00 0.00 0.78
#&gt; TCGA.V5.A7RC.06     1  0.0609      0.987 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.IG.A4P3.01     4  0.1410      0.914 0.00 0.06 0.00 0.94 0.00
#&gt; TCGA.L5.A43H.01     5  0.3274      0.658 0.00 0.00 0.22 0.00 0.78
#&gt; TCGA.LN.A7HY.01     2  0.2516      0.893 0.00 0.86 0.00 0.14 0.00
#&gt; TCGA.LN.A49P.01     4  0.0000      0.954 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A49W.01     2  0.2516      0.893 0.00 0.86 0.00 0.14 0.00
#&gt; TCGA.LN.A7HW.01     5  0.4060      0.521 0.36 0.00 0.00 0.00 0.64
#&gt; TCGA.LN.A4MQ.01     1  0.0609      0.987 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.990 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     3  0.0000      0.990 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.0000      0.987 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1  0.0000      0.987 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     5  0.3274      0.658 0.00 0.00 0.22 0.00 0.78
#&gt; TCGA.IG.A97I.01     4  0.0000      0.954 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A5S3.01     2  0.1410      0.843 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.LN.A5U6.01     3  0.0609      0.979 0.00 0.00 0.98 0.00 0.02
#&gt; TCGA.LN.A9FQ.01     1  0.0000      0.987 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     4  0.0000      0.954 0.00 0.00 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-013-get-classes-4-a').parent().next().next().hide();
$('#tab-node-013-get-classes-4-a').click(function(){
  $('#tab-node-013-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-013-get-classes-5'>
<p><a id='tab-node-013-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.S8.A6BW.01     4  0.4552      0.626 0.00 0.00 0.00 0.64 0.06 0.30
#&gt; TCGA.V5.A7RC.01     1  0.0000      0.964 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.KH.A6WC.01     2  0.4680      0.826 0.00 0.68 0.00 0.12 0.00 0.20
#&gt; TCGA.L7.A56G.01     2  0.0000      0.744 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A49K.01     5  0.1556      0.783 0.08 0.00 0.00 0.00 0.92 0.00
#&gt; TCGA.V5.A7RC.06     1  0.0000      0.964 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4P3.01     4  0.2793      0.726 0.00 0.00 0.00 0.80 0.00 0.20
#&gt; TCGA.L5.A43H.01     5  0.1267      0.762 0.00 0.00 0.06 0.00 0.94 0.00
#&gt; TCGA.LN.A7HY.01     2  0.4680      0.826 0.00 0.68 0.00 0.12 0.00 0.20
#&gt; TCGA.LN.A49P.01     4  0.0937      0.854 0.00 0.00 0.00 0.96 0.00 0.04
#&gt; TCGA.LN.A49W.01     2  0.4680      0.826 0.00 0.68 0.00 0.12 0.00 0.20
#&gt; TCGA.LN.A7HW.01     5  0.3198      0.667 0.26 0.00 0.00 0.00 0.74 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.0000      0.964 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.888 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     3  0.0000      0.888 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.1267      0.964 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.VR.A8ER.01     1  0.1267      0.964 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.IG.A97H.01     5  0.4360      0.633 0.00 0.00 0.06 0.00 0.68 0.26
#&gt; TCGA.IG.A97I.01     4  0.0000      0.860 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     2  0.0000      0.744 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U6.01     3  0.3711      0.759 0.00 0.00 0.72 0.00 0.02 0.26
#&gt; TCGA.LN.A9FQ.01     1  0.1267      0.964 0.94 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.LN.A9FR.01     4  0.0000      0.860 0.00 0.00 0.00 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-013-get-classes-5-a').parent().next().next().hide();
$('#tab-node-013-get-classes-5-a').click(function(){
  $('#tab-node-013-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-013-get-classes-6'>
<p><a id='tab-node-013-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.S8.A6BW.01     4  0.4681      0.504 0.00 0.00 0.00 0.58 0.00 0.32 0.10
#&gt; TCGA.V5.A7RC.01     1  0.3139      0.808 0.70 0.00 0.00 0.00 0.00 0.30 0.00
#&gt; TCGA.KH.A6WC.01     2  0.1671      0.805 0.00 0.90 0.00 0.10 0.00 0.00 0.00
#&gt; TCGA.L7.A56G.01     2  0.3667      0.680 0.00 0.74 0.00 0.00 0.00 0.20 0.06
#&gt; TCGA.LN.A49K.01     5  0.0504      0.760 0.02 0.00 0.00 0.00 0.98 0.00 0.00
#&gt; TCGA.V5.A7RC.06     1  0.3139      0.808 0.70 0.00 0.00 0.00 0.00 0.30 0.00
#&gt; TCGA.IG.A4P3.01     4  0.3307      0.664 0.00 0.24 0.00 0.74 0.02 0.00 0.00
#&gt; TCGA.L5.A43H.01     5  0.1363      0.718 0.00 0.00 0.02 0.00 0.94 0.00 0.04
#&gt; TCGA.LN.A7HY.01     2  0.1671      0.805 0.00 0.90 0.00 0.10 0.00 0.00 0.00
#&gt; TCGA.LN.A49P.01     4  0.1664      0.802 0.00 0.06 0.00 0.92 0.02 0.00 0.00
#&gt; TCGA.LN.A49W.01     2  0.1671      0.805 0.00 0.90 0.00 0.10 0.00 0.00 0.00
#&gt; TCGA.LN.A7HW.01     5  0.3052      0.612 0.02 0.00 0.00 0.00 0.78 0.20 0.00
#&gt; TCGA.LN.A4MQ.01     1  0.3139      0.808 0.70 0.00 0.00 0.00 0.00 0.30 0.00
#&gt; TCGA.LN.A8I1.01     3  0.0000      0.774 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A5U5.01     3  0.0000      0.774 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.0000      0.809 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1  0.0000      0.809 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     7  0.3517      0.000 0.00 0.00 0.02 0.00 0.28 0.00 0.70
#&gt; TCGA.IG.A97I.01     4  0.0000      0.810 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A5S3.01     2  0.3519      0.680 0.00 0.74 0.00 0.00 0.00 0.22 0.04
#&gt; TCGA.LN.A5U6.01     3  0.5073      0.436 0.00 0.00 0.54 0.00 0.00 0.16 0.30
#&gt; TCGA.LN.A9FQ.01     1  0.0000      0.809 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     4  0.0000      0.810 0.00 0.00 0.00 1.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-013-get-classes-6-a').parent().next().next().hide();
$('#tab-node-013-get-classes-6-a').click(function(){
  $('#tab-node-013-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-013-get-classes-7'>
<p><a id='tab-node-013-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.S8.A6BW.01     6  0.0471      0.000 0.00 0.00 0.00 0.02 0.00 0.98 0.00 0.00
#&gt; TCGA.V5.A7RC.01     1  0.4333      0.749 0.62 0.26 0.00 0.00 0.00 0.00 0.00 0.12
#&gt; TCGA.KH.A6WC.01     2  0.4004      0.265 0.00 0.50 0.00 0.04 0.00 0.00 0.46 0.00
#&gt; TCGA.L7.A56G.01     7  0.1341      0.931 0.00 0.00 0.00 0.00 0.00 0.00 0.92 0.08
#&gt; TCGA.LN.A49K.01     5  0.6255      0.658 0.00 0.14 0.00 0.32 0.38 0.00 0.00 0.16
#&gt; TCGA.V5.A7RC.06     1  0.4333      0.749 0.62 0.26 0.00 0.00 0.00 0.00 0.00 0.12
#&gt; TCGA.IG.A4P3.01     2  0.5101     -0.462 0.00 0.54 0.00 0.28 0.00 0.16 0.00 0.02
#&gt; TCGA.L5.A43H.01     5  0.6053      0.663 0.00 0.14 0.00 0.32 0.42 0.00 0.00 0.12
#&gt; TCGA.LN.A7HY.01     2  0.3992      0.267 0.00 0.52 0.00 0.04 0.00 0.00 0.44 0.00
#&gt; TCGA.LN.A49P.01     4  0.5560      0.533 0.00 0.36 0.00 0.38 0.00 0.24 0.00 0.02
#&gt; TCGA.LN.A49W.01     2  0.4004      0.265 0.00 0.50 0.00 0.04 0.00 0.00 0.46 0.00
#&gt; TCGA.LN.A7HW.01     2  0.7022     -0.551 0.04 0.36 0.00 0.18 0.20 0.00 0.00 0.22
#&gt; TCGA.LN.A4MQ.01     1  0.4333      0.749 0.62 0.26 0.00 0.00 0.00 0.00 0.00 0.12
#&gt; TCGA.LN.A8I1.01     3  0.0471      0.975 0.00 0.00 0.98 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.LN.A5U5.01     3  0.0000      0.975 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EZ.01     1  0.0000      0.746 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ER.01     1  0.0000      0.746 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A97H.01     5  0.0808      0.200 0.00 0.00 0.00 0.00 0.96 0.00 0.00 0.04
#&gt; TCGA.IG.A97I.01     4  0.3880      0.755 0.00 0.08 0.00 0.68 0.00 0.24 0.00 0.00
#&gt; TCGA.IG.A5S3.01     7  0.0000      0.931 0.00 0.00 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A5U6.01     8  0.3808      0.000 0.00 0.00 0.34 0.00 0.04 0.00 0.00 0.62
#&gt; TCGA.LN.A9FQ.01     1  0.0000      0.746 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A9FR.01     4  0.3880      0.755 0.00 0.08 0.00 0.68 0.00 0.24 0.00 0.00
</code></pre>

<script>
$('#tab-node-013-get-classes-7-a').parent().next().next().hide();
$('#tab-node-013-get-classes-7-a').click(function(){
  $('#tab-node-013-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-013-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-013-consensus-heatmap'>
<ul>
<li><a href='#tab-node-013-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-013-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-013-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-013-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-013-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-013-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-013-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-013-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-013-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-013-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-013-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-013-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-013-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-013-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-013-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-013-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-013-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-013-membership-heatmap'>
<ul>
<li><a href='#tab-node-013-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-013-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-013-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-013-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-013-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-013-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-013-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-013-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-1-1.png" alt="plot of chunk tab-node-013-membership-heatmap-1"/></p>

</div>
<div id='tab-node-013-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-2-1.png" alt="plot of chunk tab-node-013-membership-heatmap-2"/></p>

</div>
<div id='tab-node-013-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-3-1.png" alt="plot of chunk tab-node-013-membership-heatmap-3"/></p>

</div>
<div id='tab-node-013-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-4-1.png" alt="plot of chunk tab-node-013-membership-heatmap-4"/></p>

</div>
<div id='tab-node-013-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-5-1.png" alt="plot of chunk tab-node-013-membership-heatmap-5"/></p>

</div>
<div id='tab-node-013-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-6-1.png" alt="plot of chunk tab-node-013-membership-heatmap-6"/></p>

</div>
<div id='tab-node-013-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-013-membership-heatmap-7-1.png" alt="plot of chunk tab-node-013-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-013-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-013-get-signatures'>
<ul>
<li><a href='#tab-node-013-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-013-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-013-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-013-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-013-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-013-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-013-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-013-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-1-1.png" alt="plot of chunk tab-node-013-get-signatures-1"/></p>

</div>
<div id='tab-node-013-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-2-1.png" alt="plot of chunk tab-node-013-get-signatures-2"/></p>

</div>
<div id='tab-node-013-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-3-1.png" alt="plot of chunk tab-node-013-get-signatures-3"/></p>

</div>
<div id='tab-node-013-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-4-1.png" alt="plot of chunk tab-node-013-get-signatures-4"/></p>

</div>
<div id='tab-node-013-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-5-1.png" alt="plot of chunk tab-node-013-get-signatures-5"/></p>

</div>
<div id='tab-node-013-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-6-1.png" alt="plot of chunk tab-node-013-get-signatures-6"/></p>

</div>
<div id='tab-node-013-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-013-get-signatures-7-1.png" alt="plot of chunk tab-node-013-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-013-signature_compare](figure_cola/node-013-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-013-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-013-dimension-reduction'>
<ul>
<li><a href='#tab-node-013-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-013-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-013-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-013-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-013-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-013-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-013-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-013-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-1-1.png" alt="plot of chunk tab-node-013-dimension-reduction-1"/></p>

</div>
<div id='tab-node-013-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-2-1.png" alt="plot of chunk tab-node-013-dimension-reduction-2"/></p>

</div>
<div id='tab-node-013-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-3-1.png" alt="plot of chunk tab-node-013-dimension-reduction-3"/></p>

</div>
<div id='tab-node-013-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-4-1.png" alt="plot of chunk tab-node-013-dimension-reduction-4"/></p>

</div>
<div id='tab-node-013-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-5-1.png" alt="plot of chunk tab-node-013-dimension-reduction-5"/></p>

</div>
<div id='tab-node-013-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-6-1.png" alt="plot of chunk tab-node-013-dimension-reduction-6"/></p>

</div>
<div id='tab-node-013-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-013-dimension-reduction-7-1.png" alt="plot of chunk tab-node-013-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-013-collect-classes](figure_cola/node-013-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node02


Parent node: [Node0](#Node0).
Child nodes: 
                [Node011](#Node011)
        ,
                [Node012](#Node012)
        ,
                [Node013](#Node013)
        ,
                [Node021](#Node021)
        ,
                [Node022](#Node022)
        ,
                [Node023](#Node023)
        ,
                Node031-leaf
        ,
                Node032-leaf
        ,
                Node033-leaf
        ,
                Node034-leaf
        ,
                Node035-leaf
        ,
                Node041-leaf
        ,
                Node042-leaf
        ,
                Node043-leaf
        ,
                Node051-leaf
        ,
                Node052-leaf
        ,
                Node053-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["02"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 75 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'skmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-02-collect-plots](figure_cola/node-02-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-02-select-partition-number](figure_cola/node-02-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           0.999       0.999         0.3256 0.676   0.676
#> 3 3 0.957           0.955       0.982         0.6893 0.768   0.657
#> 4 4 0.775           0.857       0.929         0.0989 0.933   0.852
#> 5 5 0.803           0.733       0.849         0.0518 0.981   0.953
#> 6 6 0.739           0.615       0.830         0.0349 0.926   0.823
#> 7 7 0.736           0.602       0.831         0.0289 0.899   0.747
#> 8 8 0.664           0.589       0.807         0.0361 0.945   0.838
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-02-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-02-get-classes'>
<ul>
<li><a href='#tab-node-02-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-02-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-02-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-02-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-02-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-02-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-02-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-02-get-classes-1'>
<p><a id='tab-node-02-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2
#&gt; TCGA.JY.A6FB.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.Q9.A6FW.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.S8.A6BV.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OI.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A6DN.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OG.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A43E.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.X8.AAAR.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4ON.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.V5.AASW.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A43I.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OF.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OJ.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OH.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A6L4.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L7.A6VZ.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OO.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OP.01     2   0.242      0.958 0.04 0.96
#&gt; TCGA.L5.A43C.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OE.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A6KZ.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OR.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.V5.A7RE.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.V5.A7RE.11     2   0.000      0.999 0.00 1.00
#&gt; TCGA.V5.A7RB.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A6DQ.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.IG.A4QS.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A88Y.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A88V.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.M9.A5M8.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OW.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GK.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NW.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NH.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GR.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NV.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A6XG.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NN.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A8NS.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.JY.A938.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A8WG.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.R6.A6L6.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.V5.AASX.11     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A893.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NU.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.R6.A6XQ.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OT.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.ZR.A9CJ.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.R6.A8W8.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.JY.A93E.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GI.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GL.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NM.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.JY.A93D.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OX.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A6Y2.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.2H.A9GF.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GO.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A8NR.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A4OU.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.JY.A93C.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.V5.AASX.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NT.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.R6.A8WC.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.VR.AA4D.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GM.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NG.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.IC.A6RE.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.RE.A7BO.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NJ.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.JY.A939.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.JY.A6F8.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.VR.A8EQ.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.L5.A8NL.01     2   0.000      0.999 0.00 1.00
#&gt; TCGA.2H.A9GH.01     2   0.000      0.999 0.00 1.00
</code></pre>

<script>
$('#tab-node-02-get-classes-1-a').parent().next().next().hide();
$('#tab-node-02-get-classes-1-a').click(function(){
  $('#tab-node-02-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02-get-classes-2'>
<p><a id='tab-node-02-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.JY.A6FB.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.Q9.A6FW.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.S8.A6BV.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A43E.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A43I.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.L5.A4OF.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.R6.A6L4.01     1  0.0892      0.970 0.98 0.02 0.00
#&gt; TCGA.L7.A6VZ.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4OO.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.L5.A43C.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A6KZ.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.V5.A7RE.01     3  0.4555      0.757 0.00 0.20 0.80
#&gt; TCGA.V5.A7RE.11     3  0.4555      0.757 0.00 0.20 0.80
#&gt; TCGA.V5.A7RB.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.IG.A4QS.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.L5.A88Y.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.M9.A5M8.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NH.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.2H.A9GR.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A6XG.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.L5.A8NN.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.JY.A938.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A8WG.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.R6.A6L6.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.V5.AASX.11     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NU.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.R6.A6XQ.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A4OT.01     2  0.2537      0.899 0.00 0.92 0.08
#&gt; TCGA.ZR.A9CJ.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.R6.A8W8.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.JY.A93E.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.JY.A93D.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A4OX.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A6Y2.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     3  0.4555      0.753 0.00 0.20 0.80
#&gt; TCGA.2H.A9GO.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.VR.AA4D.01     3  0.5560      0.635 0.00 0.30 0.70
#&gt; TCGA.2H.A9GM.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.L5.A8NG.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.IC.A6RE.01     3  0.0000      0.899 0.00 0.00 1.00
#&gt; TCGA.RE.A7BO.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.JY.A939.01     1  0.0000      0.998 1.00 0.00 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0000      0.989 0.00 1.00 0.00
#&gt; TCGA.2H.A9GH.01     2  0.5948      0.362 0.00 0.64 0.36
</code></pre>

<script>
$('#tab-node-02-get-classes-2-a').parent().next().next().hide();
$('#tab-node-02-get-classes-2-a').click(function(){
  $('#tab-node-02-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02-get-classes-3'>
<p><a id='tab-node-02-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.JY.A6FB.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     4  0.2921      0.714 0.00 0.14 0.00 0.86
#&gt; TCGA.S8.A6BV.01     4  0.3037      0.757 0.00 0.10 0.02 0.88
#&gt; TCGA.L5.A4OI.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.4134      0.676 0.00 0.74 0.00 0.26
#&gt; TCGA.L5.A43E.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     3  0.2011      0.744 0.00 0.00 0.92 0.08
#&gt; TCGA.L5.A4OF.01     4  0.3172      0.808 0.16 0.00 0.00 0.84
#&gt; TCGA.L5.A4OJ.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.1637      0.749 0.00 0.00 0.94 0.06
#&gt; TCGA.R6.A6L4.01     4  0.2647      0.817 0.12 0.00 0.00 0.88
#&gt; TCGA.L7.A6VZ.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     1  0.4713      0.328 0.64 0.00 0.00 0.36
#&gt; TCGA.L5.A4OP.01     4  0.2345      0.763 0.00 0.00 0.10 0.90
#&gt; TCGA.L5.A43C.01     4  0.3172      0.809 0.16 0.00 0.00 0.84
#&gt; TCGA.L5.A4OE.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     1  0.0000      0.943 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     3  0.0707      0.757 0.00 0.00 0.98 0.02
#&gt; TCGA.V5.A7RE.01     3  0.5428      0.427 0.00 0.38 0.60 0.02
#&gt; TCGA.V5.A7RE.11     3  0.5428      0.427 0.00 0.38 0.60 0.02
#&gt; TCGA.V5.A7RB.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     3  0.3801      0.631 0.00 0.00 0.78 0.22
#&gt; TCGA.L5.A88Y.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.M9.A5M8.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.2921      0.839 0.00 0.86 0.00 0.14
#&gt; TCGA.L5.A8NW.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     3  0.1637      0.749 0.00 0.00 0.94 0.06
#&gt; TCGA.2H.A9GR.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     3  0.1211      0.758 0.00 0.00 0.96 0.04
#&gt; TCGA.L5.A8NN.01     1  0.0000      0.943 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A938.01     2  0.3400      0.794 0.00 0.82 0.00 0.18
#&gt; TCGA.R6.A8WG.01     1  0.0000      0.943 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6L6.01     1  0.0000      0.943 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.11     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NU.01     1  0.0707      0.938 0.98 0.00 0.00 0.02
#&gt; TCGA.R6.A6XQ.01     1  0.0707      0.932 0.98 0.00 0.00 0.02
#&gt; TCGA.L5.A4OT.01     2  0.4841      0.734 0.00 0.78 0.14 0.08
#&gt; TCGA.ZR.A9CJ.01     1  0.0707      0.938 0.98 0.00 0.00 0.02
#&gt; TCGA.R6.A8W8.01     3  0.1211      0.758 0.00 0.00 0.96 0.04
#&gt; TCGA.JY.A93E.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     4  0.4790      0.466 0.38 0.00 0.00 0.62
#&gt; TCGA.L5.A4OX.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     4  0.3400      0.793 0.18 0.00 0.00 0.82
#&gt; TCGA.2H.A9GF.01     3  0.7654      0.294 0.00 0.34 0.44 0.22
#&gt; TCGA.2H.A9GO.01     1  0.0000      0.943 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.2647      0.859 0.00 0.88 0.00 0.12
#&gt; TCGA.JY.A93C.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.AA4D.01     4  0.2011      0.776 0.00 0.00 0.08 0.92
#&gt; TCGA.2H.A9GM.01     3  0.1637      0.749 0.00 0.00 0.94 0.06
#&gt; TCGA.L5.A8NG.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.IC.A6RE.01     3  0.1637      0.750 0.00 0.00 0.94 0.06
#&gt; TCGA.RE.A7BO.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A939.01     1  0.0707      0.938 0.98 0.00 0.00 0.02
#&gt; TCGA.JY.A6F8.01     2  0.0000      0.963 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.3172      0.817 0.00 0.84 0.00 0.16
#&gt; TCGA.L5.A8NL.01     2  0.2921      0.839 0.00 0.86 0.00 0.14
#&gt; TCGA.2H.A9GH.01     2  0.4079      0.717 0.00 0.80 0.18 0.02
</code></pre>

<script>
$('#tab-node-02-get-classes-3-a').parent().next().next().hide();
$('#tab-node-02-get-classes-3-a').click(function(){
  $('#tab-node-02-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02-get-classes-4'>
<p><a id='tab-node-02-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     5  0.1043     0.6830 0.00 0.04 0.00 0.00 0.96
#&gt; TCGA.S8.A6BV.01     5  0.2438     0.6577 0.00 0.06 0.00 0.04 0.90
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     5  0.4302    -0.0985 0.00 0.48 0.00 0.00 0.52
#&gt; TCGA.L5.A43E.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     3  0.3291     0.5818 0.00 0.00 0.84 0.12 0.04
#&gt; TCGA.L5.A4OF.01     5  0.1648     0.6800 0.04 0.00 0.00 0.02 0.94
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.4302     0.5378 0.00 0.00 0.52 0.48 0.00
#&gt; TCGA.R6.A6L4.01     5  0.0609     0.6849 0.02 0.00 0.00 0.00 0.98
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     1  0.4126     0.4785 0.62 0.00 0.00 0.00 0.38
#&gt; TCGA.L5.A4OP.01     5  0.6244     0.2984 0.00 0.00 0.26 0.20 0.54
#&gt; TCGA.L5.A43C.01     5  0.1410     0.6752 0.06 0.00 0.00 0.00 0.94
#&gt; TCGA.L5.A4OE.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     1  0.0609     0.8819 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A4OR.01     3  0.2929     0.6214 0.00 0.00 0.82 0.18 0.00
#&gt; TCGA.V5.A7RE.01     3  0.5447     0.2337 0.00 0.44 0.50 0.06 0.00
#&gt; TCGA.V5.A7RE.11     3  0.5394     0.3132 0.00 0.40 0.54 0.06 0.00
#&gt; TCGA.V5.A7RB.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     3  0.4728     0.4684 0.00 0.00 0.70 0.24 0.06
#&gt; TCGA.L5.A88Y.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88V.01     2  0.0609     0.9097 0.00 0.98 0.00 0.00 0.02
#&gt; TCGA.M9.A5M8.01     2  0.1410     0.8765 0.00 0.94 0.00 0.00 0.06
#&gt; TCGA.L5.A4OW.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.4182     0.3692 0.00 0.60 0.00 0.00 0.40
#&gt; TCGA.L5.A8NW.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     3  0.4262     0.5505 0.00 0.00 0.56 0.44 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     3  0.1732     0.6083 0.00 0.00 0.92 0.08 0.00
#&gt; TCGA.L5.A8NN.01     1  0.1732     0.8687 0.92 0.00 0.00 0.08 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A938.01     2  0.4227     0.3177 0.00 0.58 0.00 0.00 0.42
#&gt; TCGA.R6.A8WG.01     1  0.2012     0.8714 0.92 0.00 0.00 0.06 0.02
#&gt; TCGA.R6.A6L6.01     1  0.1216     0.8847 0.96 0.00 0.00 0.02 0.02
#&gt; TCGA.V5.AASX.11     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NU.01     1  0.1410     0.8790 0.94 0.00 0.00 0.00 0.06
#&gt; TCGA.R6.A6XQ.01     1  0.5759     0.6703 0.62 0.00 0.00 0.18 0.20
#&gt; TCGA.L5.A4OT.01     2  0.5798     0.4421 0.00 0.62 0.08 0.02 0.28
#&gt; TCGA.ZR.A9CJ.01     1  0.2012     0.8773 0.92 0.00 0.00 0.02 0.06
#&gt; TCGA.R6.A8W8.01     3  0.2516     0.6215 0.00 0.00 0.86 0.14 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     5  0.4262    -0.0873 0.44 0.00 0.00 0.00 0.56
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     5  0.2020     0.6447 0.10 0.00 0.00 0.00 0.90
#&gt; TCGA.2H.A9GF.01     3  0.7598     0.2794 0.00 0.26 0.44 0.24 0.06
#&gt; TCGA.2H.A9GO.01     1  0.0609     0.8819 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.3983     0.4990 0.00 0.66 0.00 0.00 0.34
#&gt; TCGA.JY.A93C.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4D.01     5  0.5888     0.3594 0.00 0.00 0.28 0.14 0.58
#&gt; TCGA.2H.A9GM.01     3  0.4302     0.5327 0.00 0.00 0.52 0.48 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RE.01     3  0.3037     0.6165 0.00 0.00 0.86 0.10 0.04
#&gt; TCGA.RE.A7BO.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     1  0.1410     0.8790 0.94 0.00 0.00 0.00 0.06
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.9276 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.4060     0.4608 0.00 0.64 0.00 0.00 0.36
#&gt; TCGA.L5.A8NL.01     2  0.4060     0.4596 0.00 0.64 0.00 0.00 0.36
#&gt; TCGA.2H.A9GH.01     2  0.4644     0.4660 0.00 0.68 0.28 0.04 0.00
</code></pre>

<script>
$('#tab-node-02-get-classes-4-a').parent().next().next().hide();
$('#tab-node-02-get-classes-4-a').click(function(){
  $('#tab-node-02-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02-get-classes-5'>
<p><a id='tab-node-02-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     5  0.2094     0.4820 0.00 0.08 0.00 0.02 0.90 0.00
#&gt; TCGA.S8.A6BV.01     5  0.4066     0.4067 0.00 0.08 0.00 0.12 0.78 0.02
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     5  0.4609     0.1473 0.00 0.42 0.00 0.00 0.54 0.04
#&gt; TCGA.L5.A43E.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     4  0.5095    -0.0869 0.00 0.00 0.42 0.50 0.00 0.08
#&gt; TCGA.L5.A4OF.01     5  0.2474     0.4806 0.08 0.00 0.00 0.00 0.88 0.04
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.3846     0.5938 0.00 0.00 0.80 0.10 0.02 0.08
#&gt; TCGA.R6.A6L4.01     5  0.2403     0.4843 0.04 0.00 0.00 0.04 0.90 0.02
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     1  0.4326     0.6469 0.68 0.00 0.00 0.02 0.28 0.02
#&gt; TCGA.L5.A4OP.01     4  0.4552     0.3670 0.00 0.00 0.00 0.64 0.30 0.06
#&gt; TCGA.L5.A43C.01     5  0.1480     0.4965 0.04 0.00 0.02 0.00 0.94 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0937     0.8637 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.R6.A6KZ.01     1  0.1092     0.8426 0.96 0.00 0.00 0.02 0.00 0.02
#&gt; TCGA.L5.A4OR.01     3  0.5007     0.4743 0.00 0.00 0.66 0.24 0.02 0.08
#&gt; TCGA.V5.A7RE.01     2  0.6920    -0.2513 0.00 0.40 0.14 0.36 0.00 0.10
#&gt; TCGA.V5.A7RE.11     2  0.6639    -0.1446 0.00 0.44 0.10 0.36 0.00 0.10
#&gt; TCGA.V5.A7RB.01     2  0.1865     0.8407 0.00 0.92 0.00 0.00 0.04 0.04
#&gt; TCGA.R6.A6DQ.01     2  0.1480     0.8533 0.00 0.94 0.00 0.00 0.02 0.04
#&gt; TCGA.IG.A4QS.01     4  0.3873     0.3059 0.00 0.00 0.16 0.78 0.04 0.02
#&gt; TCGA.L5.A88Y.01     2  0.3103     0.7983 0.00 0.86 0.06 0.00 0.04 0.04
#&gt; TCGA.L5.A88V.01     2  0.0547     0.8670 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.M9.A5M8.01     2  0.2094     0.8189 0.00 0.90 0.00 0.00 0.08 0.02
#&gt; TCGA.L5.A4OW.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.4632     0.0864 0.00 0.52 0.00 0.00 0.44 0.04
#&gt; TCGA.L5.A8NW.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     3  0.1267     0.6802 0.00 0.00 0.94 0.06 0.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0937     0.8637 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A8NV.01     2  0.1865     0.8407 0.00 0.92 0.00 0.00 0.04 0.04
#&gt; TCGA.R6.A6XG.01     4  0.6735    -0.0644 0.00 0.04 0.26 0.40 0.00 0.30
#&gt; TCGA.L5.A8NN.01     1  0.2094     0.8193 0.90 0.00 0.02 0.00 0.00 0.08
#&gt; TCGA.L5.A8NS.01     2  0.0547     0.8701 0.00 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.JY.A938.01     2  0.4646     0.0112 0.00 0.50 0.00 0.00 0.46 0.04
#&gt; TCGA.R6.A8WG.01     1  0.4265     0.7643 0.76 0.00 0.02 0.00 0.08 0.14
#&gt; TCGA.R6.A6L6.01     1  0.0937     0.8552 0.96 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.V5.AASX.11     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NU.01     1  0.0937     0.8552 0.96 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.R6.A6XQ.01     1  0.5749     0.4528 0.46 0.00 0.00 0.02 0.10 0.42
#&gt; TCGA.L5.A4OT.01     2  0.6875     0.3284 0.00 0.56 0.12 0.08 0.20 0.04
#&gt; TCGA.ZR.A9CJ.01     1  0.2581     0.8306 0.86 0.00 0.00 0.00 0.12 0.02
#&gt; TCGA.R6.A8W8.01     3  0.5954     0.3125 0.00 0.00 0.50 0.34 0.02 0.14
#&gt; TCGA.JY.A93E.01     2  0.0937     0.8637 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0937     0.8637 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.JY.A93D.01     5  0.4632    -0.2764 0.44 0.00 0.00 0.00 0.52 0.04
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     5  0.3873     0.4124 0.16 0.00 0.00 0.02 0.78 0.04
#&gt; TCGA.2H.A9GF.01     4  0.7655     0.2404 0.00 0.16 0.08 0.50 0.12 0.14
#&gt; TCGA.2H.A9GO.01     1  0.0547     0.8454 0.98 0.00 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A8NR.01     2  0.1267     0.8375 0.00 0.94 0.06 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.4534     0.2785 0.00 0.58 0.00 0.00 0.38 0.04
#&gt; TCGA.JY.A93C.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0547     0.8701 0.00 0.98 0.00 0.00 0.00 0.02
#&gt; TCGA.R6.A8WC.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4D.01     4  0.4282     0.2999 0.00 0.00 0.00 0.56 0.42 0.02
#&gt; TCGA.2H.A9GM.01     3  0.0000     0.6661 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.1480     0.8533 0.00 0.94 0.00 0.00 0.02 0.04
#&gt; TCGA.IC.A6RE.01     4  0.6184     0.0170 0.00 0.00 0.38 0.46 0.04 0.12
#&gt; TCGA.RE.A7BO.01     2  0.1480     0.8533 0.00 0.94 0.00 0.00 0.02 0.04
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     1  0.1267     0.8520 0.94 0.00 0.00 0.00 0.06 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.8754 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     5  0.4646     0.0111 0.00 0.46 0.00 0.00 0.50 0.04
#&gt; TCGA.L5.A8NL.01     2  0.4576     0.2204 0.00 0.56 0.00 0.00 0.40 0.04
#&gt; TCGA.2H.A9GH.01     2  0.5896     0.2146 0.00 0.54 0.10 0.32 0.00 0.04
</code></pre>

<script>
$('#tab-node-02-get-classes-5-a').parent().next().next().hide();
$('#tab-node-02-get-classes-5-a').click(function(){
  $('#tab-node-02-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02-get-classes-6'>
<p><a id='tab-node-02-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     5  0.2163     0.4019 0.00 0.10 0.00 0.00 0.88 0.00 0.02
#&gt; TCGA.S8.A6BV.01     5  0.3149     0.3311 0.00 0.06 0.00 0.06 0.84 0.00 0.04
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     5  0.4354     0.5061 0.00 0.26 0.02 0.02 0.68 0.02 0.00
#&gt; TCGA.L5.A43E.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     4  0.3722     0.2308 0.00 0.02 0.18 0.76 0.00 0.00 0.04
#&gt; TCGA.L5.A4OF.01     5  0.2159     0.1715 0.06 0.00 0.00 0.02 0.90 0.02 0.00
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.1718     0.6576 0.00 0.00 0.92 0.00 0.00 0.04 0.04
#&gt; TCGA.R6.A6L4.01     5  0.2769     0.1930 0.02 0.00 0.00 0.00 0.86 0.08 0.04
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     1  0.3637     0.6148 0.72 0.00 0.00 0.00 0.24 0.04 0.00
#&gt; TCGA.L5.A4OP.01     7  0.6166     0.0000 0.00 0.00 0.00 0.26 0.28 0.04 0.42
#&gt; TCGA.L5.A43C.01     5  0.0504     0.2567 0.00 0.00 0.02 0.00 0.98 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.1006     0.9006 0.00 0.96 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.R6.A6KZ.01     1  0.1166     0.7400 0.94 0.00 0.00 0.00 0.00 0.06 0.00
#&gt; TCGA.L5.A4OR.01     3  0.5480     0.2918 0.00 0.02 0.52 0.36 0.02 0.00 0.08
#&gt; TCGA.V5.A7RE.01     4  0.4388     0.3181 0.00 0.30 0.02 0.64 0.00 0.00 0.04
#&gt; TCGA.V5.A7RE.11     4  0.4107     0.3455 0.00 0.24 0.02 0.70 0.00 0.00 0.04
#&gt; TCGA.V5.A7RB.01     2  0.1363     0.8860 0.00 0.94 0.00 0.00 0.04 0.02 0.00
#&gt; TCGA.R6.A6DQ.01     2  0.1664     0.8659 0.00 0.92 0.00 0.00 0.06 0.02 0.00
#&gt; TCGA.IG.A4QS.01     4  0.3530    -0.0260 0.00 0.00 0.02 0.76 0.02 0.00 0.20
#&gt; TCGA.L5.A88Y.01     2  0.3061     0.7776 0.00 0.84 0.08 0.00 0.06 0.02 0.00
#&gt; TCGA.L5.A88V.01     2  0.1006     0.8934 0.00 0.96 0.00 0.02 0.00 0.00 0.02
#&gt; TCGA.M9.A5M8.01     2  0.3661     0.5783 0.00 0.74 0.00 0.00 0.22 0.02 0.02
#&gt; TCGA.L5.A4OW.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     5  0.4356     0.4879 0.00 0.40 0.00 0.02 0.56 0.02 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     3  0.3208     0.7095 0.00 0.00 0.82 0.12 0.02 0.00 0.04
#&gt; TCGA.2H.A9GR.01     2  0.1006     0.9006 0.00 0.96 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.L5.A8NV.01     2  0.1363     0.8860 0.00 0.94 0.00 0.00 0.04 0.02 0.00
#&gt; TCGA.R6.A6XG.01     4  0.6550     0.0972 0.00 0.02 0.16 0.40 0.00 0.06 0.36
#&gt; TCGA.L5.A8NN.01     1  0.3228     0.6389 0.80 0.00 0.00 0.00 0.02 0.16 0.02
#&gt; TCGA.L5.A8NS.01     2  0.0504     0.9117 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.JY.A938.01     5  0.4720     0.5064 0.00 0.36 0.00 0.02 0.58 0.02 0.02
#&gt; TCGA.R6.A8WG.01     1  0.4145     0.6399 0.74 0.00 0.00 0.00 0.14 0.10 0.02
#&gt; TCGA.R6.A6L6.01     1  0.1166     0.7790 0.94 0.00 0.00 0.00 0.06 0.00 0.00
#&gt; TCGA.V5.AASX.11     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NU.01     1  0.1433     0.7781 0.92 0.00 0.00 0.00 0.08 0.00 0.00
#&gt; TCGA.R6.A6XQ.01     6  0.2945     0.0000 0.26 0.00 0.00 0.00 0.00 0.74 0.00
#&gt; TCGA.L5.A4OT.01     2  0.6738    -0.2876 0.00 0.44 0.12 0.08 0.32 0.00 0.04
#&gt; TCGA.ZR.A9CJ.01     1  0.2376     0.7660 0.86 0.00 0.00 0.00 0.12 0.02 0.00
#&gt; TCGA.R6.A8W8.01     4  0.6101     0.1012 0.00 0.02 0.20 0.48 0.00 0.02 0.28
#&gt; TCGA.JY.A93E.01     2  0.1006     0.9006 0.00 0.96 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.1006     0.9006 0.00 0.96 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.JY.A93D.01     1  0.3815     0.4576 0.62 0.00 0.00 0.00 0.36 0.02 0.00
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     5  0.4854    -0.1613 0.18 0.00 0.00 0.04 0.70 0.04 0.04
#&gt; TCGA.2H.A9GF.01     4  0.7118     0.0270 0.00 0.20 0.04 0.36 0.08 0.00 0.32
#&gt; TCGA.2H.A9GO.01     1  0.0863     0.7432 0.96 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0504     0.9075 0.00 0.98 0.02 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     2  0.4425    -0.3425 0.00 0.48 0.00 0.02 0.48 0.02 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0504     0.9117 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.R6.A8WC.01     2  0.0504     0.9044 0.00 0.98 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.VR.AA4D.01     4  0.5546    -0.4790 0.00 0.00 0.00 0.42 0.32 0.00 0.26
#&gt; TCGA.2H.A9GM.01     3  0.2509     0.7231 0.00 0.00 0.88 0.04 0.02 0.00 0.06
#&gt; TCGA.L5.A8NG.01     2  0.1006     0.9006 0.00 0.96 0.00 0.00 0.02 0.02 0.00
#&gt; TCGA.IC.A6RE.01     4  0.6134     0.1096 0.00 0.02 0.26 0.54 0.10 0.00 0.08
#&gt; TCGA.RE.A7BO.01     2  0.0504     0.9117 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     1  0.1433     0.7781 0.92 0.00 0.00 0.00 0.08 0.00 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.9188 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     5  0.5169     0.5003 0.00 0.32 0.06 0.02 0.58 0.02 0.00
#&gt; TCGA.L5.A8NL.01     5  0.4408     0.3944 0.00 0.44 0.00 0.02 0.52 0.02 0.00
#&gt; TCGA.2H.A9GH.01     2  0.3994    -0.1523 0.00 0.50 0.00 0.48 0.00 0.00 0.02
</code></pre>

<script>
$('#tab-node-02-get-classes-6-a').parent().next().next().hide();
$('#tab-node-02-get-classes-6-a').click(function(){
  $('#tab-node-02-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02-get-classes-7'>
<p><a id='tab-node-02-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.JY.A6FB.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     5  0.1091     0.3932 0.00 0.00 0.00 0.00 0.94 0.00 0.06 0.00
#&gt; TCGA.S8.A6BV.01     5  0.0471     0.4037 0.00 0.00 0.00 0.02 0.98 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OG.01     5  0.4650     0.4617 0.00 0.20 0.06 0.00 0.66 0.00 0.00 0.08
#&gt; TCGA.L5.A43E.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43I.01     4  0.5374     0.1600 0.00 0.02 0.10 0.66 0.02 0.00 0.12 0.08
#&gt; TCGA.L5.A4OF.01     5  0.3986     0.2718 0.14 0.00 0.00 0.00 0.74 0.04 0.08 0.00
#&gt; TCGA.L5.A4OJ.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.4615     0.5387 0.00 0.00 0.68 0.08 0.00 0.00 0.16 0.08
#&gt; TCGA.R6.A6L4.01     5  0.2399     0.3483 0.04 0.00 0.00 0.00 0.88 0.04 0.04 0.00
#&gt; TCGA.L7.A6VZ.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     1  0.4355     0.5303 0.72 0.00 0.00 0.00 0.16 0.02 0.06 0.04
#&gt; TCGA.L5.A4OP.01     5  0.7362    -0.3806 0.00 0.00 0.00 0.24 0.30 0.10 0.12 0.24
#&gt; TCGA.L5.A43C.01     5  0.3847     0.3478 0.10 0.00 0.06 0.00 0.78 0.00 0.04 0.02
#&gt; TCGA.L5.A4OE.01     2  0.1607     0.8850 0.00 0.92 0.00 0.00 0.04 0.00 0.00 0.04
#&gt; TCGA.R6.A6KZ.01     1  0.3970     0.5553 0.68 0.00 0.00 0.00 0.00 0.10 0.00 0.22
#&gt; TCGA.L5.A4OR.01     4  0.5080    -0.1986 0.00 0.00 0.40 0.48 0.00 0.00 0.06 0.06
#&gt; TCGA.V5.A7RE.01     4  0.3735     0.1558 0.00 0.22 0.00 0.72 0.00 0.00 0.02 0.04
#&gt; TCGA.V5.A7RE.11     4  0.4057     0.1592 0.00 0.20 0.02 0.72 0.00 0.00 0.02 0.04
#&gt; TCGA.V5.A7RB.01     2  0.2623     0.8185 0.00 0.84 0.00 0.00 0.10 0.00 0.00 0.06
#&gt; TCGA.R6.A6DQ.01     2  0.2994     0.7646 0.00 0.80 0.00 0.00 0.14 0.00 0.00 0.06
#&gt; TCGA.IG.A4QS.01     4  0.3735     0.1065 0.00 0.00 0.00 0.72 0.02 0.04 0.00 0.22
#&gt; TCGA.L5.A88Y.01     2  0.4808     0.5559 0.00 0.66 0.10 0.00 0.16 0.00 0.00 0.08
#&gt; TCGA.L5.A88V.01     2  0.0471     0.9055 0.00 0.98 0.00 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.M9.A5M8.01     2  0.3746     0.4475 0.00 0.64 0.00 0.00 0.32 0.00 0.00 0.04
#&gt; TCGA.L5.A4OW.01     2  0.0471     0.9107 0.00 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.2H.A9GK.01     5  0.3991     0.4541 0.00 0.32 0.00 0.00 0.62 0.00 0.00 0.06
#&gt; TCGA.L5.A8NW.01     2  0.2532     0.8613 0.00 0.88 0.02 0.04 0.02 0.00 0.00 0.04
#&gt; TCGA.L5.A8NH.01     3  0.4180     0.6017 0.00 0.00 0.70 0.20 0.00 0.00 0.06 0.04
#&gt; TCGA.2H.A9GR.01     2  0.1607     0.8850 0.00 0.92 0.00 0.00 0.04 0.00 0.00 0.04
#&gt; TCGA.L5.A8NV.01     2  0.2623     0.8185 0.00 0.84 0.00 0.00 0.10 0.00 0.00 0.06
#&gt; TCGA.R6.A6XG.01     7  0.5259    -0.0145 0.00 0.02 0.10 0.34 0.00 0.00 0.52 0.02
#&gt; TCGA.L5.A8NN.01     1  0.3073     0.6914 0.80 0.00 0.00 0.00 0.00 0.10 0.00 0.10
#&gt; TCGA.L5.A8NS.01     2  0.0471     0.9107 0.00 0.98 0.00 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.JY.A938.01     5  0.3922     0.4629 0.00 0.30 0.00 0.00 0.64 0.00 0.00 0.06
#&gt; TCGA.R6.A8WG.01     1  0.4492     0.5956 0.70 0.00 0.00 0.00 0.02 0.06 0.04 0.18
#&gt; TCGA.R6.A6L6.01     1  0.1557     0.7293 0.92 0.00 0.00 0.00 0.00 0.06 0.00 0.02
#&gt; TCGA.V5.AASX.11     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NU.01     1  0.0000     0.7482 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XQ.01     6  0.2267     0.0000 0.18 0.00 0.00 0.00 0.00 0.82 0.00 0.00
#&gt; TCGA.L5.A4OT.01     5  0.7615     0.1865 0.00 0.30 0.12 0.10 0.34 0.00 0.06 0.08
#&gt; TCGA.ZR.A9CJ.01     1  0.1741     0.7406 0.92 0.00 0.00 0.00 0.02 0.02 0.00 0.04
#&gt; TCGA.R6.A8W8.01     4  0.6036     0.0504 0.00 0.00 0.26 0.46 0.00 0.00 0.16 0.12
#&gt; TCGA.JY.A93E.01     2  0.1607     0.8850 0.00 0.92 0.00 0.00 0.04 0.00 0.00 0.04
#&gt; TCGA.2H.A9GI.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.1275     0.8941 0.00 0.94 0.00 0.00 0.04 0.00 0.00 0.02
#&gt; TCGA.JY.A93D.01     1  0.3880     0.3739 0.64 0.00 0.00 0.00 0.32 0.02 0.02 0.00
#&gt; TCGA.L5.A4OX.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     5  0.5617     0.0581 0.20 0.00 0.00 0.02 0.60 0.04 0.12 0.02
#&gt; TCGA.2H.A9GF.01     7  0.7721     0.1378 0.00 0.14 0.06 0.28 0.04 0.02 0.36 0.10
#&gt; TCGA.2H.A9GO.01     1  0.2547     0.6903 0.84 0.00 0.00 0.00 0.00 0.04 0.00 0.12
#&gt; TCGA.L5.A8NR.01     2  0.2807     0.7877 0.00 0.84 0.10 0.02 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A4OU.01     5  0.4174     0.3406 0.00 0.40 0.00 0.00 0.54 0.00 0.00 0.06
#&gt; TCGA.JY.A93C.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.1607     0.8850 0.00 0.92 0.00 0.00 0.04 0.00 0.00 0.04
#&gt; TCGA.R6.A8WC.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4D.01     5  0.6255    -0.1982 0.00 0.00 0.00 0.28 0.48 0.06 0.06 0.12
#&gt; TCGA.2H.A9GM.01     3  0.1804     0.6664 0.00 0.00 0.90 0.08 0.02 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.1887     0.8714 0.00 0.90 0.00 0.00 0.06 0.00 0.00 0.04
#&gt; TCGA.IC.A6RE.01     4  0.6856     0.1357 0.00 0.02 0.16 0.50 0.08 0.00 0.10 0.14
#&gt; TCGA.RE.A7BO.01     2  0.1887     0.8714 0.00 0.90 0.00 0.00 0.06 0.00 0.00 0.04
#&gt; TCGA.L5.A8NJ.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     1  0.0000     0.7482 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6F8.01     2  0.0000     0.9164 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     5  0.5064     0.4516 0.00 0.24 0.08 0.00 0.60 0.00 0.00 0.08
#&gt; TCGA.L5.A8NL.01     5  0.3991     0.4541 0.00 0.32 0.00 0.00 0.62 0.00 0.00 0.06
#&gt; TCGA.2H.A9GH.01     2  0.4670    -0.1199 0.00 0.48 0.00 0.44 0.00 0.00 0.04 0.04
</code></pre>

<script>
$('#tab-node-02-get-classes-7-a').parent().next().next().hide();
$('#tab-node-02-get-classes-7-a').click(function(){
  $('#tab-node-02-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-02-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-02-consensus-heatmap'>
<ul>
<li><a href='#tab-node-02-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-02-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-02-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-02-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-02-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-02-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-02-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-02-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-02-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-02-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-02-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-02-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-02-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-02-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-02-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-02-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-02-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-02-membership-heatmap'>
<ul>
<li><a href='#tab-node-02-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-02-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-02-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-02-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-02-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-02-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-02-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-02-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-1-1.png" alt="plot of chunk tab-node-02-membership-heatmap-1"/></p>

</div>
<div id='tab-node-02-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-2-1.png" alt="plot of chunk tab-node-02-membership-heatmap-2"/></p>

</div>
<div id='tab-node-02-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-3-1.png" alt="plot of chunk tab-node-02-membership-heatmap-3"/></p>

</div>
<div id='tab-node-02-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-4-1.png" alt="plot of chunk tab-node-02-membership-heatmap-4"/></p>

</div>
<div id='tab-node-02-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-5-1.png" alt="plot of chunk tab-node-02-membership-heatmap-5"/></p>

</div>
<div id='tab-node-02-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-6-1.png" alt="plot of chunk tab-node-02-membership-heatmap-6"/></p>

</div>
<div id='tab-node-02-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-02-membership-heatmap-7-1.png" alt="plot of chunk tab-node-02-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-02-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-02-get-signatures'>
<ul>
<li><a href='#tab-node-02-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-02-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-02-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-02-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-02-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-02-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-02-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-02-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-1-1.png" alt="plot of chunk tab-node-02-get-signatures-1"/></p>

</div>
<div id='tab-node-02-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-2-1.png" alt="plot of chunk tab-node-02-get-signatures-2"/></p>

</div>
<div id='tab-node-02-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-3-1.png" alt="plot of chunk tab-node-02-get-signatures-3"/></p>

</div>
<div id='tab-node-02-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-4-1.png" alt="plot of chunk tab-node-02-get-signatures-4"/></p>

</div>
<div id='tab-node-02-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-5-1.png" alt="plot of chunk tab-node-02-get-signatures-5"/></p>

</div>
<div id='tab-node-02-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-6-1.png" alt="plot of chunk tab-node-02-get-signatures-6"/></p>

</div>
<div id='tab-node-02-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-02-get-signatures-7-1.png" alt="plot of chunk tab-node-02-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-02-signature_compare](figure_cola/node-02-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-02-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-02-dimension-reduction'>
<ul>
<li><a href='#tab-node-02-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-02-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-02-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-02-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-02-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-02-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-02-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-02-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-1-1.png" alt="plot of chunk tab-node-02-dimension-reduction-1"/></p>

</div>
<div id='tab-node-02-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-2-1.png" alt="plot of chunk tab-node-02-dimension-reduction-2"/></p>

</div>
<div id='tab-node-02-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-3-1.png" alt="plot of chunk tab-node-02-dimension-reduction-3"/></p>

</div>
<div id='tab-node-02-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-4-1.png" alt="plot of chunk tab-node-02-dimension-reduction-4"/></p>

</div>
<div id='tab-node-02-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-5-1.png" alt="plot of chunk tab-node-02-dimension-reduction-5"/></p>

</div>
<div id='tab-node-02-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-6-1.png" alt="plot of chunk tab-node-02-dimension-reduction-6"/></p>

</div>
<div id='tab-node-02-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02-dimension-reduction-7-1.png" alt="plot of chunk tab-node-02-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-02-collect-classes](figure_cola/node-02-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node021


Parent node: [Node02](#Node02).
Child nodes: 
                Node0111-leaf
        ,
                Node0112-leaf
        ,
                Node0113-leaf
        ,
                Node0121-leaf
        ,
                Node0122-leaf
        ,
                Node0123-leaf
        ,
                Node0131-leaf
        ,
                Node0132-leaf
        ,
                Node0133-leaf
        ,
                Node0211-leaf
        ,
                Node0212-leaf
        ,
                Node0221-leaf
        ,
                [Node0222](#Node0222)
        ,
                Node0223-leaf
        ,
                Node0231-leaf
        ,
                Node0232-leaf
        ,
                Node0233-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["021"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 15 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 2.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-021-collect-plots](figure_cola/node-021-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-021-select-partition-number](figure_cola/node-021-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           1.000       1.000         0.5148 0.486   0.486
#> 3 3 0.781           0.856       0.923         0.3290 0.829   0.647
#> 4 4 0.838           0.917       0.887         0.1250 0.914   0.727
#> 5 5 0.762           0.924       0.876         0.0617 0.924   0.667
#> 6 6 0.829           0.847       0.869         0.0518 1.000   1.000
#> 7 7 0.886           0.574       0.796         0.0279 0.971   0.812
#> 8 8 0.876           0.726       0.785         0.0323 0.952   0.643
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 2
```


Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-021-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-021-get-classes'>
<ul>
<li><a href='#tab-node-021-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-021-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-021-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-021-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-021-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-021-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-021-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-021-get-classes-1'>
<p><a id='tab-node-021-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2
#&gt; TCGA.L5.A4OF.01     1       0          1  1  0
#&gt; TCGA.R6.A6L4.01     2       0          1  0  1
#&gt; TCGA.L5.A4OO.01     2       0          1  0  1
#&gt; TCGA.L5.A43C.01     2       0          1  0  1
#&gt; TCGA.R6.A6KZ.01     1       0          1  1  0
#&gt; TCGA.L5.A8NN.01     1       0          1  1  0
#&gt; TCGA.R6.A8WG.01     1       0          1  1  0
#&gt; TCGA.R6.A6L6.01     2       0          1  0  1
#&gt; TCGA.L5.A8NU.01     2       0          1  0  1
#&gt; TCGA.R6.A6XQ.01     1       0          1  1  0
#&gt; TCGA.ZR.A9CJ.01     2       0          1  0  1
#&gt; TCGA.JY.A93D.01     2       0          1  0  1
#&gt; TCGA.R6.A6Y2.01     2       0          1  0  1
#&gt; TCGA.2H.A9GO.01     1       0          1  1  0
#&gt; TCGA.JY.A939.01     2       0          1  0  1
</code></pre>

<script>
$('#tab-node-021-get-classes-1-a').parent().next().next().hide();
$('#tab-node-021-get-classes-1-a').click(function(){
  $('#tab-node-021-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-021-get-classes-2'>
<p><a id='tab-node-021-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.L5.A4OF.01     1   0.000      0.779 1.00 0.00 0.00
#&gt; TCGA.R6.A6L4.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.L5.A4OO.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.L5.A43C.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.R6.A6KZ.01     1   0.153      0.741 0.96 0.00 0.04
#&gt; TCGA.L5.A8NN.01     1   0.540      0.806 0.72 0.00 0.28
#&gt; TCGA.R6.A8WG.01     1   0.540      0.806 0.72 0.00 0.28
#&gt; TCGA.R6.A6L6.01     3   0.540      0.551 0.00 0.28 0.72
#&gt; TCGA.L5.A8NU.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.R6.A6XQ.01     1   0.540      0.806 0.72 0.00 0.28
#&gt; TCGA.ZR.A9CJ.01     3   0.540      0.787 0.28 0.00 0.72
#&gt; TCGA.JY.A93D.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.R6.A6Y2.01     3   0.540      0.787 0.28 0.00 0.72
#&gt; TCGA.2H.A9GO.01     1   0.000      0.779 1.00 0.00 0.00
#&gt; TCGA.JY.A939.01     2   0.000      1.000 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-021-get-classes-2-a').parent().next().next().hide();
$('#tab-node-021-get-classes-2-a').click(function(){
  $('#tab-node-021-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-021-get-classes-3'>
<p><a id='tab-node-021-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3  p4
#&gt; TCGA.L5.A4OF.01     1   0.000      0.965 1.00 0.00 0.00 0.0
#&gt; TCGA.R6.A6L4.01     2   0.551      0.740 0.00 0.66 0.04 0.3
#&gt; TCGA.L5.A4OO.01     2   0.000      0.879 0.00 1.00 0.00 0.0
#&gt; TCGA.L5.A43C.01     2   0.000      0.879 0.00 1.00 0.00 0.0
#&gt; TCGA.R6.A6KZ.01     1   0.121      0.932 0.96 0.00 0.04 0.0
#&gt; TCGA.L5.A8NN.01     4   0.441      1.000 0.30 0.00 0.00 0.7
#&gt; TCGA.R6.A8WG.01     4   0.441      1.000 0.30 0.00 0.00 0.7
#&gt; TCGA.R6.A6L6.01     3   0.121      0.947 0.00 0.04 0.96 0.0
#&gt; TCGA.L5.A8NU.01     2   0.000      0.879 0.00 1.00 0.00 0.0
#&gt; TCGA.R6.A6XQ.01     4   0.441      1.000 0.30 0.00 0.00 0.7
#&gt; TCGA.ZR.A9CJ.01     3   0.121      0.973 0.04 0.00 0.96 0.0
#&gt; TCGA.JY.A93D.01     2   0.000      0.879 0.00 1.00 0.00 0.0
#&gt; TCGA.R6.A6Y2.01     3   0.121      0.973 0.04 0.00 0.96 0.0
#&gt; TCGA.2H.A9GO.01     1   0.000      0.965 1.00 0.00 0.00 0.0
#&gt; TCGA.JY.A939.01     2   0.551      0.740 0.00 0.66 0.04 0.3
</code></pre>

<script>
$('#tab-node-021-get-classes-3-a').parent().next().next().hide();
$('#tab-node-021-get-classes-3-a').click(function(){
  $('#tab-node-021-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-021-get-classes-4'>
<p><a id='tab-node-021-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.L5.A4OF.01     1  0.0000      0.965 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6L4.01     5  0.0000      0.959 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A4OO.01     2  0.5861      0.903 0.00 0.50 0.00 0.10 0.40
#&gt; TCGA.L5.A43C.01     2  0.4182      0.903 0.00 0.60 0.00 0.00 0.40
#&gt; TCGA.R6.A6KZ.01     1  0.1732      0.929 0.92 0.08 0.00 0.00 0.00
#&gt; TCGA.L5.A8NN.01     4  0.5258      0.838 0.14 0.18 0.00 0.68 0.00
#&gt; TCGA.R6.A8WG.01     4  0.2516      0.922 0.14 0.00 0.00 0.86 0.00
#&gt; TCGA.R6.A6L6.01     3  0.0000      0.947 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NU.01     2  0.4182      0.903 0.00 0.60 0.00 0.00 0.40
#&gt; TCGA.R6.A6XQ.01     4  0.2516      0.922 0.14 0.00 0.00 0.86 0.00
#&gt; TCGA.ZR.A9CJ.01     3  0.2280      0.905 0.00 0.12 0.88 0.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.5861      0.903 0.00 0.50 0.00 0.10 0.40
#&gt; TCGA.R6.A6Y2.01     3  0.0609      0.944 0.00 0.02 0.98 0.00 0.00
#&gt; TCGA.2H.A9GO.01     1  0.0000      0.965 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A939.01     5  0.1043      0.959 0.00 0.00 0.00 0.04 0.96
</code></pre>

<script>
$('#tab-node-021-get-classes-4-a').parent().next().next().hide();
$('#tab-node-021-get-classes-4-a').click(function(){
  $('#tab-node-021-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-021-get-classes-5'>
<p><a id='tab-node-021-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.L5.A4OF.01     1  0.1556      0.897 0.92 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.R6.A6L4.01     5  0.2048      0.940 0.00 0.12 0.00 0.00 0.88 0.00
#&gt; TCGA.L5.A4OO.01     2  0.4172      0.769 0.04 0.68 0.00 0.28 0.00 0.00
#&gt; TCGA.L5.A43C.01     2  0.0000      0.782 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     1  0.5256      0.784 0.68 0.00 0.00 0.18 0.06 0.08
#&gt; TCGA.L5.A8NN.01     6  0.0000      0.728 0.00 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.R6.A8WG.01     6  0.3409      0.872 0.00 0.00 0.00 0.30 0.00 0.70
#&gt; TCGA.R6.A6L6.01     3  0.0547      0.915 0.00 0.00 0.98 0.00 0.02 0.00
#&gt; TCGA.L5.A8NU.01     2  0.0000      0.782 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XQ.01     6  0.3409      0.872 0.00 0.00 0.00 0.30 0.00 0.70
#&gt; TCGA.ZR.A9CJ.01     3  0.3163      0.850 0.00 0.00 0.82 0.14 0.04 0.00
#&gt; TCGA.JY.A93D.01     2  0.3499      0.769 0.00 0.68 0.00 0.32 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     3  0.0547      0.911 0.00 0.00 0.98 0.02 0.00 0.00
#&gt; TCGA.2H.A9GO.01     1  0.1556      0.897 0.92 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.JY.A939.01     5  0.3854      0.940 0.04 0.12 0.00 0.04 0.80 0.00
</code></pre>

<script>
$('#tab-node-021-get-classes-5-a').parent().next().next().hide();
$('#tab-node-021-get-classes-5-a').click(function(){
  $('#tab-node-021-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-021-get-classes-6'>
<p><a id='tab-node-021-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.L5.A4OF.01     1  0.0863      0.806 0.96 0.00 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.R6.A6L4.01     5  0.1433      0.811 0.00 0.08 0.00 0.00 0.92 0.00 0.00
#&gt; TCGA.L5.A4OO.01     2  0.1664      0.439 0.02 0.92 0.00 0.00 0.00 0.00 0.06
#&gt; TCGA.L5.A43C.01     4  0.3562      0.000 0.00 0.50 0.00 0.50 0.00 0.00 0.00
#&gt; TCGA.R6.A6KZ.01     1  0.6222      0.611 0.54 0.00 0.00 0.10 0.06 0.04 0.26
#&gt; TCGA.L5.A8NN.01     6  0.3795      0.752 0.00 0.00 0.00 0.22 0.00 0.72 0.06
#&gt; TCGA.R6.A8WG.01     6  0.0504      0.876 0.00 0.00 0.00 0.00 0.00 0.98 0.02
#&gt; TCGA.R6.A6L6.01     3  0.3358      0.807 0.00 0.00 0.64 0.00 0.00 0.00 0.36
#&gt; TCGA.L5.A8NU.01     2  0.4923     -0.877 0.02 0.50 0.00 0.42 0.00 0.00 0.06
#&gt; TCGA.R6.A6XQ.01     6  0.0000      0.876 0.00 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.ZR.A9CJ.01     3  0.0000      0.659 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93D.01     2  0.0000      0.439 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6Y2.01     3  0.4175      0.793 0.00 0.00 0.58 0.04 0.00 0.00 0.38
#&gt; TCGA.2H.A9GO.01     1  0.1860      0.806 0.92 0.00 0.00 0.02 0.02 0.04 0.00
#&gt; TCGA.JY.A939.01     5  0.5001      0.811 0.00 0.08 0.00 0.12 0.68 0.00 0.12
</code></pre>

<script>
$('#tab-node-021-get-classes-6-a').parent().next().next().hide();
$('#tab-node-021-get-classes-6-a').click(function(){
  $('#tab-node-021-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-021-get-classes-7'>
<p><a id='tab-node-021-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.L5.A4OF.01     1  0.0000      0.862 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6L4.01     5  0.0471      0.772 0.00 0.02 0.00 0.00 0.98 0.00 0.00 0.00
#&gt; TCGA.L5.A4OO.01     2  0.0000      0.942 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.01     4  0.4971      0.845 0.00 0.22 0.00 0.62 0.00 0.08 0.08 0.00
#&gt; TCGA.R6.A6KZ.01     7  0.3333      0.000 0.50 0.00 0.00 0.00 0.00 0.00 0.50 0.00
#&gt; TCGA.L5.A8NN.01     8  0.3272      0.598 0.00 0.00 0.00 0.00 0.00 0.42 0.00 0.58
#&gt; TCGA.R6.A8WG.01     8  0.0471      0.809 0.00 0.00 0.00 0.02 0.00 0.00 0.00 0.98
#&gt; TCGA.R6.A6L6.01     3  0.3586      0.687 0.00 0.00 0.78 0.06 0.00 0.12 0.04 0.00
#&gt; TCGA.L5.A8NU.01     4  0.2534      0.845 0.00 0.22 0.00 0.78 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XQ.01     8  0.0000      0.809 0.00 0.00 0.00 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.ZR.A9CJ.01     3  0.5981      0.491 0.00 0.00 0.38 0.06 0.00 0.24 0.32 0.00
#&gt; TCGA.JY.A93D.01     2  0.1091      0.942 0.00 0.94 0.00 0.00 0.00 0.00 0.06 0.00
#&gt; TCGA.R6.A6Y2.01     3  0.0000      0.652 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GO.01     1  0.1741      0.862 0.92 0.00 0.00 0.02 0.02 0.04 0.00 0.00
#&gt; TCGA.JY.A939.01     5  0.4492      0.772 0.00 0.02 0.00 0.06 0.70 0.18 0.04 0.00
</code></pre>

<script>
$('#tab-node-021-get-classes-7-a').parent().next().next().hide();
$('#tab-node-021-get-classes-7-a').click(function(){
  $('#tab-node-021-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-021-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-021-consensus-heatmap'>
<ul>
<li><a href='#tab-node-021-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-021-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-021-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-021-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-021-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-021-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-021-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-021-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-021-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-021-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-021-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-021-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-021-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-021-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-021-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-021-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-021-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-021-membership-heatmap'>
<ul>
<li><a href='#tab-node-021-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-021-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-021-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-021-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-021-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-021-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-021-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-021-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-1-1.png" alt="plot of chunk tab-node-021-membership-heatmap-1"/></p>

</div>
<div id='tab-node-021-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-2-1.png" alt="plot of chunk tab-node-021-membership-heatmap-2"/></p>

</div>
<div id='tab-node-021-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-3-1.png" alt="plot of chunk tab-node-021-membership-heatmap-3"/></p>

</div>
<div id='tab-node-021-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-4-1.png" alt="plot of chunk tab-node-021-membership-heatmap-4"/></p>

</div>
<div id='tab-node-021-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-5-1.png" alt="plot of chunk tab-node-021-membership-heatmap-5"/></p>

</div>
<div id='tab-node-021-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-6-1.png" alt="plot of chunk tab-node-021-membership-heatmap-6"/></p>

</div>
<div id='tab-node-021-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-021-membership-heatmap-7-1.png" alt="plot of chunk tab-node-021-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-021-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-021-get-signatures'>
<ul>
<li><a href='#tab-node-021-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-021-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-021-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-021-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-021-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-021-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-021-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-021-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-1-1.png" alt="plot of chunk tab-node-021-get-signatures-1"/></p>

</div>
<div id='tab-node-021-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-2-1.png" alt="plot of chunk tab-node-021-get-signatures-2"/></p>

</div>
<div id='tab-node-021-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-3-1.png" alt="plot of chunk tab-node-021-get-signatures-3"/></p>

</div>
<div id='tab-node-021-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-4-1.png" alt="plot of chunk tab-node-021-get-signatures-4"/></p>

</div>
<div id='tab-node-021-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-5-1.png" alt="plot of chunk tab-node-021-get-signatures-5"/></p>

</div>
<div id='tab-node-021-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-6-1.png" alt="plot of chunk tab-node-021-get-signatures-6"/></p>

</div>
<div id='tab-node-021-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-021-get-signatures-7-1.png" alt="plot of chunk tab-node-021-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-021-signature_compare](figure_cola/node-021-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-021-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-021-dimension-reduction'>
<ul>
<li><a href='#tab-node-021-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-021-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-021-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-021-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-021-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-021-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-021-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-021-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-1-1.png" alt="plot of chunk tab-node-021-dimension-reduction-1"/></p>

</div>
<div id='tab-node-021-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-2-1.png" alt="plot of chunk tab-node-021-dimension-reduction-2"/></p>

</div>
<div id='tab-node-021-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-3-1.png" alt="plot of chunk tab-node-021-dimension-reduction-3"/></p>

</div>
<div id='tab-node-021-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-4-1.png" alt="plot of chunk tab-node-021-dimension-reduction-4"/></p>

</div>
<div id='tab-node-021-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-5-1.png" alt="plot of chunk tab-node-021-dimension-reduction-5"/></p>

</div>
<div id='tab-node-021-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-6-1.png" alt="plot of chunk tab-node-021-dimension-reduction-6"/></p>

</div>
<div id='tab-node-021-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-021-dimension-reduction-7-1.png" alt="plot of chunk tab-node-021-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-021-collect-classes](figure_cola/node-021-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node022


Parent node: [Node02](#Node02).
Child nodes: 
                Node0111-leaf
        ,
                Node0112-leaf
        ,
                Node0113-leaf
        ,
                Node0121-leaf
        ,
                Node0122-leaf
        ,
                Node0123-leaf
        ,
                Node0131-leaf
        ,
                Node0132-leaf
        ,
                Node0133-leaf
        ,
                Node0211-leaf
        ,
                Node0212-leaf
        ,
                Node0221-leaf
        ,
                [Node0222](#Node0222)
        ,
                Node0223-leaf
        ,
                Node0231-leaf
        ,
                Node0232-leaf
        ,
                Node0233-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["022"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 46 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-022-collect-plots](figure_cola/node-022-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-022-select-partition-number](figure_cola/node-022-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           1.000       1.000         0.5077 0.493   0.493
#> 3 3 1.000           0.974       0.990         0.1794 0.662   0.450
#> 4 4 0.684           0.849       0.899         0.2198 0.826   0.584
#> 5 5 0.786           0.758       0.862         0.0726 0.933   0.752
#> 6 6 0.807           0.714       0.843         0.0374 0.970   0.856
#> 7 7 0.764           0.658       0.780         0.0266 0.934   0.675
#> 8 8 0.788           0.539       0.788         0.0217 0.991   0.944
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-022-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-022-get-classes'>
<ul>
<li><a href='#tab-node-022-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-022-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-022-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-022-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-022-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-022-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-022-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-022-get-classes-1'>
<p><a id='tab-node-022-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2
#&gt; TCGA.JY.A6FB.01     1       0          1  1  0
#&gt; TCGA.Q9.A6FW.01     2       0          1  0  1
#&gt; TCGA.S8.A6BV.01     2       0          1  0  1
#&gt; TCGA.L5.A4OI.01     1       0          1  1  0
#&gt; TCGA.R6.A6DN.01     2       0          1  0  1
#&gt; TCGA.L5.A4OG.01     2       0          1  0  1
#&gt; TCGA.L5.A43E.01     1       0          1  1  0
#&gt; TCGA.X8.AAAR.01     2       0          1  0  1
#&gt; TCGA.L5.A4ON.01     1       0          1  1  0
#&gt; TCGA.V5.AASW.01     1       0          1  1  0
#&gt; TCGA.L5.A4OJ.01     1       0          1  1  0
#&gt; TCGA.L7.A6VZ.01     1       0          1  1  0
#&gt; TCGA.L5.A4OE.01     1       0          1  1  0
#&gt; TCGA.V5.A7RB.01     2       0          1  0  1
#&gt; TCGA.R6.A6DQ.01     1       0          1  1  0
#&gt; TCGA.L5.A88Y.01     1       0          1  1  0
#&gt; TCGA.L5.A88V.01     2       0          1  0  1
#&gt; TCGA.M9.A5M8.01     2       0          1  0  1
#&gt; TCGA.L5.A4OW.01     2       0          1  0  1
#&gt; TCGA.2H.A9GK.01     2       0          1  0  1
#&gt; TCGA.L5.A8NW.01     1       0          1  1  0
#&gt; TCGA.2H.A9GR.01     2       0          1  0  1
#&gt; TCGA.L5.A8NV.01     2       0          1  0  1
#&gt; TCGA.L5.A8NS.01     2       0          1  0  1
#&gt; TCGA.JY.A938.01     2       0          1  0  1
#&gt; TCGA.V5.AASX.11     1       0          1  1  0
#&gt; TCGA.L5.A893.01     2       0          1  0  1
#&gt; TCGA.L5.A4OT.01     1       0          1  1  0
#&gt; TCGA.JY.A93E.01     2       0          1  0  1
#&gt; TCGA.2H.A9GI.01     2       0          1  0  1
#&gt; TCGA.2H.A9GL.01     1       0          1  1  0
#&gt; TCGA.L5.A8NM.01     2       0          1  0  1
#&gt; TCGA.L5.A4OX.01     1       0          1  1  0
#&gt; TCGA.L5.A8NR.01     2       0          1  0  1
#&gt; TCGA.L5.A4OU.01     2       0          1  0  1
#&gt; TCGA.JY.A93C.01     2       0          1  0  1
#&gt; TCGA.V5.AASX.01     1       0          1  1  0
#&gt; TCGA.L5.A8NT.01     2       0          1  0  1
#&gt; TCGA.R6.A8WC.01     1       0          1  1  0
#&gt; TCGA.L5.A8NG.01     2       0          1  0  1
#&gt; TCGA.RE.A7BO.01     1       0          1  1  0
#&gt; TCGA.L5.A8NJ.01     1       0          1  1  0
#&gt; TCGA.JY.A6F8.01     1       0          1  1  0
#&gt; TCGA.VR.A8EQ.01     2       0          1  0  1
#&gt; TCGA.L5.A8NL.01     2       0          1  0  1
#&gt; TCGA.2H.A9GH.01     1       0          1  1  0
</code></pre>

<script>
$('#tab-node-022-get-classes-1-a').parent().next().next().hide();
$('#tab-node-022-get-classes-1-a').click(function(){
  $('#tab-node-022-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-022-get-classes-2'>
<p><a id='tab-node-022-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.JY.A6FB.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.Q9.A6FW.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.S8.A6BV.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.L5.A4OI.01     1  0.5948      0.443 0.64 0.36 0.00
#&gt; TCGA.R6.A6DN.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A4OG.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A43E.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.L5.A4ON.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.L7.A6VZ.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.V5.A7RB.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.R6.A6DQ.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A88V.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.M9.A5M8.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NW.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.2H.A9GR.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.JY.A938.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.V5.AASX.11     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0892      0.981 0.00 0.98 0.02
#&gt; TCGA.L5.A4OT.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.2H.A9GI.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.2H.A9GL.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NM.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A4OX.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NR.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A4OU.01     3  0.0000      1.000 0.00 0.00 1.00
#&gt; TCGA.JY.A93C.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.0892      0.981 0.00 0.98 0.02
#&gt; TCGA.R6.A8WC.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.RE.A7BO.01     1  0.0892      0.939 0.98 0.02 0.00
#&gt; TCGA.L5.A8NJ.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.JY.A6F8.01     1  0.0000      0.960 1.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0000      0.997 0.00 1.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0892      0.981 0.00 0.98 0.02
#&gt; TCGA.2H.A9GH.01     1  0.0000      0.960 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-022-get-classes-2-a').parent().next().next().hide();
$('#tab-node-022-get-classes-2-a').click(function(){
  $('#tab-node-022-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-022-get-classes-3'>
<p><a id='tab-node-022-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.JY.A6FB.01     1  0.3172      0.849 0.84 0.00 0.00 0.16
#&gt; TCGA.Q9.A6FW.01     3  0.2706      0.907 0.00 0.08 0.90 0.02
#&gt; TCGA.S8.A6BV.01     3  0.0000      0.980 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A4OI.01     4  0.4227      0.822 0.12 0.06 0.00 0.82
#&gt; TCGA.R6.A6DN.01     2  0.4406      0.706 0.00 0.70 0.00 0.30
#&gt; TCGA.L5.A4OG.01     2  0.3610      0.726 0.00 0.80 0.00 0.20
#&gt; TCGA.L5.A43E.01     1  0.0000      0.892 1.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     3  0.0707      0.976 0.00 0.00 0.98 0.02
#&gt; TCGA.L5.A4ON.01     1  0.0000      0.892 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     1  0.3172      0.849 0.84 0.00 0.00 0.16
#&gt; TCGA.L5.A4OJ.01     1  0.0000      0.892 1.00 0.00 0.00 0.00
#&gt; TCGA.L7.A6VZ.01     1  0.2921      0.858 0.86 0.00 0.00 0.14
#&gt; TCGA.L5.A4OE.01     4  0.3400      0.887 0.00 0.18 0.00 0.82
#&gt; TCGA.V5.A7RB.01     3  0.0000      0.980 0.00 0.00 1.00 0.00
#&gt; TCGA.R6.A6DQ.01     4  0.3400      0.887 0.00 0.18 0.00 0.82
#&gt; TCGA.L5.A88Y.01     4  0.3400      0.887 0.00 0.18 0.00 0.82
#&gt; TCGA.L5.A88V.01     3  0.0707      0.976 0.00 0.00 0.98 0.02
#&gt; TCGA.M9.A5M8.01     2  0.1637      0.836 0.00 0.94 0.00 0.06
#&gt; TCGA.L5.A4OW.01     2  0.3610      0.726 0.00 0.80 0.00 0.20
#&gt; TCGA.2H.A9GK.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.L5.A8NW.01     4  0.1211      0.818 0.00 0.04 0.00 0.96
#&gt; TCGA.2H.A9GR.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.JY.A938.01     3  0.0000      0.980 0.00 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.11     1  0.0000      0.892 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.L5.A4OT.01     1  0.3172      0.849 0.84 0.00 0.00 0.16
#&gt; TCGA.JY.A93E.01     2  0.0707      0.861 0.00 0.98 0.00 0.02
#&gt; TCGA.2H.A9GI.01     2  0.4713      0.646 0.00 0.64 0.00 0.36
#&gt; TCGA.2H.A9GL.01     4  0.1637      0.856 0.00 0.06 0.00 0.94
#&gt; TCGA.L5.A8NM.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.L5.A4OX.01     4  0.3400      0.887 0.00 0.18 0.00 0.82
#&gt; TCGA.L5.A8NR.01     2  0.4713      0.646 0.00 0.64 0.00 0.36
#&gt; TCGA.L5.A4OU.01     3  0.0000      0.980 0.00 0.00 1.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.4406      0.706 0.00 0.70 0.00 0.30
#&gt; TCGA.V5.AASX.01     4  0.3400      0.887 0.00 0.18 0.00 0.82
#&gt; TCGA.L5.A8NT.01     2  0.3853      0.778 0.00 0.82 0.02 0.16
#&gt; TCGA.R6.A8WC.01     1  0.0000      0.892 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0000      0.864 0.00 1.00 0.00 0.00
#&gt; TCGA.RE.A7BO.01     4  0.4088      0.797 0.14 0.04 0.00 0.82
#&gt; TCGA.L5.A8NJ.01     1  0.4713      0.535 0.64 0.00 0.00 0.36
#&gt; TCGA.JY.A6F8.01     1  0.0000      0.892 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0707      0.868 0.00 0.98 0.02 0.00
#&gt; TCGA.2H.A9GH.01     4  0.1411      0.808 0.02 0.02 0.00 0.96
</code></pre>

<script>
$('#tab-node-022-get-classes-3-a').parent().next().next().hide();
$('#tab-node-022-get-classes-3-a').click(function(){
  $('#tab-node-022-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-022-get-classes-4'>
<p><a id='tab-node-022-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.JY.A6FB.01     1  0.3390     0.8644 0.84 0.00 0.00 0.10 0.06
#&gt; TCGA.Q9.A6FW.01     3  0.5355     0.6399 0.00 0.22 0.66 0.00 0.12
#&gt; TCGA.S8.A6BV.01     3  0.0000     0.9198 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OI.01     4  0.2249     0.8716 0.02 0.02 0.00 0.92 0.04
#&gt; TCGA.R6.A6DN.01     5  0.4990     0.6732 0.00 0.36 0.00 0.04 0.60
#&gt; TCGA.L5.A4OG.01     2  0.6133    -0.1825 0.00 0.54 0.00 0.16 0.30
#&gt; TCGA.L5.A43E.01     1  0.0000     0.8788 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     3  0.1732     0.9008 0.00 0.00 0.92 0.00 0.08
#&gt; TCGA.L5.A4ON.01     1  0.0000     0.8788 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     1  0.5130     0.7925 0.68 0.00 0.00 0.10 0.22
#&gt; TCGA.L5.A4OJ.01     1  0.0000     0.8788 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L7.A6VZ.01     1  0.3110     0.8708 0.86 0.00 0.00 0.08 0.06
#&gt; TCGA.L5.A4OE.01     4  0.1410     0.8954 0.00 0.06 0.00 0.94 0.00
#&gt; TCGA.V5.A7RB.01     3  0.0000     0.9198 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     4  0.1410     0.8954 0.00 0.06 0.00 0.94 0.00
#&gt; TCGA.L5.A88Y.01     4  0.1043     0.9009 0.00 0.04 0.00 0.96 0.00
#&gt; TCGA.L5.A88V.01     3  0.2873     0.8790 0.00 0.00 0.86 0.02 0.12
#&gt; TCGA.M9.A5M8.01     2  0.3291     0.6782 0.00 0.84 0.00 0.12 0.04
#&gt; TCGA.L5.A4OW.01     2  0.6200    -0.1566 0.00 0.54 0.00 0.18 0.28
#&gt; TCGA.2H.A9GK.01     2  0.0609     0.8371 0.00 0.98 0.00 0.00 0.02
#&gt; TCGA.L5.A8NW.01     4  0.4227     0.1525 0.00 0.00 0.00 0.58 0.42
#&gt; TCGA.2H.A9GR.01     2  0.0000     0.8469 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000     0.8469 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000     0.8469 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A938.01     3  0.0000     0.9198 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.AASX.11     1  0.0000     0.8788 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.1043     0.8324 0.00 0.96 0.00 0.00 0.04
#&gt; TCGA.L5.A4OT.01     1  0.3390     0.8644 0.84 0.00 0.00 0.10 0.06
#&gt; TCGA.JY.A93E.01     2  0.0000     0.8469 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     5  0.5700     0.7238 0.00 0.28 0.00 0.12 0.60
#&gt; TCGA.2H.A9GL.01     4  0.2012     0.8770 0.00 0.02 0.00 0.92 0.06
#&gt; TCGA.L5.A8NM.01     2  0.0000     0.8469 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OX.01     4  0.1043     0.9009 0.00 0.04 0.00 0.96 0.00
#&gt; TCGA.L5.A8NR.01     5  0.5700     0.7238 0.00 0.28 0.00 0.12 0.60
#&gt; TCGA.L5.A4OU.01     3  0.0000     0.9198 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     5  0.5048     0.6568 0.00 0.38 0.00 0.04 0.58
#&gt; TCGA.V5.AASX.01     4  0.1410     0.8954 0.00 0.06 0.00 0.94 0.00
#&gt; TCGA.L5.A8NT.01     2  0.3109     0.5985 0.00 0.80 0.00 0.00 0.20
#&gt; TCGA.R6.A8WC.01     1  0.4254     0.8108 0.74 0.00 0.00 0.04 0.22
#&gt; TCGA.L5.A8NG.01     2  0.0000     0.8469 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.RE.A7BO.01     4  0.1216     0.8894 0.02 0.02 0.00 0.96 0.00
#&gt; TCGA.L5.A8NJ.01     1  0.5791     0.7181 0.60 0.00 0.00 0.14 0.26
#&gt; TCGA.JY.A6F8.01     1  0.0000     0.8788 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.0609     0.8367 0.00 0.98 0.00 0.00 0.02
#&gt; TCGA.L5.A8NL.01     2  0.0609     0.8371 0.00 0.98 0.00 0.00 0.02
#&gt; TCGA.2H.A9GH.01     5  0.4613     0.0497 0.02 0.00 0.00 0.36 0.62
</code></pre>

<script>
$('#tab-node-022-get-classes-4-a').parent().next().next().hide();
$('#tab-node-022-get-classes-4-a').click(function(){
  $('#tab-node-022-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-022-get-classes-5'>
<p><a id='tab-node-022-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.JY.A6FB.01     1  0.3688     0.7395 0.80 0.00 0.00 0.02 0.04 0.14
#&gt; TCGA.Q9.A6FW.01     3  0.5428     0.4910 0.00 0.32 0.54 0.00 0.14 0.00
#&gt; TCGA.S8.A6BV.01     3  0.1267     0.8627 0.00 0.00 0.94 0.00 0.06 0.00
#&gt; TCGA.L5.A4OI.01     4  0.2790     0.8004 0.00 0.00 0.00 0.84 0.14 0.02
#&gt; TCGA.R6.A6DN.01     5  0.6294     0.9096 0.00 0.18 0.00 0.04 0.52 0.26
#&gt; TCGA.L5.A4OG.01     2  0.7411    -0.2527 0.00 0.38 0.00 0.24 0.14 0.24
#&gt; TCGA.L5.A43E.01     1  0.0000     0.8615 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     3  0.2048     0.8497 0.00 0.00 0.88 0.00 0.12 0.00
#&gt; TCGA.L5.A4ON.01     1  0.0547     0.8569 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.V5.AASW.01     6  0.3864     0.4319 0.48 0.00 0.00 0.00 0.00 0.52
#&gt; TCGA.L5.A4OJ.01     1  0.0000     0.8615 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L7.A6VZ.01     1  0.3688     0.7395 0.80 0.00 0.00 0.02 0.04 0.14
#&gt; TCGA.L5.A4OE.01     4  0.0000     0.8752 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.A7RB.01     3  0.0000     0.8677 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     4  0.1480     0.8606 0.00 0.00 0.00 0.94 0.02 0.04
#&gt; TCGA.L5.A88Y.01     4  0.0937     0.8652 0.00 0.00 0.00 0.96 0.00 0.04
#&gt; TCGA.L5.A88V.01     3  0.4607     0.7658 0.00 0.02 0.72 0.00 0.18 0.08
#&gt; TCGA.M9.A5M8.01     2  0.4703     0.5742 0.00 0.72 0.00 0.18 0.04 0.06
#&gt; TCGA.L5.A4OW.01     2  0.7320    -0.2047 0.00 0.38 0.00 0.28 0.12 0.22
#&gt; TCGA.2H.A9GK.01     2  0.0000     0.8127 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     4  0.5655     0.0345 0.00 0.00 0.00 0.48 0.16 0.36
#&gt; TCGA.2H.A9GR.01     2  0.0547     0.8191 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0547     0.8191 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0000     0.8127 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A938.01     3  0.0000     0.8677 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.11     1  0.0000     0.8615 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.0547     0.8081 0.00 0.98 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A4OT.01     1  0.3688     0.7395 0.80 0.00 0.00 0.02 0.04 0.14
#&gt; TCGA.JY.A93E.01     2  0.0547     0.8191 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.2H.A9GI.01     5  0.6356     0.9419 0.00 0.16 0.00 0.04 0.48 0.32
#&gt; TCGA.2H.A9GL.01     4  0.2790     0.8004 0.00 0.00 0.00 0.84 0.14 0.02
#&gt; TCGA.L5.A8NM.01     2  0.0547     0.8191 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A4OX.01     4  0.0000     0.8752 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NR.01     5  0.6356     0.9419 0.00 0.16 0.00 0.04 0.48 0.32
#&gt; TCGA.L5.A4OU.01     3  0.0000     0.8677 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     5  0.6365     0.9375 0.00 0.18 0.00 0.04 0.50 0.28
#&gt; TCGA.V5.AASX.01     4  0.0000     0.8752 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     2  0.3309     0.4240 0.00 0.72 0.00 0.00 0.28 0.00
#&gt; TCGA.R6.A8WC.01     6  0.3864     0.4319 0.48 0.00 0.00 0.00 0.00 0.52
#&gt; TCGA.L5.A8NG.01     2  0.0547     0.8191 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.RE.A7BO.01     4  0.1092     0.8689 0.00 0.00 0.00 0.96 0.02 0.02
#&gt; TCGA.L5.A8NJ.01     6  0.4575     0.5270 0.34 0.00 0.00 0.02 0.02 0.62
#&gt; TCGA.JY.A6F8.01     1  0.0000     0.8615 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.1092     0.8105 0.00 0.96 0.00 0.02 0.02 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0000     0.8127 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GH.01     6  0.2048     0.0763 0.00 0.00 0.00 0.12 0.00 0.88
</code></pre>

<script>
$('#tab-node-022-get-classes-5-a').parent().next().next().hide();
$('#tab-node-022-get-classes-5-a').click(function(){
  $('#tab-node-022-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-022-get-classes-6'>
<p><a id='tab-node-022-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.JY.A6FB.01     1  0.4763     0.5175 0.62 0.00 0.00 0.18 0.00 0.20 0.00
#&gt; TCGA.Q9.A6FW.01     3  0.7367     0.4853 0.00 0.22 0.44 0.10 0.12 0.12 0.00
#&gt; TCGA.S8.A6BV.01     3  0.0504     0.8151 0.00 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A4OI.01     7  0.1166     0.9139 0.00 0.00 0.00 0.06 0.00 0.00 0.94
#&gt; TCGA.R6.A6DN.01     5  0.4569     0.7764 0.00 0.18 0.00 0.08 0.70 0.04 0.00
#&gt; TCGA.L5.A4OG.01     4  0.5291     0.2232 0.00 0.30 0.00 0.50 0.20 0.00 0.00
#&gt; TCGA.L5.A43E.01     1  0.0000     0.7790 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     3  0.3940     0.7593 0.00 0.00 0.78 0.06 0.08 0.08 0.00
#&gt; TCGA.L5.A4ON.01     1  0.0504     0.7741 0.98 0.00 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.V5.AASW.01     6  0.3047     0.7598 0.28 0.00 0.00 0.00 0.00 0.72 0.00
#&gt; TCGA.L5.A4OJ.01     1  0.0000     0.7790 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L7.A6VZ.01     1  0.4629     0.5358 0.64 0.00 0.00 0.16 0.00 0.20 0.00
#&gt; TCGA.L5.A4OE.01     4  0.4421     0.2835 0.00 0.00 0.00 0.50 0.02 0.02 0.46
#&gt; TCGA.V5.A7RB.01     3  0.0000     0.8168 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     4  0.3606     0.3904 0.00 0.00 0.00 0.68 0.00 0.02 0.30
#&gt; TCGA.L5.A88Y.01     4  0.3755     0.3854 0.00 0.00 0.00 0.64 0.00 0.02 0.34
#&gt; TCGA.L5.A88V.01     3  0.6543     0.6211 0.00 0.02 0.54 0.16 0.06 0.20 0.02
#&gt; TCGA.M9.A5M8.01     4  0.4936     0.0824 0.00 0.44 0.00 0.48 0.06 0.02 0.00
#&gt; TCGA.L5.A4OW.01     4  0.5291     0.2232 0.00 0.30 0.00 0.50 0.20 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.0504     0.8973 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.L5.A8NW.01     4  0.5410     0.2139 0.00 0.00 0.00 0.48 0.38 0.02 0.12
#&gt; TCGA.2H.A9GR.01     2  0.0504     0.9004 0.00 0.98 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.1006     0.8968 0.00 0.96 0.00 0.02 0.02 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.0504     0.8973 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.JY.A938.01     3  0.0000     0.8168 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.11     1  0.0000     0.7790 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.1860     0.8694 0.00 0.92 0.00 0.04 0.02 0.02 0.00
#&gt; TCGA.L5.A4OT.01     1  0.4763     0.5175 0.62 0.00 0.00 0.18 0.00 0.20 0.00
#&gt; TCGA.JY.A93E.01     2  0.1860     0.8750 0.00 0.92 0.00 0.04 0.02 0.02 0.00
#&gt; TCGA.2H.A9GI.01     5  0.3487     0.8379 0.00 0.10 0.00 0.12 0.78 0.00 0.00
#&gt; TCGA.2H.A9GL.01     7  0.2213     0.9157 0.00 0.00 0.00 0.04 0.04 0.02 0.90
#&gt; TCGA.L5.A8NM.01     2  0.1860     0.8750 0.00 0.92 0.00 0.04 0.02 0.02 0.00
#&gt; TCGA.L5.A4OX.01     4  0.4421     0.2835 0.00 0.00 0.00 0.50 0.02 0.02 0.46
#&gt; TCGA.L5.A8NR.01     5  0.3487     0.8379 0.00 0.10 0.00 0.12 0.78 0.00 0.00
#&gt; TCGA.L5.A4OU.01     3  0.0000     0.8168 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     5  0.2422     0.8363 0.00 0.18 0.00 0.00 0.82 0.00 0.00
#&gt; TCGA.V5.AASX.01     4  0.4421     0.2835 0.00 0.00 0.00 0.50 0.02 0.02 0.46
#&gt; TCGA.L5.A8NT.01     2  0.3867     0.1604 0.00 0.60 0.00 0.00 0.38 0.02 0.00
#&gt; TCGA.R6.A8WC.01     6  0.3139     0.7449 0.30 0.00 0.00 0.00 0.00 0.70 0.00
#&gt; TCGA.L5.A8NG.01     2  0.0504     0.9004 0.00 0.98 0.00 0.02 0.00 0.00 0.00
#&gt; TCGA.RE.A7BO.01     4  0.3867     0.3564 0.00 0.00 0.00 0.60 0.00 0.02 0.38
#&gt; TCGA.L5.A8NJ.01     6  0.4377     0.7593 0.24 0.00 0.00 0.06 0.00 0.68 0.02
#&gt; TCGA.JY.A6F8.01     1  0.0000     0.7790 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.1664     0.8730 0.00 0.92 0.00 0.06 0.02 0.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0504     0.8973 0.00 0.98 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.2H.A9GH.01     6  0.4242     0.5212 0.00 0.00 0.00 0.08 0.18 0.72 0.02
</code></pre>

<script>
$('#tab-node-022-get-classes-6-a').parent().next().next().hide();
$('#tab-node-022-get-classes-6-a').click(function(){
  $('#tab-node-022-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-022-get-classes-7'>
<p><a id='tab-node-022-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.JY.A6FB.01     1  0.5037      0.584 0.54 0.00 0.00 0.00 0.00 0.14 0.02 0.30
#&gt; TCGA.Q9.A6FW.01     3  0.6879      0.238 0.00 0.36 0.40 0.02 0.08 0.06 0.02 0.06
#&gt; TCGA.S8.A6BV.01     3  0.0808      0.786 0.00 0.00 0.96 0.00 0.04 0.00 0.00 0.00
#&gt; TCGA.L5.A4OI.01     7  0.3675      0.925 0.00 0.00 0.00 0.04 0.00 0.00 0.66 0.30
#&gt; TCGA.R6.A6DN.01     5  0.5407      0.448 0.00 0.02 0.00 0.12 0.62 0.08 0.00 0.16
#&gt; TCGA.L5.A4OG.01     4  0.2025      0.191 0.00 0.10 0.00 0.88 0.02 0.00 0.00 0.00
#&gt; TCGA.L5.A43E.01     1  0.0000      0.762 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.X8.AAAR.01     3  0.2624      0.756 0.00 0.00 0.86 0.00 0.06 0.02 0.00 0.06
#&gt; TCGA.L5.A4ON.01     1  0.2025      0.742 0.88 0.00 0.00 0.00 0.00 0.00 0.02 0.10
#&gt; TCGA.V5.AASW.01     6  0.2114      0.864 0.16 0.00 0.00 0.00 0.00 0.84 0.00 0.00
#&gt; TCGA.L5.A4OJ.01     1  0.0000      0.762 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L7.A6VZ.01     1  0.5037      0.584 0.54 0.00 0.00 0.00 0.00 0.14 0.02 0.30
#&gt; TCGA.L5.A4OE.01     4  0.4803     -0.478 0.00 0.02 0.00 0.46 0.00 0.00 0.08 0.44
#&gt; TCGA.V5.A7RB.01     3  0.0000      0.791 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     4  0.3714     -0.751 0.00 0.02 0.00 0.54 0.00 0.00 0.00 0.44
#&gt; TCGA.L5.A88Y.01     4  0.3729     -0.756 0.00 0.02 0.00 0.52 0.00 0.00 0.00 0.46
#&gt; TCGA.L5.A88V.01     3  0.6619      0.468 0.00 0.04 0.46 0.00 0.02 0.06 0.26 0.16
#&gt; TCGA.M9.A5M8.01     4  0.4028      0.101 0.00 0.28 0.00 0.66 0.00 0.04 0.00 0.02
#&gt; TCGA.L5.A4OW.01     4  0.2025      0.191 0.00 0.10 0.00 0.88 0.02 0.00 0.00 0.00
#&gt; TCGA.2H.A9GK.01     2  0.1408      0.906 0.00 0.94 0.00 0.02 0.02 0.00 0.02 0.00
#&gt; TCGA.L5.A8NW.01     4  0.4399     -0.593 0.00 0.00 0.00 0.50 0.44 0.02 0.00 0.04
#&gt; TCGA.2H.A9GR.01     2  0.0941      0.918 0.00 0.96 0.00 0.02 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NV.01     2  0.0941      0.918 0.00 0.96 0.00 0.02 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NS.01     2  0.1408      0.906 0.00 0.94 0.00 0.02 0.02 0.00 0.02 0.00
#&gt; TCGA.JY.A938.01     3  0.0000      0.791 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.11     1  0.0000      0.762 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.2204      0.891 0.00 0.90 0.00 0.04 0.02 0.02 0.02 0.00
#&gt; TCGA.L5.A4OT.01     1  0.5037      0.584 0.54 0.00 0.00 0.00 0.00 0.14 0.02 0.30
#&gt; TCGA.JY.A93E.01     2  0.1275      0.910 0.00 0.94 0.00 0.02 0.00 0.00 0.00 0.04
#&gt; TCGA.2H.A9GI.01     5  0.3142      0.786 0.00 0.00 0.00 0.36 0.64 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     7  0.4134      0.924 0.00 0.00 0.00 0.08 0.00 0.00 0.62 0.30
#&gt; TCGA.L5.A8NM.01     2  0.1275      0.910 0.00 0.94 0.00 0.02 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A4OX.01     4  0.4562     -0.486 0.00 0.00 0.00 0.46 0.00 0.00 0.10 0.44
#&gt; TCGA.L5.A8NR.01     5  0.3142      0.786 0.00 0.00 0.00 0.36 0.64 0.00 0.00 0.00
#&gt; TCGA.L5.A4OU.01     3  0.0000      0.791 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     5  0.3198      0.774 0.00 0.02 0.00 0.26 0.72 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     4  0.4803     -0.478 0.00 0.02 0.00 0.46 0.00 0.00 0.08 0.44
#&gt; TCGA.L5.A8NT.01     2  0.3941      0.613 0.00 0.68 0.00 0.04 0.26 0.00 0.02 0.00
#&gt; TCGA.R6.A8WC.01     6  0.2114      0.864 0.16 0.00 0.00 0.00 0.00 0.84 0.00 0.00
#&gt; TCGA.L5.A8NG.01     2  0.1275      0.918 0.00 0.94 0.00 0.04 0.00 0.00 0.00 0.02
#&gt; TCGA.RE.A7BO.01     8  0.3729      0.000 0.00 0.00 0.00 0.46 0.00 0.02 0.00 0.52
#&gt; TCGA.L5.A8NJ.01     6  0.4294      0.849 0.10 0.00 0.00 0.06 0.02 0.76 0.04 0.02
#&gt; TCGA.JY.A6F8.01     1  0.0000      0.762 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     2  0.1557      0.911 0.00 0.92 0.00 0.06 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NL.01     2  0.0941      0.907 0.00 0.96 0.00 0.00 0.02 0.00 0.02 0.00
#&gt; TCGA.2H.A9GH.01     6  0.2623      0.762 0.00 0.00 0.00 0.10 0.06 0.84 0.00 0.00
</code></pre>

<script>
$('#tab-node-022-get-classes-7-a').parent().next().next().hide();
$('#tab-node-022-get-classes-7-a').click(function(){
  $('#tab-node-022-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-022-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-022-consensus-heatmap'>
<ul>
<li><a href='#tab-node-022-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-022-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-022-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-022-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-022-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-022-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-022-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-022-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-022-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-022-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-022-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-022-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-022-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-022-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-022-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-022-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-022-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-022-membership-heatmap'>
<ul>
<li><a href='#tab-node-022-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-022-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-022-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-022-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-022-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-022-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-022-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-022-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-1-1.png" alt="plot of chunk tab-node-022-membership-heatmap-1"/></p>

</div>
<div id='tab-node-022-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-2-1.png" alt="plot of chunk tab-node-022-membership-heatmap-2"/></p>

</div>
<div id='tab-node-022-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-3-1.png" alt="plot of chunk tab-node-022-membership-heatmap-3"/></p>

</div>
<div id='tab-node-022-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-4-1.png" alt="plot of chunk tab-node-022-membership-heatmap-4"/></p>

</div>
<div id='tab-node-022-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-5-1.png" alt="plot of chunk tab-node-022-membership-heatmap-5"/></p>

</div>
<div id='tab-node-022-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-6-1.png" alt="plot of chunk tab-node-022-membership-heatmap-6"/></p>

</div>
<div id='tab-node-022-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-022-membership-heatmap-7-1.png" alt="plot of chunk tab-node-022-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-022-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-022-get-signatures'>
<ul>
<li><a href='#tab-node-022-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-022-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-022-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-022-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-022-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-022-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-022-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-022-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-1-1.png" alt="plot of chunk tab-node-022-get-signatures-1"/></p>

</div>
<div id='tab-node-022-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-2-1.png" alt="plot of chunk tab-node-022-get-signatures-2"/></p>

</div>
<div id='tab-node-022-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-3-1.png" alt="plot of chunk tab-node-022-get-signatures-3"/></p>

</div>
<div id='tab-node-022-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-4-1.png" alt="plot of chunk tab-node-022-get-signatures-4"/></p>

</div>
<div id='tab-node-022-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-5-1.png" alt="plot of chunk tab-node-022-get-signatures-5"/></p>

</div>
<div id='tab-node-022-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-6-1.png" alt="plot of chunk tab-node-022-get-signatures-6"/></p>

</div>
<div id='tab-node-022-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-022-get-signatures-7-1.png" alt="plot of chunk tab-node-022-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-022-signature_compare](figure_cola/node-022-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-022-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-022-dimension-reduction'>
<ul>
<li><a href='#tab-node-022-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-022-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-022-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-022-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-022-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-022-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-022-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-022-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-1-1.png" alt="plot of chunk tab-node-022-dimension-reduction-1"/></p>

</div>
<div id='tab-node-022-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-2-1.png" alt="plot of chunk tab-node-022-dimension-reduction-2"/></p>

</div>
<div id='tab-node-022-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-3-1.png" alt="plot of chunk tab-node-022-dimension-reduction-3"/></p>

</div>
<div id='tab-node-022-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-4-1.png" alt="plot of chunk tab-node-022-dimension-reduction-4"/></p>

</div>
<div id='tab-node-022-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-5-1.png" alt="plot of chunk tab-node-022-dimension-reduction-5"/></p>

</div>
<div id='tab-node-022-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-6-1.png" alt="plot of chunk tab-node-022-dimension-reduction-6"/></p>

</div>
<div id='tab-node-022-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-022-dimension-reduction-7-1.png" alt="plot of chunk tab-node-022-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-022-collect-classes](figure_cola/node-022-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node0222


Parent node: [Node022](#Node022).
Child nodes: 
                [Node02221](#Node02221)
        ,
                Node02222-leaf
        ,
                Node02223-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["0222"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 25 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-0222-collect-plots](figure_cola/node-0222-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-0222-select-partition-number](figure_cola/node-0222-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 0.580           0.777       0.871         0.4791 0.500   0.500
#> 3 3 1.000           0.953       0.984         0.3506 0.613   0.373
#> 4 4 0.787           0.518       0.730         0.1348 0.817   0.542
#> 5 5 0.801           0.885       0.889         0.0990 0.827   0.447
#> 6 6 0.881           0.899       0.904         0.0431 0.967   0.818
#> 7 7 0.866           0.841       0.887         0.0236 1.000   1.000
#> 8 8 0.909           0.786       0.862         0.0234 0.990   0.933
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
```


Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-0222-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-0222-get-classes'>
<ul>
<li><a href='#tab-node-0222-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-0222-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-0222-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-0222-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-0222-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-0222-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-0222-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-0222-get-classes-1'>
<p><a id='tab-node-0222-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2
#&gt; TCGA.R6.A6DN.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.L5.A4OG.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.L5.A4OE.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.R6.A6DQ.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.L5.A88Y.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.M9.A5M8.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.L5.A4OW.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.2H.A9GK.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.L5.A8NW.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.2H.A9GR.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.L5.A8NV.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.L5.A8NS.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.L5.A893.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.JY.A93E.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.2H.A9GI.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.2H.A9GL.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.L5.A8NM.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.L5.A4OX.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.L5.A8NR.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.JY.A93C.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.V5.AASX.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.L5.A8NT.01     2   0.995      0.729 0.46 0.54
#&gt; TCGA.L5.A8NG.01     2   0.000      0.513 0.00 1.00
#&gt; TCGA.VR.A8EQ.01     1   0.995      1.000 0.54 0.46
#&gt; TCGA.L5.A8NL.01     1   0.995      1.000 0.54 0.46
</code></pre>

<script>
$('#tab-node-0222-get-classes-1-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-1-a').click(function(){
  $('#tab-node-0222-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0222-get-classes-2'>
<p><a id='tab-node-0222-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette  p1  p2 p3
#&gt; TCGA.R6.A6DN.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.L5.A4OG.01     3   0.000      1.000 0.0 0.0  1
#&gt; TCGA.L5.A4OE.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.R6.A6DQ.01     3   0.000      1.000 0.0 0.0  1
#&gt; TCGA.L5.A88Y.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.M9.A5M8.01     3   0.000      1.000 0.0 0.0  1
#&gt; TCGA.L5.A4OW.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.2H.A9GK.01     3   0.000      1.000 0.0 0.0  1
#&gt; TCGA.L5.A8NW.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.2H.A9GR.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.L5.A8NV.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.L5.A8NS.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.L5.A893.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.JY.A93E.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.2H.A9GI.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.2H.A9GL.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.L5.A8NM.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.L5.A4OX.01     2   0.613      0.333 0.4 0.6  0
#&gt; TCGA.L5.A8NR.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.JY.A93C.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.V5.AASX.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.L5.A8NT.01     2   0.000      0.927 0.0 1.0  0
#&gt; TCGA.L5.A8NG.01     1   0.000      1.000 1.0 0.0  0
#&gt; TCGA.VR.A8EQ.01     3   0.000      1.000 0.0 0.0  1
#&gt; TCGA.L5.A8NL.01     1   0.000      1.000 1.0 0.0  0
</code></pre>

<script>
$('#tab-node-0222-get-classes-2-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-2-a').click(function(){
  $('#tab-node-0222-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0222-get-classes-3'>
<p><a id='tab-node-0222-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2 p3   p4
#&gt; TCGA.R6.A6DN.01     2   0.000      0.847 0.00 1.00  0 0.00
#&gt; TCGA.L5.A4OG.01     3   0.000      1.000 0.00 0.00  1 0.00
#&gt; TCGA.L5.A4OE.01     1   0.000      0.676 1.00 0.00  0 0.00
#&gt; TCGA.R6.A6DQ.01     3   0.000      1.000 0.00 0.00  1 0.00
#&gt; TCGA.L5.A88Y.01     4   0.491     -0.460 0.42 0.00  0 0.58
#&gt; TCGA.M9.A5M8.01     3   0.000      1.000 0.00 0.00  1 0.00
#&gt; TCGA.L5.A4OW.01     4   0.491     -0.460 0.42 0.00  0 0.58
#&gt; TCGA.2H.A9GK.01     3   0.000      1.000 0.00 0.00  1 0.00
#&gt; TCGA.L5.A8NW.01     4   0.495     -0.221 0.00 0.44  0 0.56
#&gt; TCGA.2H.A9GR.01     1   0.000      0.676 1.00 0.00  0 0.00
#&gt; TCGA.L5.A8NV.01     1   0.495      0.567 0.56 0.00  0 0.44
#&gt; TCGA.L5.A8NS.01     1   0.495      0.567 0.56 0.00  0 0.44
#&gt; TCGA.L5.A893.01     1   0.495      0.567 0.56 0.00  0 0.44
#&gt; TCGA.JY.A93E.01     1   0.000      0.676 1.00 0.00  0 0.00
#&gt; TCGA.2H.A9GI.01     4   0.495     -0.221 0.00 0.44  0 0.56
#&gt; TCGA.2H.A9GL.01     2   0.471      0.393 0.00 0.64  0 0.36
#&gt; TCGA.L5.A8NM.01     1   0.000      0.676 1.00 0.00  0 0.00
#&gt; TCGA.L5.A4OX.01     1   0.380      0.394 0.78 0.00  0 0.22
#&gt; TCGA.L5.A8NR.01     2   0.000      0.847 0.00 1.00  0 0.00
#&gt; TCGA.JY.A93C.01     2   0.000      0.847 0.00 1.00  0 0.00
#&gt; TCGA.V5.AASX.01     1   0.000      0.676 1.00 0.00  0 0.00
#&gt; TCGA.L5.A8NT.01     4   0.495     -0.221 0.00 0.44  0 0.56
#&gt; TCGA.L5.A8NG.01     1   0.495      0.567 0.56 0.00  0 0.44
#&gt; TCGA.VR.A8EQ.01     3   0.000      1.000 0.00 0.00  1 0.00
#&gt; TCGA.L5.A8NL.01     1   0.495      0.567 0.56 0.00  0 0.44
</code></pre>

<script>
$('#tab-node-0222-get-classes-3-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-3-a').click(function(){
  $('#tab-node-0222-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0222-get-classes-4'>
<p><a id='tab-node-0222-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.R6.A6DN.01     2  0.4263      0.931 0.00 0.76 0.00 0.18 0.06
#&gt; TCGA.L5.A4OG.01     3  0.0000      0.996 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     1  0.0000      0.982 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     3  0.0000      0.996 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     5  0.5700      0.613 0.00 0.12 0.00 0.28 0.60
#&gt; TCGA.M9.A5M8.01     3  0.0609      0.984 0.00 0.02 0.98 0.00 0.00
#&gt; TCGA.L5.A4OW.01     5  0.5700      0.613 0.00 0.12 0.00 0.28 0.60
#&gt; TCGA.2H.A9GK.01     3  0.0000      0.996 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     4  0.1732      0.842 0.00 0.08 0.00 0.92 0.00
#&gt; TCGA.2H.A9GR.01     1  0.0000      0.982 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     5  0.2516      0.844 0.14 0.00 0.00 0.00 0.86
#&gt; TCGA.L5.A8NS.01     5  0.3868      0.845 0.14 0.00 0.00 0.06 0.80
#&gt; TCGA.L5.A893.01     5  0.2280      0.844 0.12 0.00 0.00 0.00 0.88
#&gt; TCGA.JY.A93E.01     1  0.0000      0.982 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     4  0.1732      0.842 0.00 0.08 0.00 0.92 0.00
#&gt; TCGA.2H.A9GL.01     4  0.4854      0.522 0.00 0.26 0.00 0.68 0.06
#&gt; TCGA.L5.A8NM.01     1  0.1043      0.967 0.96 0.04 0.00 0.00 0.00
#&gt; TCGA.L5.A4OX.01     1  0.1648      0.952 0.94 0.04 0.00 0.00 0.02
#&gt; TCGA.L5.A8NR.01     2  0.2929      0.966 0.00 0.82 0.00 0.18 0.00
#&gt; TCGA.JY.A93C.01     2  0.2929      0.966 0.00 0.82 0.00 0.18 0.00
#&gt; TCGA.V5.AASX.01     1  0.0000      0.982 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     4  0.0000      0.782 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NG.01     5  0.3868      0.845 0.14 0.00 0.00 0.06 0.80
#&gt; TCGA.VR.A8EQ.01     3  0.0000      0.996 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NL.01     5  0.2516      0.844 0.14 0.00 0.00 0.00 0.86
</code></pre>

<script>
$('#tab-node-0222-get-classes-4-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-4-a').click(function(){
  $('#tab-node-0222-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0222-get-classes-5'>
<p><a id='tab-node-0222-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.R6.A6DN.01     2  0.2260      0.864 0.00 0.86 0.00 0.00 0.00 0.14
#&gt; TCGA.L5.A4OG.01     3  0.2190      0.934 0.00 0.00 0.90 0.06 0.00 0.04
#&gt; TCGA.L5.A4OE.01     1  0.0937      0.950 0.96 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.R6.A6DQ.01     3  0.0000      0.956 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     6  0.4482      1.000 0.00 0.00 0.00 0.04 0.36 0.60
#&gt; TCGA.M9.A5M8.01     3  0.1092      0.941 0.00 0.00 0.96 0.02 0.00 0.02
#&gt; TCGA.L5.A4OW.01     6  0.4482      1.000 0.00 0.00 0.00 0.04 0.36 0.60
#&gt; TCGA.2H.A9GK.01     3  0.0000      0.956 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     4  0.1556      0.858 0.00 0.08 0.00 0.92 0.00 0.00
#&gt; TCGA.2H.A9GR.01     1  0.0937      0.950 0.96 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.L5.A8NV.01     5  0.0000      0.896 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NS.01     5  0.2094      0.862 0.02 0.00 0.00 0.00 0.90 0.08
#&gt; TCGA.L5.A893.01     5  0.0937      0.857 0.00 0.00 0.00 0.00 0.96 0.04
#&gt; TCGA.JY.A93E.01     1  0.0937      0.950 0.96 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.2H.A9GI.01     4  0.1556      0.858 0.00 0.08 0.00 0.92 0.00 0.00
#&gt; TCGA.2H.A9GL.01     4  0.5144      0.494 0.00 0.34 0.00 0.56 0.00 0.10
#&gt; TCGA.L5.A8NM.01     1  0.1814      0.897 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.L5.A4OX.01     1  0.1814      0.897 0.90 0.00 0.00 0.00 0.00 0.10
#&gt; TCGA.L5.A8NR.01     2  0.0000      0.933 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93C.01     2  0.0000      0.933 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     1  0.0937      0.950 0.96 0.00 0.00 0.00 0.04 0.00
#&gt; TCGA.L5.A8NT.01     4  0.1865      0.836 0.00 0.04 0.00 0.92 0.00 0.04
#&gt; TCGA.L5.A8NG.01     5  0.2094      0.862 0.02 0.00 0.00 0.00 0.90 0.08
#&gt; TCGA.VR.A8EQ.01     3  0.1865      0.942 0.00 0.00 0.92 0.04 0.00 0.04
#&gt; TCGA.L5.A8NL.01     5  0.0000      0.896 0.00 0.00 0.00 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-0222-get-classes-5-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-5-a').click(function(){
  $('#tab-node-0222-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0222-get-classes-6'>
<p><a id='tab-node-0222-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.R6.A6DN.01     7  0.4379      0.823 0.00 0.10 0.00 0.06 0.00 0.10 0.74
#&gt; TCGA.L5.A4OG.01     3  0.3086      0.843 0.00 0.16 0.80 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A4OE.01     1  0.3927      0.857 0.66 0.30 0.00 0.00 0.04 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     3  0.0000      0.941 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     6  0.2376      0.980 0.00 0.00 0.00 0.02 0.12 0.86 0.00
#&gt; TCGA.M9.A5M8.01     3  0.0863      0.933 0.00 0.00 0.96 0.00 0.00 0.04 0.00
#&gt; TCGA.L5.A4OW.01     6  0.2864      0.980 0.00 0.02 0.00 0.02 0.12 0.84 0.00
#&gt; TCGA.2H.A9GK.01     3  0.0000      0.941 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     4  0.0000      0.863 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GR.01     1  0.3927      0.858 0.66 0.30 0.00 0.00 0.04 0.00 0.00
#&gt; TCGA.L5.A8NV.01     5  0.0000      0.824 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     5  0.3370      0.768 0.00 0.16 0.00 0.00 0.78 0.06 0.00
#&gt; TCGA.L5.A893.01     5  0.3000      0.708 0.00 0.10 0.00 0.00 0.84 0.04 0.02
#&gt; TCGA.JY.A93E.01     1  0.3841      0.860 0.68 0.28 0.00 0.00 0.04 0.00 0.00
#&gt; TCGA.2H.A9GI.01     4  0.0000      0.863 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GL.01     4  0.5055      0.464 0.00 0.26 0.00 0.56 0.00 0.00 0.18
#&gt; TCGA.L5.A8NM.01     1  0.0000      0.729 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OX.01     1  0.0000      0.729 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NR.01     7  0.1166      0.913 0.00 0.00 0.00 0.06 0.00 0.00 0.94
#&gt; TCGA.JY.A93C.01     7  0.1166      0.913 0.00 0.00 0.00 0.06 0.00 0.00 0.94
#&gt; TCGA.V5.AASX.01     1  0.4003      0.848 0.64 0.32 0.00 0.00 0.04 0.00 0.00
#&gt; TCGA.L5.A8NT.01     4  0.0000      0.863 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NG.01     5  0.3370      0.768 0.00 0.16 0.00 0.00 0.78 0.06 0.00
#&gt; TCGA.VR.A8EQ.01     3  0.1363      0.930 0.00 0.04 0.94 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A8NL.01     5  0.0000      0.824 0.00 0.00 0.00 0.00 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-0222-get-classes-6-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-6-a').click(function(){
  $('#tab-node-0222-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-0222-get-classes-7'>
<p><a id='tab-node-0222-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.R6.A6DN.01     7  0.3523      0.785 0.00 0.00 0.00 0.00 0.10 0.02 0.78 0.10
#&gt; TCGA.L5.A4OG.01     3  0.4134      0.652 0.00 0.00 0.62 0.30 0.08 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.01     1  0.1607      0.799 0.92 0.00 0.00 0.04 0.04 0.00 0.00 0.00
#&gt; TCGA.R6.A6DQ.01     3  0.0000      0.882 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Y.01     6  0.2071      0.914 0.00 0.02 0.00 0.04 0.04 0.90 0.00 0.00
#&gt; TCGA.M9.A5M8.01     3  0.1341      0.870 0.00 0.00 0.92 0.00 0.08 0.00 0.00 0.00
#&gt; TCGA.L5.A4OW.01     6  0.0471      0.915 0.00 0.02 0.00 0.00 0.00 0.98 0.00 0.00
#&gt; TCGA.2H.A9GK.01     3  0.0000      0.882 0.00 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NW.01     4  0.3318      0.969 0.00 0.00 0.00 0.54 0.00 0.00 0.00 0.46
#&gt; TCGA.2H.A9GR.01     1  0.0000      0.824 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     2  0.0000      0.786 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     2  0.5103      0.680 0.02 0.64 0.00 0.04 0.16 0.14 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.2132      0.723 0.00 0.88 0.00 0.04 0.08 0.00 0.00 0.00
#&gt; TCGA.JY.A93E.01     1  0.0000      0.824 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GI.01     4  0.3318      0.969 0.00 0.00 0.00 0.54 0.00 0.00 0.00 0.46
#&gt; TCGA.2H.A9GL.01     8  0.1765      0.000 0.00 0.00 0.00 0.00 0.00 0.00 0.12 0.88
#&gt; TCGA.L5.A8NM.01     1  0.3193      0.658 0.62 0.00 0.00 0.00 0.38 0.00 0.00 0.00
#&gt; TCGA.L5.A4OX.01     1  0.3193      0.658 0.62 0.00 0.00 0.00 0.38 0.00 0.00 0.00
#&gt; TCGA.L5.A8NR.01     7  0.0000      0.893 0.00 0.00 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.JY.A93C.01     7  0.0000      0.893 0.00 0.00 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.V5.AASX.01     1  0.1275      0.809 0.94 0.00 0.00 0.02 0.04 0.00 0.00 0.00
#&gt; TCGA.L5.A8NT.01     4  0.4004      0.937 0.00 0.00 0.00 0.50 0.04 0.00 0.00 0.46
#&gt; TCGA.L5.A8NG.01     2  0.5103      0.680 0.02 0.64 0.00 0.04 0.16 0.14 0.00 0.00
#&gt; TCGA.VR.A8EQ.01     3  0.2165      0.862 0.00 0.00 0.88 0.06 0.06 0.00 0.00 0.00
#&gt; TCGA.L5.A8NL.01     2  0.0000      0.786 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-0222-get-classes-7-a').parent().next().next().hide();
$('#tab-node-0222-get-classes-7-a').click(function(){
  $('#tab-node-0222-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-0222-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-0222-consensus-heatmap'>
<ul>
<li><a href='#tab-node-0222-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-0222-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-0222-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-0222-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-0222-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-0222-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-0222-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-0222-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-0222-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-0222-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-0222-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-0222-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-0222-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-0222-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-0222-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-0222-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-0222-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-0222-membership-heatmap'>
<ul>
<li><a href='#tab-node-0222-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-0222-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-0222-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-0222-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-0222-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-0222-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-0222-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-0222-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-1-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-1"/></p>

</div>
<div id='tab-node-0222-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-2-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-2"/></p>

</div>
<div id='tab-node-0222-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-3-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-3"/></p>

</div>
<div id='tab-node-0222-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-4-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-4"/></p>

</div>
<div id='tab-node-0222-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-5-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-5"/></p>

</div>
<div id='tab-node-0222-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-6-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-6"/></p>

</div>
<div id='tab-node-0222-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-0222-membership-heatmap-7-1.png" alt="plot of chunk tab-node-0222-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-0222-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-0222-get-signatures'>
<ul>
<li><a href='#tab-node-0222-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-0222-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-0222-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-0222-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-0222-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-0222-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-0222-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-0222-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-1-1.png" alt="plot of chunk tab-node-0222-get-signatures-1"/></p>

</div>
<div id='tab-node-0222-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-2-1.png" alt="plot of chunk tab-node-0222-get-signatures-2"/></p>

</div>
<div id='tab-node-0222-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-3-1.png" alt="plot of chunk tab-node-0222-get-signatures-3"/></p>

</div>
<div id='tab-node-0222-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-4-1.png" alt="plot of chunk tab-node-0222-get-signatures-4"/></p>

</div>
<div id='tab-node-0222-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-5-1.png" alt="plot of chunk tab-node-0222-get-signatures-5"/></p>

</div>
<div id='tab-node-0222-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-6-1.png" alt="plot of chunk tab-node-0222-get-signatures-6"/></p>

</div>
<div id='tab-node-0222-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-0222-get-signatures-7-1.png" alt="plot of chunk tab-node-0222-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-0222-signature_compare](figure_cola/node-0222-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-0222-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-0222-dimension-reduction'>
<ul>
<li><a href='#tab-node-0222-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-0222-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-0222-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-0222-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-0222-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-0222-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-0222-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-0222-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-1-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-1"/></p>

</div>
<div id='tab-node-0222-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-2-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-2"/></p>

</div>
<div id='tab-node-0222-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-3-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-3"/></p>

</div>
<div id='tab-node-0222-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-4-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-4"/></p>

</div>
<div id='tab-node-0222-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-5-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-5"/></p>

</div>
<div id='tab-node-0222-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-6-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-6"/></p>

</div>
<div id='tab-node-0222-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-0222-dimension-reduction-7-1.png" alt="plot of chunk tab-node-0222-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-0222-collect-classes](figure_cola/node-0222-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node02221


Parent node: [Node0222](#Node0222).
Child nodes: 
                Node022211-leaf
        ,
                Node022212-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["02221"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 12 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 5.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-02221-collect-plots](figure_cola/node-02221-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-02221-select-partition-number](figure_cola/node-02221-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           1.000       1.000         0.4854 0.515   0.515
#> 3 3 0.727           0.738       0.847         0.2657 0.955   0.912
#> 4 4 0.818           0.899       0.967         0.2091 0.773   0.516
#> 5 5 0.909           0.799       0.953         0.0832 0.939   0.750
#> 6 6 0.879           0.643       0.882         0.0679 1.000   1.000
#> 7 7 0.864           0.632       0.817         0.0391 0.909   0.500
#> 8 8 0.833           0.558       0.885         0.0360 0.970   0.667
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 5
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-02221-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-02221-get-classes'>
<ul>
<li><a href='#tab-node-02221-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-02221-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-02221-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-02221-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-02221-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-02221-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-02221-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-02221-get-classes-1'>
<p><a id='tab-node-02221-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2
#&gt; TCGA.L5.A4OE.01     2       0          1  0  1
#&gt; TCGA.L5.A88Y.01     2       0          1  0  1
#&gt; TCGA.L5.A4OW.01     2       0          1  0  1
#&gt; TCGA.2H.A9GR.01     1       0          1  1  0
#&gt; TCGA.L5.A8NV.01     1       0          1  1  0
#&gt; TCGA.L5.A8NS.01     1       0          1  1  0
#&gt; TCGA.L5.A893.01     2       0          1  0  1
#&gt; TCGA.JY.A93E.01     1       0          1  1  0
#&gt; TCGA.L5.A8NM.01     1       0          1  1  0
#&gt; TCGA.V5.AASX.01     1       0          1  1  0
#&gt; TCGA.L5.A8NG.01     1       0          1  1  0
#&gt; TCGA.L5.A8NL.01     1       0          1  1  0
</code></pre>

<script>
$('#tab-node-02221-get-classes-1-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-1-a').click(function(){
  $('#tab-node-02221-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02221-get-classes-2'>
<p><a id='tab-node-02221-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3
#&gt; TCGA.L5.A4OE.01     3   0.628      0.000 0.00 0.46 0.54
#&gt; TCGA.L5.A88Y.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.L5.A4OW.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.2H.A9GR.01     1   0.000      0.797 1.00 0.00 0.00
#&gt; TCGA.L5.A8NV.01     1   0.000      0.797 1.00 0.00 0.00
#&gt; TCGA.L5.A8NS.01     1   0.628      0.623 0.54 0.00 0.46
#&gt; TCGA.L5.A893.01     2   0.000      1.000 0.00 1.00 0.00
#&gt; TCGA.JY.A93E.01     1   0.000      0.797 1.00 0.00 0.00
#&gt; TCGA.L5.A8NM.01     1   0.000      0.797 1.00 0.00 0.00
#&gt; TCGA.V5.AASX.01     1   0.628      0.623 0.54 0.00 0.46
#&gt; TCGA.L5.A8NG.01     1   0.000      0.797 1.00 0.00 0.00
#&gt; TCGA.L5.A8NL.01     1   0.628      0.623 0.54 0.00 0.46
</code></pre>

<script>
$('#tab-node-02221-get-classes-2-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-2-a').click(function(){
  $('#tab-node-02221-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02221-get-classes-3'>
<p><a id='tab-node-02221-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2 p3   p4
#&gt; TCGA.L5.A4OE.01     3   0.000      0.000 0.00 0.00  1 0.00
#&gt; TCGA.L5.A88Y.01     2   0.000      0.983 0.00 1.00  0 0.00
#&gt; TCGA.L5.A4OW.01     2   0.000      0.983 0.00 1.00  0 0.00
#&gt; TCGA.2H.A9GR.01     1   0.000      0.983 1.00 0.00  0 0.00
#&gt; TCGA.L5.A8NV.01     1   0.000      0.983 1.00 0.00  0 0.00
#&gt; TCGA.L5.A8NS.01     4   0.234      1.000 0.10 0.00  0 0.90
#&gt; TCGA.L5.A893.01     2   0.121      0.965 0.00 0.96  0 0.04
#&gt; TCGA.JY.A93E.01     1   0.000      0.983 1.00 0.00  0 0.00
#&gt; TCGA.L5.A8NM.01     1   0.000      0.983 1.00 0.00  0 0.00
#&gt; TCGA.V5.AASX.01     4   0.234      1.000 0.10 0.00  0 0.90
#&gt; TCGA.L5.A8NG.01     1   0.164      0.928 0.94 0.00  0 0.06
#&gt; TCGA.L5.A8NL.01     4   0.234      1.000 0.10 0.00  0 0.90
</code></pre>

<script>
$('#tab-node-02221-get-classes-3-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-3-a').click(function(){
  $('#tab-node-02221-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02221-get-classes-4'>
<p><a id='tab-node-02221-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2 p3   p4   p5
#&gt; TCGA.L5.A4OE.01     3   0.000      0.000 0.00 0.00  1 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2   0.000      0.900 0.00 1.00  0 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2   0.000      0.900 0.00 1.00  0 0.00 0.00
#&gt; TCGA.2H.A9GR.01     1   0.000      1.000 1.00 0.00  0 0.00 0.00
#&gt; TCGA.L5.A8NV.01     1   0.000      1.000 1.00 0.00  0 0.00 0.00
#&gt; TCGA.L5.A8NS.01     4   0.141      1.000 0.06 0.00  0 0.94 0.00
#&gt; TCGA.L5.A893.01     2   0.407      0.788 0.00 0.78  0 0.06 0.16
#&gt; TCGA.JY.A93E.01     1   0.000      1.000 1.00 0.00  0 0.00 0.00
#&gt; TCGA.L5.A8NM.01     1   0.000      1.000 1.00 0.00  0 0.00 0.00
#&gt; TCGA.V5.AASX.01     4   0.141      1.000 0.06 0.00  0 0.94 0.00
#&gt; TCGA.L5.A8NG.01     5   0.273      0.000 0.16 0.00  0 0.00 0.84
#&gt; TCGA.L5.A8NL.01     4   0.141      1.000 0.06 0.00  0 0.94 0.00
</code></pre>

<script>
$('#tab-node-02221-get-classes-4-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-4-a').click(function(){
  $('#tab-node-02221-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02221-get-classes-5'>
<p><a id='tab-node-02221-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2 p3  p4   p5   p6
#&gt; TCGA.L5.A4OE.01     3  0.0000      0.000 0.00 0.00  1 0.0 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2  0.0000      0.895 0.00 1.00  0 0.0 0.00 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0547      0.895 0.00 0.98  0 0.0 0.02 0.00
#&gt; TCGA.2H.A9GR.01     1  0.3706      0.733 0.62 0.00  0 0.0 0.00 0.38
#&gt; TCGA.L5.A8NV.01     1  0.3706      0.733 0.62 0.00  0 0.0 0.00 0.38
#&gt; TCGA.L5.A8NS.01     4  0.0000      0.811 0.00 0.00  0 1.0 0.00 0.00
#&gt; TCGA.L5.A893.01     2  0.2941      0.794 0.00 0.78  0 0.0 0.00 0.22
#&gt; TCGA.JY.A93E.01     1  0.0000      0.733 1.00 0.00  0 0.0 0.00 0.00
#&gt; TCGA.L5.A8NM.01     1  0.0000      0.733 1.00 0.00  0 0.0 0.00 0.00
#&gt; TCGA.V5.AASX.01     4  0.3756      0.580 0.00 0.00  0 0.6 0.00 0.40
#&gt; TCGA.L5.A8NG.01     5  0.0547      0.000 0.02 0.00  0 0.0 0.98 0.00
#&gt; TCGA.L5.A8NL.01     4  0.0000      0.811 0.00 0.00  0 1.0 0.00 0.00
</code></pre>

<script>
$('#tab-node-02221-get-classes-5-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-5-a').click(function(){
  $('#tab-node-02221-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02221-get-classes-6'>
<p><a id='tab-node-02221-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2 p3   p4 p5   p6   p7
#&gt; TCGA.L5.A4OE.01     3   0.000      0.000 0.00 0.00  1 0.00  0 0.00 0.00
#&gt; TCGA.L5.A88Y.01     2   0.540      0.688 0.00 0.44  0 0.20  0 0.36 0.00
#&gt; TCGA.L5.A4OW.01     2   0.549      0.688 0.00 0.44  0 0.32  0 0.24 0.00
#&gt; TCGA.2H.A9GR.01     1   0.000      1.000 1.00 0.00  0 0.00  0 0.00 0.00
#&gt; TCGA.L5.A8NV.01     1   0.000      1.000 1.00 0.00  0 0.00  0 0.00 0.00
#&gt; TCGA.L5.A8NS.01     4   0.449      0.900 0.00 0.00  0 0.60  0 0.08 0.32
#&gt; TCGA.L5.A893.01     2   0.000      0.414 0.00 1.00  0 0.00  0 0.00 0.00
#&gt; TCGA.JY.A93E.01     6   0.352      1.000 0.44 0.00  0 0.00  0 0.56 0.00
#&gt; TCGA.L5.A8NM.01     6   0.352      1.000 0.44 0.00  0 0.00  0 0.56 0.00
#&gt; TCGA.V5.AASX.01     7   0.000      0.000 0.00 0.00  0 0.00  0 0.00 1.00
#&gt; TCGA.L5.A8NG.01     5   0.000      0.000 0.00 0.00  0 0.00  1 0.00 0.00
#&gt; TCGA.L5.A8NL.01     4   0.322      0.900 0.00 0.00  0 0.68  0 0.00 0.32
</code></pre>

<script>
$('#tab-node-02221-get-classes-6-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-6-a').click(function(){
  $('#tab-node-02221-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-02221-get-classes-7'>
<p><a id='tab-node-02221-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2 p3   p4 p5   p6  p7   p8
#&gt; TCGA.L5.A4OE.01     3  0.0000      0.000 0.00 0.00  1 0.00  0 0.00 0.0 0.00
#&gt; TCGA.L5.A88Y.01     2  0.3263      0.708 0.12 0.78  0 0.00  0 0.00 0.1 0.00
#&gt; TCGA.L5.A4OW.01     2  0.0000      0.708 0.00 1.00  0 0.00  0 0.00 0.0 0.00
#&gt; TCGA.2H.A9GR.01     1  0.2267      0.892 0.82 0.00  0 0.00  0 0.18 0.0 0.00
#&gt; TCGA.L5.A8NV.01     1  0.3909      0.892 0.70 0.00  0 0.00  0 0.18 0.0 0.12
#&gt; TCGA.L5.A8NS.01     4  0.0000      0.763 0.00 0.00  0 1.00  0 0.00 0.0 0.00
#&gt; TCGA.L5.A893.01     8  0.3015      0.000 0.00 0.32  0 0.00  0 0.00 0.0 0.68
#&gt; TCGA.JY.A93E.01     6  0.0000      0.982 0.00 0.00  0 0.00  0 1.00 0.0 0.00
#&gt; TCGA.L5.A8NM.01     6  0.0471      0.982 0.00 0.00  0 0.00  0 0.98 0.0 0.02
#&gt; TCGA.V5.AASX.01     7  0.1563      0.000 0.00 0.00  0 0.10  0 0.00 0.9 0.00
#&gt; TCGA.L5.A8NG.01     5  0.0000      0.000 0.00 0.00  0 0.00  1 0.00 0.0 0.00
#&gt; TCGA.L5.A8NL.01     4  0.3299      0.763 0.06 0.00  0 0.76  0 0.00 0.0 0.18
</code></pre>

<script>
$('#tab-node-02221-get-classes-7-a').parent().next().next().hide();
$('#tab-node-02221-get-classes-7-a').click(function(){
  $('#tab-node-02221-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-02221-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-02221-consensus-heatmap'>
<ul>
<li><a href='#tab-node-02221-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-02221-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-02221-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-02221-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-02221-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-02221-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-02221-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-02221-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-02221-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-02221-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-02221-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-02221-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-02221-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-02221-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-02221-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-02221-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-02221-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-02221-membership-heatmap'>
<ul>
<li><a href='#tab-node-02221-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-02221-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-02221-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-02221-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-02221-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-02221-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-02221-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-02221-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-1-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-1"/></p>

</div>
<div id='tab-node-02221-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-2-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-2"/></p>

</div>
<div id='tab-node-02221-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-3-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-3"/></p>

</div>
<div id='tab-node-02221-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-4-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-4"/></p>

</div>
<div id='tab-node-02221-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-5-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-5"/></p>

</div>
<div id='tab-node-02221-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-6-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-6"/></p>

</div>
<div id='tab-node-02221-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-02221-membership-heatmap-7-1.png" alt="plot of chunk tab-node-02221-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-02221-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-02221-get-signatures'>
<ul>
<li><a href='#tab-node-02221-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-02221-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-02221-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-02221-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-02221-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-02221-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-02221-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-02221-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-1-1.png" alt="plot of chunk tab-node-02221-get-signatures-1"/></p>

</div>
<div id='tab-node-02221-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-2-1.png" alt="plot of chunk tab-node-02221-get-signatures-2"/></p>

</div>
<div id='tab-node-02221-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-3-1.png" alt="plot of chunk tab-node-02221-get-signatures-3"/></p>

</div>
<div id='tab-node-02221-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-4-1.png" alt="plot of chunk tab-node-02221-get-signatures-4"/></p>

</div>
<div id='tab-node-02221-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-5-1.png" alt="plot of chunk tab-node-02221-get-signatures-5"/></p>

</div>
<div id='tab-node-02221-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-6-1.png" alt="plot of chunk tab-node-02221-get-signatures-6"/></p>

</div>
<div id='tab-node-02221-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-02221-get-signatures-7-1.png" alt="plot of chunk tab-node-02221-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-02221-signature_compare](figure_cola/node-02221-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-02221-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-02221-dimension-reduction'>
<ul>
<li><a href='#tab-node-02221-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-02221-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-02221-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-02221-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-02221-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-02221-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-02221-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-02221-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-1-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-1"/></p>

</div>
<div id='tab-node-02221-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-2-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-2"/></p>

</div>
<div id='tab-node-02221-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-3-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-3"/></p>

</div>
<div id='tab-node-02221-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-4-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-4"/></p>

</div>
<div id='tab-node-02221-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-5-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-5"/></p>

</div>
<div id='tab-node-02221-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-6-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-6"/></p>

</div>
<div id='tab-node-02221-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-02221-dimension-reduction-7-1.png" alt="plot of chunk tab-node-02221-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-02221-collect-classes](figure_cola/node-02221-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node023


Parent node: [Node02](#Node02).
Child nodes: 
                Node0111-leaf
        ,
                Node0112-leaf
        ,
                Node0113-leaf
        ,
                Node0121-leaf
        ,
                Node0122-leaf
        ,
                Node0123-leaf
        ,
                Node0131-leaf
        ,
                Node0132-leaf
        ,
                Node0133-leaf
        ,
                Node0211-leaf
        ,
                Node0212-leaf
        ,
                Node0221-leaf
        ,
                [Node0222](#Node0222)
        ,
                Node0223-leaf
        ,
                Node0231-leaf
        ,
                Node0232-leaf
        ,
                Node0233-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["023"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 14 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-023-collect-plots](figure_cola/node-023-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-023-select-partition-number](figure_cola/node-023-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 0.857           0.917       0.970         0.5343 0.462   0.462
#> 3 3 1.000           1.000       1.000         0.2552 0.868   0.714
#> 4 4 0.945           0.897       0.966         0.0366 0.978   0.933
#> 5 5 0.879           0.815       0.951         0.0759 0.934   0.786
#> 6 6 0.857           0.799       0.901         0.0981 0.912   0.636
#> 7 7 0.813           0.447       0.787         0.0371 0.945   0.667
#> 8 8 0.802           0.436       0.857         0.0472 0.989   0.909
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
```


Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-023-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-023-get-classes'>
<ul>
<li><a href='#tab-node-023-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-023-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-023-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-023-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-023-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-023-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-023-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-023-get-classes-1'>
<p><a id='tab-node-023-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2
#&gt; TCGA.L5.A43I.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A4OH.01     2   0.000      0.927 0.00 1.00
#&gt; TCGA.L5.A4OP.01     2   0.000      0.927 0.00 1.00
#&gt; TCGA.L5.A4OR.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.V5.A7RE.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.V5.A7RE.11     1   0.000      1.000 1.00 0.00
#&gt; TCGA.IG.A4QS.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.L5.A8NH.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.R6.A6XG.01     2   0.000      0.927 0.00 1.00
#&gt; TCGA.R6.A8W8.01     2   0.981      0.276 0.42 0.58
#&gt; TCGA.2H.A9GF.01     2   0.000      0.927 0.00 1.00
#&gt; TCGA.VR.AA4D.01     2   0.000      0.927 0.00 1.00
#&gt; TCGA.2H.A9GM.01     1   0.000      1.000 1.00 0.00
#&gt; TCGA.IC.A6RE.01     2   0.000      0.927 0.00 1.00
</code></pre>

<script>
$('#tab-node-023-get-classes-1-a').parent().next().next().hide();
$('#tab-node-023-get-classes-1-a').click(function(){
  $('#tab-node-023-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-023-get-classes-2'>
<p><a id='tab-node-023-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2 p3
#&gt; TCGA.L5.A43I.01     1       0          1  1  0  0
#&gt; TCGA.L5.A4OH.01     3       0          1  0  0  1
#&gt; TCGA.L5.A4OP.01     2       0          1  0  1  0
#&gt; TCGA.L5.A4OR.01     1       0          1  1  0  0
#&gt; TCGA.V5.A7RE.01     1       0          1  1  0  0
#&gt; TCGA.V5.A7RE.11     1       0          1  1  0  0
#&gt; TCGA.IG.A4QS.01     1       0          1  1  0  0
#&gt; TCGA.L5.A8NH.01     1       0          1  1  0  0
#&gt; TCGA.R6.A6XG.01     2       0          1  0  1  0
#&gt; TCGA.R6.A8W8.01     3       0          1  0  0  1
#&gt; TCGA.2H.A9GF.01     2       0          1  0  1  0
#&gt; TCGA.VR.AA4D.01     2       0          1  0  1  0
#&gt; TCGA.2H.A9GM.01     1       0          1  1  0  0
#&gt; TCGA.IC.A6RE.01     3       0          1  0  0  1
</code></pre>

<script>
$('#tab-node-023-get-classes-2-a').parent().next().next().hide();
$('#tab-node-023-get-classes-2-a').click(function(){
  $('#tab-node-023-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-023-get-classes-3'>
<p><a id='tab-node-023-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1   p2   p3   p4
#&gt; TCGA.L5.A43I.01     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3   0.000      1.000  0 0.00 1.00 0.00
#&gt; TCGA.L5.A4OP.01     2   0.000      0.926  0 1.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.11     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     2   0.361      0.798  0 0.80 0.00 0.20
#&gt; TCGA.R6.A8W8.01     4   0.398      0.000  0 0.00 0.24 0.76
#&gt; TCGA.2H.A9GF.01     2   0.121      0.911  0 0.96 0.00 0.04
#&gt; TCGA.VR.AA4D.01     2   0.000      0.926  0 1.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     1   0.000      1.000  1 0.00 0.00 0.00
#&gt; TCGA.IC.A6RE.01     3   0.000      1.000  0 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-023-get-classes-3-a').parent().next().next().hide();
$('#tab-node-023-get-classes-3-a').click(function(){
  $('#tab-node-023-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-023-get-classes-4'>
<p><a id='tab-node-023-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.L5.A43I.01     1  0.0000      1.000 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.01     3  0.0000      1.000 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     2  0.0000      0.895 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OR.01     1  0.0000      1.000 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     1  0.0000      1.000 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.11     1  0.0000      1.000 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QS.01     1  0.0000      1.000 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     1  0.0000      1.000 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     2  0.3109      0.786 0.00 0.80 0.00 0.00 0.20
#&gt; TCGA.R6.A8W8.01     4  0.0609      0.000 0.00 0.00 0.02 0.98 0.00
#&gt; TCGA.2H.A9GF.01     2  0.2873      0.832 0.00 0.86 0.00 0.02 0.12
#&gt; TCGA.VR.AA4D.01     2  0.0000      0.895 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     5  0.3895      0.000 0.32 0.00 0.00 0.00 0.68
#&gt; TCGA.IC.A6RE.01     3  0.0000      1.000 0.00 0.00 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-023-get-classes-4-a').parent().next().next().hide();
$('#tab-node-023-get-classes-4-a').click(function(){
  $('#tab-node-023-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-023-get-classes-5'>
<p><a id='tab-node-023-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.L5.A43I.01     1  0.3797      1.000 0.58 0.00 0.00 0.00 0.00 0.42
#&gt; TCGA.L5.A4OH.01     3  0.0000      1.000 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     2  0.0547      0.854 0.00 0.98 0.00 0.02 0.00 0.00
#&gt; TCGA.L5.A4OR.01     1  0.3797      1.000 0.58 0.00 0.00 0.00 0.00 0.42
#&gt; TCGA.V5.A7RE.01     6  0.0000      1.000 0.00 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.V5.A7RE.11     6  0.0000      1.000 0.00 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.IG.A4QS.01     1  0.3797      1.000 0.58 0.00 0.00 0.00 0.00 0.42
#&gt; TCGA.L5.A8NH.01     1  0.3797      1.000 0.58 0.00 0.00 0.00 0.00 0.42
#&gt; TCGA.R6.A6XG.01     2  0.3679      0.733 0.20 0.76 0.00 0.00 0.04 0.00
#&gt; TCGA.R6.A8W8.01     4  0.0547      0.000 0.00 0.00 0.02 0.98 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.2941      0.749 0.22 0.78 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA4D.01     2  0.0000      0.854 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     5  0.0937      0.000 0.00 0.00 0.00 0.00 0.96 0.04
#&gt; TCGA.IC.A6RE.01     3  0.0000      1.000 0.00 0.00 1.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-023-get-classes-5-a').parent().next().next().hide();
$('#tab-node-023-get-classes-5-a').click(function(){
  $('#tab-node-023-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-023-get-classes-6'>
<p><a id='tab-node-023-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3 p4   p5   p6   p7
#&gt; TCGA.L5.A43I.01     1  0.2259      0.709 0.84 0.00 0.00  0 0.00 0.00 0.16
#&gt; TCGA.L5.A4OH.01     3  0.1363      0.950 0.00 0.00 0.94  0 0.02 0.00 0.04
#&gt; TCGA.L5.A4OP.01     2  0.0863      0.766 0.00 0.96 0.00  0 0.04 0.00 0.00
#&gt; TCGA.L5.A4OR.01     1  0.0000      0.918 1.00 0.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     6  0.5589     -0.766 0.32 0.00 0.00  0 0.00 0.40 0.28
#&gt; TCGA.V5.A7RE.11     7  0.4850      0.000 0.32 0.00 0.00  0 0.00 0.12 0.56
#&gt; TCGA.IG.A4QS.01     1  0.0000      0.918 1.00 0.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     1  0.0000      0.918 1.00 0.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     6  0.3459     -0.418 0.00 0.40 0.00  0 0.00 0.60 0.00
#&gt; TCGA.R6.A8W8.01     4  0.0000      0.000 0.00 0.00 0.00  1 0.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2  0.3459      0.544 0.00 0.60 0.00  0 0.00 0.00 0.40
#&gt; TCGA.VR.AA4D.01     2  0.0000      0.766 0.00 1.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     5  0.1166      0.000 0.06 0.00 0.00  0 0.94 0.00 0.00
#&gt; TCGA.IC.A6RE.01     3  0.0000      0.950 0.00 0.00 1.00  0 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-023-get-classes-6-a').parent().next().next().hide();
$('#tab-node-023-get-classes-6-a').click(function(){
  $('#tab-node-023-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-023-get-classes-7'>
<p><a id='tab-node-023-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2  p3 p4 p5   p6   p7   p8
#&gt; TCGA.L5.A43I.01     1   0.507      0.287 0.56 0.00 0.0  0  0 0.02 0.24 0.18
#&gt; TCGA.L5.A4OH.01     3   0.000      0.916 0.00 0.00 1.0  0  0 0.00 0.00 0.00
#&gt; TCGA.L5.A4OP.01     2   0.134      0.597 0.00 0.92 0.0  0  0 0.00 0.08 0.00
#&gt; TCGA.L5.A4OR.01     1   0.000      0.836 1.00 0.00 0.0  0  0 0.00 0.00 0.00
#&gt; TCGA.V5.A7RE.01     6   0.448      0.000 0.10 0.00 0.0  0  0 0.54 0.36 0.00
#&gt; TCGA.V5.A7RE.11     7   0.156      0.000 0.10 0.00 0.0  0  0 0.00 0.90 0.00
#&gt; TCGA.IG.A4QS.01     1   0.000      0.836 1.00 0.00 0.0  0  0 0.00 0.00 0.00
#&gt; TCGA.L5.A8NH.01     1   0.000      0.836 1.00 0.00 0.0  0  0 0.00 0.00 0.00
#&gt; TCGA.R6.A6XG.01     8   0.301      0.000 0.00 0.32 0.0  0  0 0.00 0.00 0.68
#&gt; TCGA.R6.A8W8.01     4   0.000      0.000 0.00 0.00 0.0  1  0 0.00 0.00 0.00
#&gt; TCGA.2H.A9GF.01     2   0.454      0.283 0.00 0.50 0.0  0  0 0.40 0.00 0.10
#&gt; TCGA.VR.AA4D.01     2   0.000      0.597 0.00 1.00 0.0  0  0 0.00 0.00 0.00
#&gt; TCGA.2H.A9GM.01     5   0.000      0.000 0.00 0.00 0.0  0  1 0.00 0.00 0.00
#&gt; TCGA.IC.A6RE.01     3   0.207      0.916 0.00 0.00 0.9  0  0 0.04 0.02 0.04
</code></pre>

<script>
$('#tab-node-023-get-classes-7-a').parent().next().next().hide();
$('#tab-node-023-get-classes-7-a').click(function(){
  $('#tab-node-023-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-023-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-023-consensus-heatmap'>
<ul>
<li><a href='#tab-node-023-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-023-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-023-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-023-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-023-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-023-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-023-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-023-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-023-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-023-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-023-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-023-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-023-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-023-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-023-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-023-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-023-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-023-membership-heatmap'>
<ul>
<li><a href='#tab-node-023-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-023-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-023-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-023-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-023-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-023-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-023-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-023-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-1-1.png" alt="plot of chunk tab-node-023-membership-heatmap-1"/></p>

</div>
<div id='tab-node-023-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-2-1.png" alt="plot of chunk tab-node-023-membership-heatmap-2"/></p>

</div>
<div id='tab-node-023-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-3-1.png" alt="plot of chunk tab-node-023-membership-heatmap-3"/></p>

</div>
<div id='tab-node-023-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-4-1.png" alt="plot of chunk tab-node-023-membership-heatmap-4"/></p>

</div>
<div id='tab-node-023-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-5-1.png" alt="plot of chunk tab-node-023-membership-heatmap-5"/></p>

</div>
<div id='tab-node-023-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-6-1.png" alt="plot of chunk tab-node-023-membership-heatmap-6"/></p>

</div>
<div id='tab-node-023-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-023-membership-heatmap-7-1.png" alt="plot of chunk tab-node-023-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-023-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-023-get-signatures'>
<ul>
<li><a href='#tab-node-023-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-023-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-023-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-023-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-023-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-023-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-023-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-023-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-1-1.png" alt="plot of chunk tab-node-023-get-signatures-1"/></p>

</div>
<div id='tab-node-023-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-2-1.png" alt="plot of chunk tab-node-023-get-signatures-2"/></p>

</div>
<div id='tab-node-023-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-3-1.png" alt="plot of chunk tab-node-023-get-signatures-3"/></p>

</div>
<div id='tab-node-023-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-4-1.png" alt="plot of chunk tab-node-023-get-signatures-4"/></p>

</div>
<div id='tab-node-023-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-5-1.png" alt="plot of chunk tab-node-023-get-signatures-5"/></p>

</div>
<div id='tab-node-023-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-6-1.png" alt="plot of chunk tab-node-023-get-signatures-6"/></p>

</div>
<div id='tab-node-023-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-023-get-signatures-7-1.png" alt="plot of chunk tab-node-023-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-023-signature_compare](figure_cola/node-023-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-023-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-023-dimension-reduction'>
<ul>
<li><a href='#tab-node-023-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-023-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-023-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-023-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-023-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-023-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-023-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-023-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-1-1.png" alt="plot of chunk tab-node-023-dimension-reduction-1"/></p>

</div>
<div id='tab-node-023-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-2-1.png" alt="plot of chunk tab-node-023-dimension-reduction-2"/></p>

</div>
<div id='tab-node-023-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-3-1.png" alt="plot of chunk tab-node-023-dimension-reduction-3"/></p>

</div>
<div id='tab-node-023-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-4-1.png" alt="plot of chunk tab-node-023-dimension-reduction-4"/></p>

</div>
<div id='tab-node-023-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-5-1.png" alt="plot of chunk tab-node-023-dimension-reduction-5"/></p>

</div>
<div id='tab-node-023-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-6-1.png" alt="plot of chunk tab-node-023-dimension-reduction-6"/></p>

</div>
<div id='tab-node-023-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-023-dimension-reduction-7-1.png" alt="plot of chunk tab-node-023-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-023-collect-classes](figure_cola/node-023-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node03


Parent node: [Node0](#Node0).
Child nodes: 
                [Node011](#Node011)
        ,
                [Node012](#Node012)
        ,
                [Node013](#Node013)
        ,
                [Node021](#Node021)
        ,
                [Node022](#Node022)
        ,
                [Node023](#Node023)
        ,
                Node031-leaf
        ,
                Node032-leaf
        ,
                Node033-leaf
        ,
                Node034-leaf
        ,
                Node035-leaf
        ,
                Node041-leaf
        ,
                Node042-leaf
        ,
                Node043-leaf
        ,
                Node051-leaf
        ,
                Node052-leaf
        ,
                Node053-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["03"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 20 columns.
#>   Top rows (1000) are extracted by 'SD' method.
#>   Subgroups are detected by 'skmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 5.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-03-collect-plots](figure_cola/node-03-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-03-select-partition-number](figure_cola/node-03-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           1.000       1.000         0.5215 0.479   0.479
#> 3 3 1.000           1.000       1.000         0.2016 0.895   0.780
#> 4 4 1.000           1.000       1.000         0.2349 0.853   0.606
#> 5 5 0.932           0.968       0.971         0.0661 0.947   0.767
#> 6 6 0.926           0.884       0.950         0.0285 0.979   0.879
#> 7 7 0.921           0.835       0.945         0.0229 0.984   0.897
#> 8 8 0.900           0.759       0.928         0.0236 0.979   0.846
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 5
#> attr(,"optional")
#> [1] 2 3 4
```

There is also optional best $k$ = 2 3 4 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-03-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-03-get-classes'>
<ul>
<li><a href='#tab-node-03-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-03-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-03-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-03-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-03-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-03-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-03-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-03-get-classes-1'>
<p><a id='tab-node-03-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2
#&gt; TCGA.Z6.AAPN.01     2       0          1  0  1
#&gt; TCGA.L5.A43C.11     1       0          1  1  0
#&gt; TCGA.VR.A8ET.01     2       0          1  0  1
#&gt; TCGA.L5.A4OH.11     1       0          1  1  0
#&gt; TCGA.L5.A4OE.11     1       0          1  1  0
#&gt; TCGA.L5.A88T.01     2       0          1  0  1
#&gt; TCGA.L5.A4ON.11     2       0          1  0  1
#&gt; TCGA.L5.A4OQ.11     2       0          1  0  1
#&gt; TCGA.L5.A4OI.11     1       0          1  1  0
#&gt; TCGA.IG.A4QT.01     2       0          1  0  1
#&gt; TCGA.L5.A4OF.11     1       0          1  1  0
#&gt; TCGA.L5.A4OJ.11     1       0          1  1  0
#&gt; TCGA.L5.A4OM.11     1       0          1  1  0
#&gt; TCGA.L5.A4OP.11     1       0          1  1  0
#&gt; TCGA.IG.A3I8.11     2       0          1  0  1
#&gt; TCGA.L5.A4OG.11     1       0          1  1  0
#&gt; TCGA.IG.A7DP.01     2       0          1  0  1
#&gt; TCGA.LN.A9FP.01     2       0          1  0  1
#&gt; TCGA.IC.A6RE.11     2       0          1  0  1
#&gt; TCGA.L5.A4OS.01     2       0          1  0  1
</code></pre>

<script>
$('#tab-node-03-get-classes-1-a').parent().next().next().hide();
$('#tab-node-03-get-classes-1-a').click(function(){
  $('#tab-node-03-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-03-get-classes-2'>
<p><a id='tab-node-03-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2 p3
#&gt; TCGA.Z6.AAPN.01     2       0          1  0  1  0
#&gt; TCGA.L5.A43C.11     1       0          1  1  0  0
#&gt; TCGA.VR.A8ET.01     2       0          1  0  1  0
#&gt; TCGA.L5.A4OH.11     1       0          1  1  0  0
#&gt; TCGA.L5.A4OE.11     1       0          1  1  0  0
#&gt; TCGA.L5.A88T.01     2       0          1  0  1  0
#&gt; TCGA.L5.A4ON.11     2       0          1  0  1  0
#&gt; TCGA.L5.A4OQ.11     2       0          1  0  1  0
#&gt; TCGA.L5.A4OI.11     1       0          1  1  0  0
#&gt; TCGA.IG.A4QT.01     2       0          1  0  1  0
#&gt; TCGA.L5.A4OF.11     1       0          1  1  0  0
#&gt; TCGA.L5.A4OJ.11     3       0          1  0  0  1
#&gt; TCGA.L5.A4OM.11     3       0          1  0  0  1
#&gt; TCGA.L5.A4OP.11     3       0          1  0  0  1
#&gt; TCGA.IG.A3I8.11     2       0          1  0  1  0
#&gt; TCGA.L5.A4OG.11     3       0          1  0  0  1
#&gt; TCGA.IG.A7DP.01     2       0          1  0  1  0
#&gt; TCGA.LN.A9FP.01     2       0          1  0  1  0
#&gt; TCGA.IC.A6RE.11     2       0          1  0  1  0
#&gt; TCGA.L5.A4OS.01     2       0          1  0  1  0
</code></pre>

<script>
$('#tab-node-03-get-classes-2-a').parent().next().next().hide();
$('#tab-node-03-get-classes-2-a').click(function(){
  $('#tab-node-03-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-03-get-classes-3'>
<p><a id='tab-node-03-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2 p3 p4
#&gt; TCGA.Z6.AAPN.01     2       0          1  0  1  0  0
#&gt; TCGA.L5.A43C.11     1       0          1  1  0  0  0
#&gt; TCGA.VR.A8ET.01     2       0          1  0  1  0  0
#&gt; TCGA.L5.A4OH.11     1       0          1  1  0  0  0
#&gt; TCGA.L5.A4OE.11     1       0          1  1  0  0  0
#&gt; TCGA.L5.A88T.01     2       0          1  0  1  0  0
#&gt; TCGA.L5.A4ON.11     2       0          1  0  1  0  0
#&gt; TCGA.L5.A4OQ.11     2       0          1  0  1  0  0
#&gt; TCGA.L5.A4OI.11     1       0          1  1  0  0  0
#&gt; TCGA.IG.A4QT.01     2       0          1  0  1  0  0
#&gt; TCGA.L5.A4OF.11     1       0          1  1  0  0  0
#&gt; TCGA.L5.A4OJ.11     3       0          1  0  0  1  0
#&gt; TCGA.L5.A4OM.11     3       0          1  0  0  1  0
#&gt; TCGA.L5.A4OP.11     3       0          1  0  0  1  0
#&gt; TCGA.IG.A3I8.11     4       0          1  0  0  0  1
#&gt; TCGA.L5.A4OG.11     3       0          1  0  0  1  0
#&gt; TCGA.IG.A7DP.01     4       0          1  0  0  0  1
#&gt; TCGA.LN.A9FP.01     4       0          1  0  0  0  1
#&gt; TCGA.IC.A6RE.11     2       0          1  0  1  0  0
#&gt; TCGA.L5.A4OS.01     4       0          1  0  0  0  1
</code></pre>

<script>
$('#tab-node-03-get-classes-3-a').parent().next().next().hide();
$('#tab-node-03-get-classes-3-a').click(function(){
  $('#tab-node-03-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-03-get-classes-4'>
<p><a id='tab-node-03-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1   p2   p3   p4   p5
#&gt; TCGA.Z6.AAPN.01     2  0.2516      0.883  0 0.86 0.00 0.00 0.14
#&gt; TCGA.L5.A43C.11     1  0.0000      1.000  1 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8ET.01     2  0.2020      0.912  0 0.90 0.00 0.00 0.10
#&gt; TCGA.L5.A4OH.11     1  0.0000      1.000  1 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.11     1  0.0000      1.000  1 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88T.01     5  0.1410      0.975  0 0.06 0.00 0.00 0.94
#&gt; TCGA.L5.A4ON.11     2  0.0609      0.896  0 0.98 0.00 0.00 0.02
#&gt; TCGA.L5.A4OQ.11     2  0.1043      0.883  0 0.96 0.00 0.00 0.04
#&gt; TCGA.L5.A4OI.11     1  0.0000      1.000  1 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QT.01     2  0.1732      0.917  0 0.92 0.00 0.00 0.08
#&gt; TCGA.L5.A4OF.11     1  0.0000      1.000  1 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.11     3  0.0000      0.995  0 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A4OM.11     3  0.0609      0.984  0 0.00 0.98 0.00 0.02
#&gt; TCGA.L5.A4OP.11     3  0.0000      0.995  0 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     4  0.0609      0.989  0 0.00 0.00 0.98 0.02
#&gt; TCGA.L5.A4OG.11     3  0.0000      0.995  0 0.00 1.00 0.00 0.00
#&gt; TCGA.IG.A7DP.01     4  0.0000      0.989  0 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A9FP.01     4  0.0609      0.989  0 0.00 0.00 0.98 0.02
#&gt; TCGA.IC.A6RE.11     5  0.1732      0.975  0 0.08 0.00 0.00 0.92
#&gt; TCGA.L5.A4OS.01     4  0.0000      0.989  0 0.00 0.00 1.00 0.00
</code></pre>

<script>
$('#tab-node-03-get-classes-4-a').parent().next().next().hide();
$('#tab-node-03-get-classes-4-a').click(function(){
  $('#tab-node-03-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-03-get-classes-5'>
<p><a id='tab-node-03-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.Z6.AAPN.01     2  0.0000      0.904 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.11     1  0.0547      0.968 0.98 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.VR.A8ET.01     2  0.0000      0.904 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.11     1  0.0000      0.974 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OE.11     1  0.2094      0.915 0.90 0.00 0.00 0.00 0.02 0.08
#&gt; TCGA.L5.A88T.01     5  0.0937      0.970 0.00 0.04 0.00 0.00 0.96 0.00
#&gt; TCGA.L5.A4ON.11     2  0.2793      0.642 0.00 0.80 0.00 0.00 0.00 0.20
#&gt; TCGA.L5.A4OQ.11     6  0.3592      0.000 0.00 0.24 0.00 0.00 0.02 0.74
#&gt; TCGA.L5.A4OI.11     1  0.0000      0.974 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IG.A4QT.01     2  0.0000      0.904 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OF.11     1  0.0000      0.974 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OJ.11     3  0.0000      0.977 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.11     3  0.1556      0.928 0.00 0.00 0.92 0.00 0.00 0.08
#&gt; TCGA.L5.A4OP.11     3  0.0000      0.977 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     4  0.2350      0.928 0.00 0.00 0.00 0.88 0.02 0.10
#&gt; TCGA.L5.A4OG.11     3  0.0000      0.977 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A7DP.01     4  0.0000      0.928 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.LN.A9FP.01     4  0.2350      0.928 0.00 0.00 0.00 0.88 0.02 0.10
#&gt; TCGA.IC.A6RE.11     5  0.1267      0.970 0.00 0.06 0.00 0.00 0.94 0.00
#&gt; TCGA.L5.A4OS.01     4  0.0000      0.928 0.00 0.00 0.00 1.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-03-get-classes-5-a').parent().next().next().hide();
$('#tab-node-03-get-classes-5-a').click(function(){
  $('#tab-node-03-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-03-get-classes-6'>
<p><a id='tab-node-03-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3  p4 p5   p6   p7
#&gt; TCGA.Z6.AAPN.01     2  0.0000      0.893 0.00 1.00 0.00 0.0  0 0.00 0.00
#&gt; TCGA.L5.A43C.11     1  0.0504      0.944 0.98 0.00 0.00 0.0  0 0.00 0.02
#&gt; TCGA.VR.A8ET.01     2  0.0000      0.893 0.00 1.00 0.00 0.0  0 0.00 0.00
#&gt; TCGA.L5.A4OH.11     1  0.0504      0.944 0.98 0.00 0.00 0.0  0 0.00 0.02
#&gt; TCGA.L5.A4OE.11     1  0.2259      0.830 0.84 0.00 0.00 0.0  0 0.00 0.16
#&gt; TCGA.L5.A88T.01     5  0.0000      1.000 0.00 0.00 0.00 0.0  1 0.00 0.00
#&gt; TCGA.L5.A4ON.11     2  0.3637      0.661 0.00 0.72 0.00 0.0  0 0.24 0.04
#&gt; TCGA.L5.A4OQ.11     6  0.0000      0.000 0.00 0.00 0.00 0.0  0 1.00 0.00
#&gt; TCGA.L5.A4OI.11     1  0.0504      0.944 0.98 0.00 0.00 0.0  0 0.00 0.02
#&gt; TCGA.IG.A4QT.01     2  0.0863      0.886 0.00 0.96 0.00 0.0  0 0.00 0.04
#&gt; TCGA.L5.A4OF.11     1  0.0504      0.944 0.98 0.00 0.00 0.0  0 0.00 0.02
#&gt; TCGA.L5.A4OJ.11     3  0.0000      1.000 0.00 0.00 1.00 0.0  0 0.00 0.00
#&gt; TCGA.L5.A4OM.11     7  0.3294      0.000 0.00 0.00 0.34 0.0  0 0.00 0.66
#&gt; TCGA.L5.A4OP.11     3  0.0000      1.000 0.00 0.00 1.00 0.0  0 0.00 0.00
#&gt; TCGA.IG.A3I8.11     4  0.1671      0.938 0.00 0.00 0.00 0.9  0 0.00 0.10
#&gt; TCGA.L5.A4OG.11     3  0.0000      1.000 0.00 0.00 1.00 0.0  0 0.00 0.00
#&gt; TCGA.IG.A7DP.01     4  0.0000      0.938 0.00 0.00 0.00 1.0  0 0.00 0.00
#&gt; TCGA.LN.A9FP.01     4  0.1671      0.938 0.00 0.00 0.00 0.9  0 0.00 0.10
#&gt; TCGA.IC.A6RE.11     5  0.0000      1.000 0.00 0.00 0.00 0.0  1 0.00 0.00
#&gt; TCGA.L5.A4OS.01     4  0.0000      0.938 0.00 0.00 0.00 1.0  0 0.00 0.00
</code></pre>

<script>
$('#tab-node-03-get-classes-6-a').parent().next().next().hide();
$('#tab-node-03-get-classes-6-a').click(function(){
  $('#tab-node-03-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-03-get-classes-7'>
<p><a id='tab-node-03-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4 p5   p6   p7   p8
#&gt; TCGA.Z6.AAPN.01     2  0.0000      0.931 0.00 1.00 0.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.L5.A43C.11     1  0.1563      0.804 0.90 0.00 0.00 0.00  0 0.00 0.00 0.10
#&gt; TCGA.VR.A8ET.01     2  0.0000      0.931 0.00 1.00 0.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.L5.A4OH.11     1  0.1887      0.866 0.90 0.00 0.00 0.00  0 0.00 0.04 0.06
#&gt; TCGA.L5.A4OE.11     8  0.2267      0.000 0.18 0.00 0.00 0.00  0 0.00 0.00 0.82
#&gt; TCGA.L5.A88T.01     5  0.0000      1.000 0.00 0.00 0.00 0.00  1 0.00 0.00 0.00
#&gt; TCGA.L5.A4ON.11     2  0.2267      0.795 0.00 0.82 0.00 0.00  0 0.18 0.00 0.00
#&gt; TCGA.L5.A4OQ.11     6  0.0000      0.000 0.00 0.00 0.00 0.00  0 1.00 0.00 0.00
#&gt; TCGA.L5.A4OI.11     1  0.0941      0.849 0.96 0.00 0.00 0.00  0 0.00 0.02 0.02
#&gt; TCGA.IG.A4QT.01     2  0.0471      0.928 0.00 0.98 0.00 0.00  0 0.02 0.00 0.00
#&gt; TCGA.L5.A4OF.11     1  0.1887      0.866 0.90 0.00 0.00 0.00  0 0.00 0.04 0.06
#&gt; TCGA.L5.A4OJ.11     3  0.0000      0.976 0.00 0.00 1.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.L5.A4OM.11     7  0.2114      0.000 0.00 0.00 0.16 0.00  0 0.00 0.84 0.00
#&gt; TCGA.L5.A4OP.11     3  0.0000      0.976 0.00 0.00 1.00 0.00  0 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.11     4  0.3528      0.824 0.00 0.00 0.00 0.74  0 0.00 0.08 0.18
#&gt; TCGA.L5.A4OG.11     3  0.0808      0.950 0.00 0.00 0.96 0.00  0 0.00 0.04 0.00
#&gt; TCGA.IG.A7DP.01     4  0.0000      0.832 0.00 0.00 0.00 1.00  0 0.00 0.00 0.00
#&gt; TCGA.LN.A9FP.01     4  0.3385      0.832 0.00 0.00 0.00 0.76  0 0.00 0.08 0.16
#&gt; TCGA.IC.A6RE.11     5  0.0000      1.000 0.00 0.00 0.00 0.00  1 0.00 0.00 0.00
#&gt; TCGA.L5.A4OS.01     4  0.0471      0.824 0.00 0.00 0.00 0.98  0 0.00 0.02 0.00
</code></pre>

<script>
$('#tab-node-03-get-classes-7-a').parent().next().next().hide();
$('#tab-node-03-get-classes-7-a').click(function(){
  $('#tab-node-03-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-03-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-03-consensus-heatmap'>
<ul>
<li><a href='#tab-node-03-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-03-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-03-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-03-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-03-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-03-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-03-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-03-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-03-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-03-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-03-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-03-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-03-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-03-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-03-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-03-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-03-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-03-membership-heatmap'>
<ul>
<li><a href='#tab-node-03-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-03-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-03-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-03-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-03-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-03-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-03-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-03-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-1-1.png" alt="plot of chunk tab-node-03-membership-heatmap-1"/></p>

</div>
<div id='tab-node-03-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-2-1.png" alt="plot of chunk tab-node-03-membership-heatmap-2"/></p>

</div>
<div id='tab-node-03-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-3-1.png" alt="plot of chunk tab-node-03-membership-heatmap-3"/></p>

</div>
<div id='tab-node-03-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-4-1.png" alt="plot of chunk tab-node-03-membership-heatmap-4"/></p>

</div>
<div id='tab-node-03-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-5-1.png" alt="plot of chunk tab-node-03-membership-heatmap-5"/></p>

</div>
<div id='tab-node-03-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-6-1.png" alt="plot of chunk tab-node-03-membership-heatmap-6"/></p>

</div>
<div id='tab-node-03-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-03-membership-heatmap-7-1.png" alt="plot of chunk tab-node-03-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-03-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-03-get-signatures'>
<ul>
<li><a href='#tab-node-03-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-03-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-03-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-03-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-03-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-03-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-03-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-03-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-1-1.png" alt="plot of chunk tab-node-03-get-signatures-1"/></p>

</div>
<div id='tab-node-03-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-2-1.png" alt="plot of chunk tab-node-03-get-signatures-2"/></p>

</div>
<div id='tab-node-03-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-3-1.png" alt="plot of chunk tab-node-03-get-signatures-3"/></p>

</div>
<div id='tab-node-03-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-4-1.png" alt="plot of chunk tab-node-03-get-signatures-4"/></p>

</div>
<div id='tab-node-03-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-5-1.png" alt="plot of chunk tab-node-03-get-signatures-5"/></p>

</div>
<div id='tab-node-03-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-6-1.png" alt="plot of chunk tab-node-03-get-signatures-6"/></p>

</div>
<div id='tab-node-03-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-03-get-signatures-7-1.png" alt="plot of chunk tab-node-03-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-03-signature_compare](figure_cola/node-03-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-03-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-03-dimension-reduction'>
<ul>
<li><a href='#tab-node-03-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-03-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-03-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-03-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-03-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-03-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-03-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-03-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-1-1.png" alt="plot of chunk tab-node-03-dimension-reduction-1"/></p>

</div>
<div id='tab-node-03-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-2-1.png" alt="plot of chunk tab-node-03-dimension-reduction-2"/></p>

</div>
<div id='tab-node-03-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-3-1.png" alt="plot of chunk tab-node-03-dimension-reduction-3"/></p>

</div>
<div id='tab-node-03-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-4-1.png" alt="plot of chunk tab-node-03-dimension-reduction-4"/></p>

</div>
<div id='tab-node-03-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-5-1.png" alt="plot of chunk tab-node-03-dimension-reduction-5"/></p>

</div>
<div id='tab-node-03-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-6-1.png" alt="plot of chunk tab-node-03-dimension-reduction-6"/></p>

</div>
<div id='tab-node-03-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-03-dimension-reduction-7-1.png" alt="plot of chunk tab-node-03-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-03-collect-classes](figure_cola/node-03-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node04


Parent node: [Node0](#Node0).
Child nodes: 
                [Node011](#Node011)
        ,
                [Node012](#Node012)
        ,
                [Node013](#Node013)
        ,
                [Node021](#Node021)
        ,
                [Node022](#Node022)
        ,
                [Node023](#Node023)
        ,
                Node031-leaf
        ,
                Node032-leaf
        ,
                Node033-leaf
        ,
                Node034-leaf
        ,
                Node035-leaf
        ,
                Node041-leaf
        ,
                Node042-leaf
        ,
                Node043-leaf
        ,
                Node051-leaf
        ,
                Node052-leaf
        ,
                Node053-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["04"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 14 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-04-collect-plots](figure_cola/node-04-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-04-select-partition-number](figure_cola/node-04-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 0.505           0.793       0.857         0.4731 0.505   0.505
#> 3 3 1.000           1.000       1.000         0.4873 0.681   0.431
#> 4 4 0.802           0.427       0.701         0.1029 0.791   0.457
#> 5 5 0.835           0.874       0.863         0.0629 0.758   0.267
#> 6 6 0.824           0.767       0.854         0.0423 0.967   0.786
#> 7 7 0.824           0.738       0.871         0.0363 1.000   1.000
#> 8 8 0.846           0.409       0.767         0.0212 0.956   0.636
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
```


Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-04-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-04-get-classes'>
<ul>
<li><a href='#tab-node-04-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-04-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-04-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-04-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-04-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-04-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-04-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-04-get-classes-1'>
<p><a id='tab-node-04-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette  p1  p2
#&gt; TCGA.L5.A43M.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.L5.A4OQ.01     2   0.971      0.667 0.4 0.6
#&gt; TCGA.R6.A8W5.01     2   0.971      0.667 0.4 0.6
#&gt; TCGA.L5.A8NE.01     2   0.971      0.667 0.4 0.6
#&gt; TCGA.JY.A6FH.01     2   0.971      0.667 0.4 0.6
#&gt; TCGA.VR.A8Q7.01     2   0.000      0.692 0.0 1.0
#&gt; TCGA.R6.A6Y0.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.L5.A891.01     2   0.000      0.692 0.0 1.0
#&gt; TCGA.2H.A9GJ.01     2   0.000      0.692 0.0 1.0
#&gt; TCGA.2H.A9GN.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.2H.A9GG.01     1   0.000      1.000 1.0 0.0
#&gt; TCGA.2H.A9GQ.01     2   0.000      0.692 0.0 1.0
#&gt; TCGA.L5.A8NF.01     2   0.971      0.667 0.4 0.6
#&gt; TCGA.L5.A8NI.01     1   0.000      1.000 1.0 0.0
</code></pre>

<script>
$('#tab-node-04-get-classes-1-a').parent().next().next().hide();
$('#tab-node-04-get-classes-1-a').click(function(){
  $('#tab-node-04-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-04-get-classes-2'>
<p><a id='tab-node-04-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2 p3
#&gt; TCGA.L5.A43M.01     1       0          1  1  0  0
#&gt; TCGA.L5.A4OQ.01     2       0          1  0  1  0
#&gt; TCGA.R6.A8W5.01     2       0          1  0  1  0
#&gt; TCGA.L5.A8NE.01     2       0          1  0  1  0
#&gt; TCGA.JY.A6FH.01     2       0          1  0  1  0
#&gt; TCGA.VR.A8Q7.01     3       0          1  0  0  1
#&gt; TCGA.R6.A6Y0.01     2       0          1  0  1  0
#&gt; TCGA.L5.A891.01     3       0          1  0  0  1
#&gt; TCGA.2H.A9GJ.01     3       0          1  0  0  1
#&gt; TCGA.2H.A9GN.01     1       0          1  1  0  0
#&gt; TCGA.2H.A9GG.01     1       0          1  1  0  0
#&gt; TCGA.2H.A9GQ.01     3       0          1  0  0  1
#&gt; TCGA.L5.A8NF.01     2       0          1  0  1  0
#&gt; TCGA.L5.A8NI.01     1       0          1  1  0  0
</code></pre>

<script>
$('#tab-node-04-get-classes-2-a').parent().next().next().hide();
$('#tab-node-04-get-classes-2-a').click(function(){
  $('#tab-node-04-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-04-get-classes-3'>
<p><a id='tab-node-04-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.L5.A43M.01     1   0.491      0.489 0.58 0.00 0.42 0.00
#&gt; TCGA.L5.A4OQ.01     1   0.778     -0.580 0.42 0.26 0.00 0.32
#&gt; TCGA.R6.A8W5.01     1   0.778     -0.580 0.42 0.26 0.00 0.32
#&gt; TCGA.L5.A8NE.01     2   0.491      0.745 0.42 0.58 0.00 0.00
#&gt; TCGA.JY.A6FH.01     2   0.491      0.745 0.42 0.58 0.00 0.00
#&gt; TCGA.VR.A8Q7.01     4   0.452      0.000 0.00 0.00 0.32 0.68
#&gt; TCGA.R6.A6Y0.01     2   0.452      0.114 0.00 0.68 0.00 0.32
#&gt; TCGA.L5.A891.01     3   0.491      1.000 0.00 0.00 0.58 0.42
#&gt; TCGA.2H.A9GJ.01     3   0.491      1.000 0.00 0.00 0.58 0.42
#&gt; TCGA.2H.A9GN.01     1   0.491      0.489 0.58 0.00 0.42 0.00
#&gt; TCGA.2H.A9GG.01     1   0.491      0.489 0.58 0.00 0.42 0.00
#&gt; TCGA.2H.A9GQ.01     3   0.491      1.000 0.00 0.00 0.58 0.42
#&gt; TCGA.L5.A8NF.01     2   0.491      0.745 0.42 0.58 0.00 0.00
#&gt; TCGA.L5.A8NI.01     1   0.491      0.320 0.58 0.42 0.00 0.00
</code></pre>

<script>
$('#tab-node-04-get-classes-3-a').parent().next().next().hide();
$('#tab-node-04-get-classes-3-a').click(function(){
  $('#tab-node-04-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-04-get-classes-4'>
<p><a id='tab-node-04-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.L5.A43M.01     1   0.000      0.974 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     5   0.000      0.934 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.R6.A8W5.01     5   0.000      0.934 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.L5.A8NE.01     2   0.430      1.000 0.00 0.52 0.00 0.00 0.48
#&gt; TCGA.JY.A6FH.01     5   0.141      0.857 0.00 0.06 0.00 0.00 0.94
#&gt; TCGA.VR.A8Q7.01     3   0.543      0.521 0.00 0.42 0.52 0.06 0.00
#&gt; TCGA.R6.A6Y0.01     4   0.252      0.795 0.00 0.00 0.00 0.86 0.14
#&gt; TCGA.L5.A891.01     3   0.000      0.840 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     3   0.000      0.840 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.2H.A9GN.01     1   0.000      0.974 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     1   0.141      0.947 0.94 0.06 0.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     3   0.173      0.823 0.00 0.00 0.92 0.08 0.00
#&gt; TCGA.L5.A8NF.01     2   0.430      1.000 0.00 0.52 0.00 0.00 0.48
#&gt; TCGA.L5.A8NI.01     4   0.252      0.791 0.14 0.00 0.00 0.86 0.00
</code></pre>

<script>
$('#tab-node-04-get-classes-4-a').parent().next().next().hide();
$('#tab-node-04-get-classes-4-a').click(function(){
  $('#tab-node-04-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-04-get-classes-5'>
<p><a id='tab-node-04-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.L5.A43M.01     1  0.0000      0.826 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     5  0.0000      0.848 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.R6.A8W5.01     5  0.0000      0.848 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NE.01     2  0.3309      0.950 0.00 0.72 0.00 0.00 0.28 0.00
#&gt; TCGA.JY.A6FH.01     5  0.4004      0.643 0.00 0.12 0.00 0.00 0.76 0.12
#&gt; TCGA.VR.A8Q7.01     6  0.3797      0.000 0.00 0.00 0.42 0.00 0.00 0.58
#&gt; TCGA.R6.A6Y0.01     4  0.1556      0.875 0.00 0.00 0.00 0.92 0.08 0.00
#&gt; TCGA.L5.A891.01     3  0.0547      0.848 0.00 0.00 0.98 0.02 0.00 0.00
#&gt; TCGA.2H.A9GJ.01     3  0.0000      0.855 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GN.01     1  0.1267      0.826 0.94 0.06 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GG.01     1  0.4926      0.675 0.64 0.12 0.00 0.00 0.00 0.24
#&gt; TCGA.2H.A9GQ.01     3  0.3045      0.717 0.00 0.10 0.84 0.06 0.00 0.00
#&gt; TCGA.L5.A8NF.01     2  0.4172      0.951 0.00 0.68 0.00 0.00 0.28 0.04
#&gt; TCGA.L5.A8NI.01     4  0.2094      0.876 0.08 0.00 0.00 0.90 0.00 0.02
</code></pre>

<script>
$('#tab-node-04-get-classes-5-a').parent().next().next().hide();
$('#tab-node-04-get-classes-5-a').click(function(){
  $('#tab-node-04-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-04-get-classes-6'>
<p><a id='tab-node-04-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.L5.A43M.01     1  0.0504      0.843 0.98 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A4OQ.01     7  0.2376      0.786 0.00 0.12 0.00 0.00 0.02 0.00 0.86
#&gt; TCGA.R6.A8W5.01     7  0.1886      0.786 0.00 0.12 0.00 0.00 0.00 0.00 0.88
#&gt; TCGA.L5.A8NE.01     2  0.2572      0.879 0.00 0.86 0.00 0.00 0.08 0.06 0.00
#&gt; TCGA.JY.A6FH.01     7  0.5016      0.539 0.00 0.12 0.00 0.00 0.00 0.42 0.46
#&gt; TCGA.VR.A8Q7.01     6  0.5164      0.000 0.00 0.00 0.20 0.00 0.26 0.54 0.00
#&gt; TCGA.R6.A6Y0.01     4  0.0000      0.934 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A891.01     3  0.3417      0.799 0.00 0.00 0.72 0.00 0.26 0.00 0.02
#&gt; TCGA.2H.A9GJ.01     3  0.2945      0.804 0.00 0.00 0.74 0.00 0.26 0.00 0.00
#&gt; TCGA.2H.A9GN.01     1  0.0504      0.843 0.98 0.00 0.00 0.00 0.00 0.02 0.00
#&gt; TCGA.2H.A9GG.01     1  0.3221      0.695 0.68 0.00 0.00 0.00 0.32 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     3  0.0863      0.612 0.00 0.00 0.96 0.00 0.00 0.00 0.04
#&gt; TCGA.L5.A8NF.01     2  0.0000      0.880 0.00 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A8NI.01     4  0.1718      0.934 0.00 0.00 0.00 0.92 0.04 0.00 0.04
</code></pre>

<script>
$('#tab-node-04-get-classes-6-a').parent().next().next().hide();
$('#tab-node-04-get-classes-6-a').click(function(){
  $('#tab-node-04-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-04-get-classes-7'>
<p><a id='tab-node-04-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3  p4   p5   p6   p7   p8
#&gt; TCGA.L5.A43M.01     5  0.3318      0.000 0.46 0.00 0.00 0.0 0.54 0.00 0.00 0.00
#&gt; TCGA.L5.A4OQ.01     7  0.2132      0.853 0.00 0.00 0.00 0.0 0.08 0.04 0.88 0.00
#&gt; TCGA.R6.A8W5.01     7  0.0000      0.853 0.00 0.00 0.00 0.0 0.00 0.00 1.00 0.00
#&gt; TCGA.L5.A8NE.01     2  0.5352      0.687 0.00 0.64 0.00 0.0 0.12 0.04 0.06 0.14
#&gt; TCGA.JY.A6FH.01     8  0.2938      0.000 0.00 0.00 0.00 0.0 0.00 0.00 0.30 0.70
#&gt; TCGA.VR.A8Q7.01     6  0.2852      0.000 0.00 0.00 0.28 0.0 0.00 0.72 0.00 0.00
#&gt; TCGA.R6.A6Y0.01     4  0.2719      0.832 0.00 0.02 0.00 0.8 0.00 0.18 0.00 0.00
#&gt; TCGA.L5.A891.01     3  0.0808      0.693 0.00 0.00 0.96 0.0 0.00 0.00 0.00 0.04
#&gt; TCGA.2H.A9GJ.01     3  0.0808      0.693 0.00 0.04 0.96 0.0 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GN.01     1  0.4803     -0.840 0.46 0.00 0.00 0.0 0.44 0.02 0.00 0.08
#&gt; TCGA.2H.A9GG.01     1  0.0000      0.000 1.00 0.00 0.00 0.0 0.00 0.00 0.00 0.00
#&gt; TCGA.2H.A9GQ.01     3  0.4482      0.417 0.00 0.00 0.60 0.0 0.26 0.00 0.00 0.14
#&gt; TCGA.L5.A8NF.01     2  0.1091      0.704 0.00 0.94 0.00 0.0 0.00 0.00 0.06 0.00
#&gt; TCGA.L5.A8NI.01     4  0.0000      0.832 0.00 0.00 0.00 1.0 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-04-get-classes-7-a').parent().next().next().hide();
$('#tab-node-04-get-classes-7-a').click(function(){
  $('#tab-node-04-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-04-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-04-consensus-heatmap'>
<ul>
<li><a href='#tab-node-04-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-04-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-04-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-04-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-04-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-04-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-04-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-04-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-04-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-04-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-04-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-04-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-04-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-04-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-04-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-04-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-04-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-04-membership-heatmap'>
<ul>
<li><a href='#tab-node-04-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-04-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-04-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-04-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-04-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-04-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-04-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-04-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-1-1.png" alt="plot of chunk tab-node-04-membership-heatmap-1"/></p>

</div>
<div id='tab-node-04-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-2-1.png" alt="plot of chunk tab-node-04-membership-heatmap-2"/></p>

</div>
<div id='tab-node-04-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-3-1.png" alt="plot of chunk tab-node-04-membership-heatmap-3"/></p>

</div>
<div id='tab-node-04-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-4-1.png" alt="plot of chunk tab-node-04-membership-heatmap-4"/></p>

</div>
<div id='tab-node-04-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-5-1.png" alt="plot of chunk tab-node-04-membership-heatmap-5"/></p>

</div>
<div id='tab-node-04-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-6-1.png" alt="plot of chunk tab-node-04-membership-heatmap-6"/></p>

</div>
<div id='tab-node-04-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-04-membership-heatmap-7-1.png" alt="plot of chunk tab-node-04-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-04-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-04-get-signatures'>
<ul>
<li><a href='#tab-node-04-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-04-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-04-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-04-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-04-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-04-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-04-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-04-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-1-1.png" alt="plot of chunk tab-node-04-get-signatures-1"/></p>

</div>
<div id='tab-node-04-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-2-1.png" alt="plot of chunk tab-node-04-get-signatures-2"/></p>

</div>
<div id='tab-node-04-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-3-1.png" alt="plot of chunk tab-node-04-get-signatures-3"/></p>

</div>
<div id='tab-node-04-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-4-1.png" alt="plot of chunk tab-node-04-get-signatures-4"/></p>

</div>
<div id='tab-node-04-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-5-1.png" alt="plot of chunk tab-node-04-get-signatures-5"/></p>

</div>
<div id='tab-node-04-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-6-1.png" alt="plot of chunk tab-node-04-get-signatures-6"/></p>

</div>
<div id='tab-node-04-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-04-get-signatures-7-1.png" alt="plot of chunk tab-node-04-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-04-signature_compare](figure_cola/node-04-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-04-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-04-dimension-reduction'>
<ul>
<li><a href='#tab-node-04-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-04-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-04-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-04-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-04-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-04-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-04-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-04-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-1-1.png" alt="plot of chunk tab-node-04-dimension-reduction-1"/></p>

</div>
<div id='tab-node-04-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-2-1.png" alt="plot of chunk tab-node-04-dimension-reduction-2"/></p>

</div>
<div id='tab-node-04-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-3-1.png" alt="plot of chunk tab-node-04-dimension-reduction-3"/></p>

</div>
<div id='tab-node-04-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-4-1.png" alt="plot of chunk tab-node-04-dimension-reduction-4"/></p>

</div>
<div id='tab-node-04-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-5-1.png" alt="plot of chunk tab-node-04-dimension-reduction-5"/></p>

</div>
<div id='tab-node-04-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-6-1.png" alt="plot of chunk tab-node-04-dimension-reduction-6"/></p>

</div>
<div id='tab-node-04-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-04-dimension-reduction-7-1.png" alt="plot of chunk tab-node-04-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-04-collect-classes](figure_cola/node-04-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

---------------------------------------------------




### Node05


Parent node: [Node0](#Node0).
Child nodes: 
                [Node011](#Node011)
        ,
                [Node012](#Node012)
        ,
                [Node013](#Node013)
        ,
                [Node021](#Node021)
        ,
                [Node022](#Node022)
        ,
                [Node023](#Node023)
        ,
                Node031-leaf
        ,
                Node032-leaf
        ,
                Node033-leaf
        ,
                Node034-leaf
        ,
                Node035-leaf
        ,
                Node041-leaf
        ,
                Node042-leaf
        ,
                Node043-leaf
        ,
                Node051-leaf
        ,
                Node052-leaf
        ,
                Node053-leaf
        .







The object with results only for a single top-value method and a single partitioning method 
can be extracted as:

```r
res = res_rh["05"]
```

A summary of `res` and all the functions that can be applied to it:

```r
res
```

```
#> A 'ConsensusPartition' object with k = 2, 3, 4, 5, 6, 7, 8.
#>   On a matrix with 30000 rows and 22 columns.
#>   Top rows (1000) are extracted by 'ATC' method.
#>   Subgroups are detected by 'kmeans' method.
#>   Performed in total 350 partitions by row resampling.
#>   Best k for subgroups seems to be 3.
#> 
#> Following methods can be applied to this 'ConsensusPartition' object:
#>  [1] "cola_report"             "collect_classes"         "collect_plots"          
#>  [4] "collect_stats"           "colnames"                "compare_partitions"     
#>  [7] "compare_signatures"      "consensus_heatmap"       "dimension_reduction"    
#> [10] "functional_enrichment"   "get_anno_col"            "get_anno"               
#> [13] "get_classes"             "get_consensus"           "get_matrix"             
#> [16] "get_membership"          "get_param"               "get_signatures"         
#> [19] "get_stats"               "is_best_k"               "is_stable_k"            
#> [22] "membership_heatmap"      "ncol"                    "nrow"                   
#> [25] "plot_ecdf"               "predict_classes"         "rownames"               
#> [28] "select_partition_number" "show"                    "suggest_best_k"         
#> [31] "test_to_known_factors"   "top_rows_heatmap"
```

`collect_plots()` function collects all the plots made from `res` for all `k` (number of subgroups)
into one single page to provide an easy and fast comparison between different `k`.

```r
collect_plots(res)
```

![plot of chunk node-05-collect-plots](figure_cola/node-05-collect-plots-1.png)

The plots are:

- The first row: a plot of the eCDF (empirical cumulative distribution
  function) curves of the consensus matrix for each `k` and the heatmap of
  predicted classes for each `k`.
- The second row: heatmaps of the consensus matrix for each `k`.
- The third row: heatmaps of the membership matrix for each `k`.
- The fouth row: heatmaps of the signatures for each `k`.

All the plots in panels can be made by individual functions and they are
plotted later in this section.

`select_partition_number()` produces several plots showing different
statistics for choosing "optimized" `k`. There are following statistics:

- eCDF curves of the consensus matrix for each `k`;
- 1-PAC. [The PAC score](https://en.wikipedia.org/wiki/Consensus_clustering#Over-interpretation_potential_of_consensus_clustering)
  measures the proportion of the ambiguous subgrouping.
- Mean silhouette score.
- Concordance. The mean probability of fiting the consensus subgroup labels in all
  partitions.
- Area increased. Denote $A_k$ as the area under the eCDF curve for current
  `k`, the area increased is defined as $A_k - A_{k-1}$.
- Rand index. The percent of pairs of samples that are both in a same cluster
  or both are not in a same cluster in the partition of k and k-1.
- Jaccard index. The ratio of pairs of samples are both in a same cluster in
  the partition of k and k-1 and the pairs of samples are both in a same
  cluster in the partition k or k-1.

The detailed explanations of these statistics can be found in [the _cola_
vignette](https://jokergoo.github.io/cola_vignettes/cola.html#toc_13).

Generally speaking, higher 1-PAC score, higher mean silhouette score or higher
concordance corresponds to better partition. Rand index and Jaccard index
measure how similar the current partition is compared to partition with `k-1`.
If they are too similar, we won't accept `k` is better than `k-1`.

```r
select_partition_number(res)
```

![plot of chunk node-05-select-partition-number](figure_cola/node-05-select-partition-number-1.png)

The numeric values for all these statistics can be obtained by `get_stats()`.

```r
get_stats(res)
```

```
#>   k 1-PAC mean_silhouette concordance area_increased  Rand Jaccard
#> 2 2 1.000           1.000       1.000         0.4854 0.515   0.515
#> 3 3 1.000           0.992       0.995         0.4266 0.792   0.597
#> 4 4 0.789           0.892       0.879         0.0901 0.931   0.775
#> 5 5 0.916           0.871       0.812         0.0548 1.000   1.000
#> 6 6 0.816           0.844       0.880         0.0428 0.948   0.782
#> 7 7 0.824           0.665       0.763         0.0258 0.944   0.711
#> 8 8 0.838           0.602       0.756         0.0189 0.944   0.649
```

`suggest_best_k()` suggests the best $k$ based on these statistics. The rules are as follows:

- All $k$ with Jaccard index larger than 0.95 are removed because increasing
  $k$ does not provide enough extra information. If all $k$ are removed, it is
  marked as no subgroup is detected.
- For all $k$ with 1-PAC score larger than 0.9, the maximal $k$ is taken as
  the best $k$, and other $k$ are marked as optional $k$.
- If it does not fit the second rule. The $k$ with the maximal vote of the
  highest 1-PAC score, highest mean silhouette, and highest concordance is
  taken as the best $k$.

```r
suggest_best_k(res)
```

```
#> [1] 3
#> attr(,"optional")
#> [1] 2
```

There is also optional best $k$ = 2 that is worth to check.

Following is the table of the partitions (You need to click the **show/hide
code output** link to see it). The membership matrix (columns with name `p*`)
is inferred by
[`clue::cl_consensus()`](https://www.rdocumentation.org/link/cl_consensus?package=clue)
function with the `SE` method. Basically the value in the membership matrix
represents the probability to belong to a certain group. The finall subgroup
label for an item is determined with the group with highest probability it
belongs to.

In `get_classes()` function, the entropy is calculated from the membership
matrix and the silhouette score is calculated from the consensus matrix.



<script>
$( function() {
	$( '#tabs-node-05-get-classes' ).tabs();
} );
</script>
<div id='tabs-node-05-get-classes'>
<ul>
<li><a href='#tab-node-05-get-classes-1'>k = 2</a></li>
<li><a href='#tab-node-05-get-classes-2'>k = 3</a></li>
<li><a href='#tab-node-05-get-classes-3'>k = 4</a></li>
<li><a href='#tab-node-05-get-classes-4'>k = 5</a></li>
<li><a href='#tab-node-05-get-classes-5'>k = 6</a></li>
<li><a href='#tab-node-05-get-classes-6'>k = 7</a></li>
<li><a href='#tab-node-05-get-classes-7'>k = 8</a></li>
</ul>

<div id='tab-node-05-get-classes-1'>
<p><a id='tab-node-05-get-classes-1-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 2), get_membership(res, k = 2))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1 p2
#&gt; TCGA.LN.A49L.01     2       0          1  0  1
#&gt; TCGA.LN.A49M.01     1       0          1  1  0
#&gt; TCGA.IG.A3YB.01     2       0          1  0  1
#&gt; TCGA.IG.A51D.01     2       0          1  0  1
#&gt; TCGA.L5.A43J.01     2       0          1  0  1
#&gt; TCGA.IG.A3I8.01     2       0          1  0  1
#&gt; TCGA.LN.A49V.01     2       0          1  0  1
#&gt; TCGA.JY.A6FG.01     1       0          1  1  0
#&gt; TCGA.L5.A88W.01     1       0          1  1  0
#&gt; TCGA.LN.A4A5.01     2       0          1  0  1
#&gt; TCGA.VR.AA7I.01     2       0          1  0  1
#&gt; TCGA.VR.AA7D.01     2       0          1  0  1
#&gt; TCGA.IC.A6RF.01     1       0          1  1  0
#&gt; TCGA.JY.A93F.01     1       0          1  1  0
#&gt; TCGA.L5.A88Z.01     2       0          1  0  1
#&gt; TCGA.IC.A6RF.11     1       0          1  1  0
#&gt; TCGA.Z6.A8JE.01     2       0          1  0  1
#&gt; TCGA.IG.A6QS.01     2       0          1  0  1
#&gt; TCGA.XP.A8T7.01     2       0          1  0  1
#&gt; TCGA.VR.A8EY.01     1       0          1  1  0
#&gt; TCGA.Z6.A9VB.01     2       0          1  0  1
#&gt; TCGA.V5.AASV.01     1       0          1  1  0
</code></pre>

<script>
$('#tab-node-05-get-classes-1-a').parent().next().next().hide();
$('#tab-node-05-get-classes-1-a').click(function(){
  $('#tab-node-05-get-classes-1-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-05-get-classes-2'>
<p><a id='tab-node-05-get-classes-2-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 3), get_membership(res, k = 3))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette p1   p2   p3
#&gt; TCGA.LN.A49L.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.LN.A49M.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.IG.A3YB.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.IG.A51D.01     2   0.000      0.983  0 1.00 0.00
#&gt; TCGA.L5.A43J.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.IG.A3I8.01     2   0.153      0.970  0 0.96 0.04
#&gt; TCGA.LN.A49V.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.JY.A6FG.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.L5.A88W.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.LN.A4A5.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.VR.AA7I.01     2   0.153      0.970  0 0.96 0.04
#&gt; TCGA.VR.AA7D.01     2   0.000      0.983  0 1.00 0.00
#&gt; TCGA.IC.A6RF.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.JY.A93F.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.L5.A88Z.01     3   0.000      1.000  0 0.00 1.00
#&gt; TCGA.IC.A6RF.11     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.Z6.A8JE.01     2   0.000      0.983  0 1.00 0.00
#&gt; TCGA.IG.A6QS.01     2   0.153      0.970  0 0.96 0.04
#&gt; TCGA.XP.A8T7.01     2   0.000      0.983  0 1.00 0.00
#&gt; TCGA.VR.A8EY.01     1   0.000      1.000  1 0.00 0.00
#&gt; TCGA.Z6.A9VB.01     2   0.000      0.983  0 1.00 0.00
#&gt; TCGA.V5.AASV.01     1   0.000      1.000  1 0.00 0.00
</code></pre>

<script>
$('#tab-node-05-get-classes-2-a').parent().next().next().hide();
$('#tab-node-05-get-classes-2-a').click(function(){
  $('#tab-node-05-get-classes-2-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-05-get-classes-3'>
<p><a id='tab-node-05-get-classes-3-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 4), get_membership(res, k = 4))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4
#&gt; TCGA.LN.A49L.01     3   0.000      1.000 0.00 0.00 1.00 0.00
#&gt; TCGA.LN.A49M.01     1   0.498      0.596 0.54 0.00 0.00 0.46
#&gt; TCGA.IG.A3YB.01     3   0.000      1.000 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A51D.01     2   0.000      0.940 0.00 1.00 0.00 0.00
#&gt; TCGA.L5.A43J.01     3   0.000      1.000 0.00 0.00 1.00 0.00
#&gt; TCGA.IG.A3I8.01     4   0.688      0.919 0.00 0.34 0.12 0.54
#&gt; TCGA.LN.A49V.01     3   0.000      1.000 0.00 0.00 1.00 0.00
#&gt; TCGA.JY.A6FG.01     1   0.000      0.886 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     1   0.000      0.886 1.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     3   0.000      1.000 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.AA7I.01     4   0.688      0.919 0.00 0.34 0.12 0.54
#&gt; TCGA.VR.AA7D.01     4   0.498      0.711 0.00 0.46 0.00 0.54
#&gt; TCGA.IC.A6RF.01     1   0.000      0.886 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A93F.01     1   0.000      0.886 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     3   0.000      1.000 0.00 0.00 1.00 0.00
#&gt; TCGA.IC.A6RF.11     1   0.000      0.886 1.00 0.00 0.00 0.00
#&gt; TCGA.Z6.A8JE.01     2   0.234      0.828 0.00 0.90 0.00 0.10
#&gt; TCGA.IG.A6QS.01     4   0.688      0.919 0.00 0.34 0.12 0.54
#&gt; TCGA.XP.A8T7.01     2   0.000      0.940 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.A8EY.01     1   0.498      0.596 0.54 0.00 0.00 0.46
#&gt; TCGA.Z6.A9VB.01     2   0.000      0.940 0.00 1.00 0.00 0.00
#&gt; TCGA.V5.AASV.01     1   0.000      0.886 1.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-05-get-classes-3-a').parent().next().next().hide();
$('#tab-node-05-get-classes-3-a').click(function(){
  $('#tab-node-05-get-classes-3-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-05-get-classes-4'>
<p><a id='tab-node-05-get-classes-4-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 5), get_membership(res, k = 5))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5
#&gt; TCGA.LN.A49L.01     5   0.228      0.851 0.00 0.00 0.12 0.00 0.88
#&gt; TCGA.LN.A49M.01     1   0.568      0.553 0.50 0.02 0.44 0.04 0.00
#&gt; TCGA.IG.A3YB.01     5   0.228      0.926 0.00 0.00 0.12 0.00 0.88
#&gt; TCGA.IG.A51D.01     2   0.332      0.911 0.00 0.82 0.16 0.02 0.00
#&gt; TCGA.L5.A43J.01     5   0.228      0.926 0.00 0.00 0.12 0.00 0.88
#&gt; TCGA.IG.A3I8.01     4   0.275      0.929 0.00 0.00 0.08 0.88 0.04
#&gt; TCGA.LN.A49V.01     5   0.228      0.926 0.00 0.00 0.12 0.00 0.88
#&gt; TCGA.JY.A6FG.01     1   0.000      0.866 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     1   0.000      0.866 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     5   0.000      0.918 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.VR.AA7I.01     4   0.104      0.960 0.00 0.00 0.00 0.96 0.04
#&gt; TCGA.VR.AA7D.01     4   0.104      0.931 0.00 0.04 0.00 0.96 0.00
#&gt; TCGA.IC.A6RF.01     1   0.122      0.860 0.96 0.02 0.02 0.00 0.00
#&gt; TCGA.JY.A93F.01     1   0.000      0.866 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     5   0.000      0.918 0.00 0.00 0.00 0.00 1.00
#&gt; TCGA.IC.A6RF.11     1   0.122      0.860 0.96 0.02 0.02 0.00 0.00
#&gt; TCGA.Z6.A8JE.01     2   0.122      0.903 0.00 0.96 0.02 0.02 0.00
#&gt; TCGA.IG.A6QS.01     4   0.104      0.960 0.00 0.00 0.00 0.96 0.04
#&gt; TCGA.XP.A8T7.01     2   0.332      0.911 0.00 0.82 0.16 0.02 0.00
#&gt; TCGA.VR.A8EY.01     1   0.431      0.553 0.50 0.00 0.50 0.00 0.00
#&gt; TCGA.Z6.A9VB.01     2   0.122      0.902 0.00 0.96 0.02 0.02 0.00
#&gt; TCGA.V5.AASV.01     1   0.000      0.866 1.00 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-05-get-classes-4-a').parent().next().next().hide();
$('#tab-node-05-get-classes-4-a').click(function(){
  $('#tab-node-05-get-classes-4-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-05-get-classes-5'>
<p><a id='tab-node-05-get-classes-5-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 6), get_membership(res, k = 6))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6
#&gt; TCGA.LN.A49L.01     5   0.273      0.816 0.00 0.10 0.00 0.00 0.86 0.04
#&gt; TCGA.LN.A49M.01     6   0.263      0.817 0.18 0.00 0.00 0.00 0.00 0.82
#&gt; TCGA.IG.A3YB.01     5   0.247      0.916 0.00 0.08 0.00 0.00 0.88 0.04
#&gt; TCGA.IG.A51D.01     3   0.000      0.717 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43J.01     5   0.247      0.916 0.00 0.08 0.00 0.00 0.88 0.04
#&gt; TCGA.IG.A3I8.01     4   0.279      0.873 0.00 0.08 0.00 0.86 0.00 0.06
#&gt; TCGA.LN.A49V.01     5   0.247      0.916 0.00 0.08 0.00 0.00 0.88 0.04
#&gt; TCGA.JY.A6FG.01     1   0.000      0.882 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     1   0.000      0.882 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     5   0.000      0.907 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.VR.AA7I.01     4   0.000      0.960 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.AA7D.01     4   0.000      0.960 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     1   0.399      0.733 0.76 0.10 0.00 0.00 0.00 0.14
#&gt; TCGA.JY.A93F.01     1   0.000      0.882 1.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     5   0.000      0.907 0.00 0.00 0.00 0.00 1.00 0.00
#&gt; TCGA.IC.A6RF.11     1   0.399      0.733 0.76 0.10 0.00 0.00 0.00 0.14
#&gt; TCGA.Z6.A8JE.01     3   0.461      0.690 0.00 0.42 0.54 0.00 0.00 0.04
#&gt; TCGA.IG.A6QS.01     4   0.000      0.960 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.XP.A8T7.01     3   0.000      0.717 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EY.01     6   0.529      0.824 0.18 0.22 0.00 0.00 0.00 0.60
#&gt; TCGA.Z6.A9VB.01     3   0.386      0.681 0.00 0.48 0.52 0.00 0.00 0.00
#&gt; TCGA.V5.AASV.01     1   0.000      0.882 1.00 0.00 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-05-get-classes-5-a').parent().next().next().hide();
$('#tab-node-05-get-classes-5-a').click(function(){
  $('#tab-node-05-get-classes-5-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-05-get-classes-6'>
<p><a id='tab-node-05-get-classes-6-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 7), get_membership(res, k = 7))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7
#&gt; TCGA.LN.A49L.01     5  0.3000      0.711 0.00 0.00 0.00 0.10 0.84 0.02 0.04
#&gt; TCGA.LN.A49M.01     6  0.4538      0.502 0.10 0.00 0.00 0.00 0.00 0.62 0.28
#&gt; TCGA.IG.A3YB.01     5  0.2832      0.838 0.00 0.00 0.00 0.24 0.76 0.00 0.00
#&gt; TCGA.IG.A51D.01     3  0.0000      0.718 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43J.01     5  0.2832      0.838 0.00 0.00 0.00 0.24 0.76 0.00 0.00
#&gt; TCGA.IG.A3I8.01     2  0.5423      0.688 0.00 0.66 0.00 0.16 0.04 0.04 0.10
#&gt; TCGA.LN.A49V.01     5  0.2832      0.838 0.00 0.00 0.00 0.24 0.76 0.00 0.00
#&gt; TCGA.JY.A6FG.01     1  0.0000      0.985 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88W.01     1  0.0863      0.953 0.96 0.04 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.LN.A4A5.01     5  0.0000      0.822 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.VR.AA7I.01     2  0.0863      0.885 0.00 0.96 0.00 0.00 0.04 0.00 0.00
#&gt; TCGA.VR.AA7D.01     2  0.0863      0.859 0.00 0.96 0.04 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     7  0.3546      0.164 0.46 0.00 0.00 0.00 0.00 0.00 0.54
#&gt; TCGA.JY.A93F.01     1  0.0000      0.985 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     5  0.0000      0.822 0.00 0.00 0.00 0.00 1.00 0.00 0.00
#&gt; TCGA.IC.A6RF.11     7  0.3546      0.164 0.46 0.00 0.00 0.00 0.00 0.00 0.54
#&gt; TCGA.Z6.A8JE.01     3  0.6073      0.323 0.00 0.00 0.42 0.34 0.00 0.04 0.20
#&gt; TCGA.IG.A6QS.01     2  0.0863      0.885 0.00 0.96 0.00 0.00 0.04 0.00 0.00
#&gt; TCGA.XP.A8T7.01     3  0.0000      0.718 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.A8EY.01     6  0.4905      0.549 0.10 0.00 0.00 0.16 0.00 0.68 0.06
#&gt; TCGA.Z6.A9VB.01     7  0.5485     -0.607 0.00 0.00 0.38 0.22 0.00 0.00 0.40
#&gt; TCGA.V5.AASV.01     1  0.0000      0.985 1.00 0.00 0.00 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-05-get-classes-6-a').parent().next().next().hide();
$('#tab-node-05-get-classes-6-a').click(function(){
  $('#tab-node-05-get-classes-6-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>

<div id='tab-node-05-get-classes-7'>
<p><a id='tab-node-05-get-classes-7-a' style='color:#0366d6' href='#'>show/hide code output</a></p>
<pre><code class="r">cbind(get_classes(res, k = 8), get_membership(res, k = 8))
</code></pre>

<pre><code>#&gt;                 class entropy silhouette   p1   p2   p3   p4   p5   p6   p7   p8
#&gt; TCGA.LN.A49L.01     8  0.3272      0.000 0.00 0.00 0.00 0.00 0.42 0.00 0.00 0.58
#&gt; TCGA.LN.A49M.01     7  0.6618     -0.469 0.10 0.00 0.22 0.00 0.00 0.10 0.48 0.10
#&gt; TCGA.IG.A3YB.01     5  0.0000      0.745 0.00 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A51D.01     3  0.2938      0.977 0.00 0.00 0.70 0.30 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A43J.01     5  0.0000      0.745 0.00 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.IG.A3I8.01     2  0.7244      0.361 0.00 0.46 0.08 0.12 0.00 0.06 0.08 0.20
#&gt; TCGA.LN.A49V.01     5  0.0000      0.745 0.00 0.00 0.00 0.00 1.00 0.00 0.00 0.00
#&gt; TCGA.JY.A6FG.01     1  0.0471      0.958 0.98 0.00 0.00 0.00 0.00 0.00 0.00 0.02
#&gt; TCGA.L5.A88W.01     1  0.1341      0.912 0.92 0.00 0.00 0.00 0.00 0.00 0.00 0.08
#&gt; TCGA.LN.A4A5.01     5  0.2650      0.456 0.00 0.00 0.00 0.00 0.76 0.00 0.00 0.24
#&gt; TCGA.VR.AA7I.01     2  0.0000      0.830 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.VR.AA7D.01     2  0.0000      0.830 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.IC.A6RF.01     7  0.3272      0.470 0.42 0.00 0.00 0.00 0.00 0.00 0.58 0.00
#&gt; TCGA.JY.A93F.01     1  0.0000      0.962 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.L5.A88Z.01     5  0.2756      0.429 0.00 0.00 0.00 0.00 0.74 0.00 0.00 0.26
#&gt; TCGA.IC.A6RF.11     7  0.3272      0.470 0.42 0.00 0.00 0.00 0.00 0.00 0.58 0.00
#&gt; TCGA.Z6.A8JE.01     4  0.3995      0.519 0.00 0.00 0.02 0.60 0.00 0.36 0.00 0.02
#&gt; TCGA.IG.A6QS.01     2  0.0000      0.830 0.00 1.00 0.00 0.00 0.00 0.00 0.00 0.00
#&gt; TCGA.XP.A8T7.01     3  0.3374      0.977 0.00 0.00 0.68 0.30 0.00 0.00 0.02 0.00
#&gt; TCGA.VR.A8EY.01     6  0.4433      0.000 0.10 0.00 0.00 0.00 0.00 0.56 0.34 0.00
#&gt; TCGA.Z6.A9VB.01     4  0.0000      0.533 0.00 0.00 0.00 1.00 0.00 0.00 0.00 0.00
#&gt; TCGA.V5.AASV.01     1  0.0000      0.962 1.00 0.00 0.00 0.00 0.00 0.00 0.00 0.00
</code></pre>

<script>
$('#tab-node-05-get-classes-7-a').parent().next().next().hide();
$('#tab-node-05-get-classes-7-a').click(function(){
  $('#tab-node-05-get-classes-7-a').parent().next().next().toggle();
  return(false);
});
</script>
</div>
</div>

Heatmaps for the consensus matrix. It visualizes the probability of two
samples to be in a same group.




<script>
$( function() {
	$( '#tabs-node-05-consensus-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-05-consensus-heatmap'>
<ul>
<li><a href='#tab-node-05-consensus-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-05-consensus-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-05-consensus-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-05-consensus-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-05-consensus-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-05-consensus-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-05-consensus-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-05-consensus-heatmap-1'>
<pre><code class="r">consensus_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-1-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-1"/></p>

</div>
<div id='tab-node-05-consensus-heatmap-2'>
<pre><code class="r">consensus_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-2-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-2"/></p>

</div>
<div id='tab-node-05-consensus-heatmap-3'>
<pre><code class="r">consensus_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-3-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-3"/></p>

</div>
<div id='tab-node-05-consensus-heatmap-4'>
<pre><code class="r">consensus_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-4-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-4"/></p>

</div>
<div id='tab-node-05-consensus-heatmap-5'>
<pre><code class="r">consensus_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-5-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-5"/></p>

</div>
<div id='tab-node-05-consensus-heatmap-6'>
<pre><code class="r">consensus_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-6-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-6"/></p>

</div>
<div id='tab-node-05-consensus-heatmap-7'>
<pre><code class="r">consensus_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-05-consensus-heatmap-7-1.png" alt="plot of chunk tab-node-05-consensus-heatmap-7"/></p>

</div>
</div>

Heatmaps for the membership of samples in all partitions to see how consistent they are:





<script>
$( function() {
	$( '#tabs-node-05-membership-heatmap' ).tabs();
} );
</script>
<div id='tabs-node-05-membership-heatmap'>
<ul>
<li><a href='#tab-node-05-membership-heatmap-1'>k = 2</a></li>
<li><a href='#tab-node-05-membership-heatmap-2'>k = 3</a></li>
<li><a href='#tab-node-05-membership-heatmap-3'>k = 4</a></li>
<li><a href='#tab-node-05-membership-heatmap-4'>k = 5</a></li>
<li><a href='#tab-node-05-membership-heatmap-5'>k = 6</a></li>
<li><a href='#tab-node-05-membership-heatmap-6'>k = 7</a></li>
<li><a href='#tab-node-05-membership-heatmap-7'>k = 8</a></li>
</ul>
<div id='tab-node-05-membership-heatmap-1'>
<pre><code class="r">membership_heatmap(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-1-1.png" alt="plot of chunk tab-node-05-membership-heatmap-1"/></p>

</div>
<div id='tab-node-05-membership-heatmap-2'>
<pre><code class="r">membership_heatmap(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-2-1.png" alt="plot of chunk tab-node-05-membership-heatmap-2"/></p>

</div>
<div id='tab-node-05-membership-heatmap-3'>
<pre><code class="r">membership_heatmap(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-3-1.png" alt="plot of chunk tab-node-05-membership-heatmap-3"/></p>

</div>
<div id='tab-node-05-membership-heatmap-4'>
<pre><code class="r">membership_heatmap(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-4-1.png" alt="plot of chunk tab-node-05-membership-heatmap-4"/></p>

</div>
<div id='tab-node-05-membership-heatmap-5'>
<pre><code class="r">membership_heatmap(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-5-1.png" alt="plot of chunk tab-node-05-membership-heatmap-5"/></p>

</div>
<div id='tab-node-05-membership-heatmap-6'>
<pre><code class="r">membership_heatmap(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-6-1.png" alt="plot of chunk tab-node-05-membership-heatmap-6"/></p>

</div>
<div id='tab-node-05-membership-heatmap-7'>
<pre><code class="r">membership_heatmap(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-05-membership-heatmap-7-1.png" alt="plot of chunk tab-node-05-membership-heatmap-7"/></p>

</div>
</div>

As soon as the classes for columns are determined, the signatures
that are significantly different between subgroups can be looked for. 
Following are the heatmaps for signatures.






<script>
$( function() {
	$( '#tabs-node-05-get-signatures' ).tabs();
} );
</script>
<div id='tabs-node-05-get-signatures'>
<ul>
<li><a href='#tab-node-05-get-signatures-1'>k = 2</a></li>
<li><a href='#tab-node-05-get-signatures-2'>k = 3</a></li>
<li><a href='#tab-node-05-get-signatures-3'>k = 4</a></li>
<li><a href='#tab-node-05-get-signatures-4'>k = 5</a></li>
<li><a href='#tab-node-05-get-signatures-5'>k = 6</a></li>
<li><a href='#tab-node-05-get-signatures-6'>k = 7</a></li>
<li><a href='#tab-node-05-get-signatures-7'>k = 8</a></li>
</ul>
<div id='tab-node-05-get-signatures-1'>
<pre><code class="r">get_signatures(res, k = 2)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-1-1.png" alt="plot of chunk tab-node-05-get-signatures-1"/></p>

</div>
<div id='tab-node-05-get-signatures-2'>
<pre><code class="r">get_signatures(res, k = 3)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-2-1.png" alt="plot of chunk tab-node-05-get-signatures-2"/></p>

</div>
<div id='tab-node-05-get-signatures-3'>
<pre><code class="r">get_signatures(res, k = 4)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-3-1.png" alt="plot of chunk tab-node-05-get-signatures-3"/></p>

</div>
<div id='tab-node-05-get-signatures-4'>
<pre><code class="r">get_signatures(res, k = 5)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-4-1.png" alt="plot of chunk tab-node-05-get-signatures-4"/></p>

</div>
<div id='tab-node-05-get-signatures-5'>
<pre><code class="r">get_signatures(res, k = 6)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-5-1.png" alt="plot of chunk tab-node-05-get-signatures-5"/></p>

</div>
<div id='tab-node-05-get-signatures-6'>
<pre><code class="r">get_signatures(res, k = 7)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-6-1.png" alt="plot of chunk tab-node-05-get-signatures-6"/></p>

</div>
<div id='tab-node-05-get-signatures-7'>
<pre><code class="r">get_signatures(res, k = 8)
</code></pre>

<p><img src="figure_cola/tab-node-05-get-signatures-7-1.png" alt="plot of chunk tab-node-05-get-signatures-7"/></p>

</div>
</div>



Compare the overlap of signatures from different k:

```r
compare_signatures(res)
```

![plot of chunk node-05-signature_compare](figure_cola/node-05-signature_compare-1.png)

`get_signature()` returns a data frame invisibly. To get the list of signatures, the function
call should be assigned to a variable explicitly. In following code, if `plot` argument is set
to `FALSE`, no heatmap is plotted while only the differential analysis is performed.

```r
# code only for demonstration
tb = get_signature(res, k = ..., plot = FALSE)
```

An example of the output of `tb` is:

```
#>   which_row         fdr    mean_1    mean_2 scaled_mean_1 scaled_mean_2 km
#> 1        38 0.042760348  8.373488  9.131774    -0.5533452     0.5164555  1
#> 2        40 0.018707592  7.106213  8.469186    -0.6173731     0.5762149  1
#> 3        55 0.019134737 10.221463 11.207825    -0.6159697     0.5749050  1
#> 4        59 0.006059896  5.921854  7.869574    -0.6899429     0.6439467  1
#> 5        60 0.018055526  8.928898 10.211722    -0.6204761     0.5791110  1
#> 6        98 0.009384629 15.714769 14.887706     0.6635654    -0.6193277  2
...
```

The columns in `tb` are:

1. `which_row`: row indices corresponding to the input matrix.
2. `fdr`: FDR for the differential test. 
3. `mean_x`: The mean value in group x.
4. `scaled_mean_x`: The mean value in group x after rows are scaled.
5. `km`: Row groups if k-means clustering is applied to rows (which is done by automatically selecting number of clusters).

If there are too many signatures, `top_signatures = ...` can be set to only show the 
signatures with the highest FDRs:

```r
# code only for demonstration
# e.g. to show the top 500 most significant rows
tb = get_signature(res, k = ..., top_signatures = 500)
```

If the signatures are defined as these which are uniquely high in current group, `diff_method` argument
can be set to `"uniquely_high_in_one_group"`:

```r
# code only for demonstration
tb = get_signature(res, k = ..., diff_method = "uniquely_high_in_one_group")
```




UMAP plot which shows how samples are separated.


<script>
$( function() {
	$( '#tabs-node-05-dimension-reduction' ).tabs();
} );
</script>
<div id='tabs-node-05-dimension-reduction'>
<ul>
<li><a href='#tab-node-05-dimension-reduction-1'>k = 2</a></li>
<li><a href='#tab-node-05-dimension-reduction-2'>k = 3</a></li>
<li><a href='#tab-node-05-dimension-reduction-3'>k = 4</a></li>
<li><a href='#tab-node-05-dimension-reduction-4'>k = 5</a></li>
<li><a href='#tab-node-05-dimension-reduction-5'>k = 6</a></li>
<li><a href='#tab-node-05-dimension-reduction-6'>k = 7</a></li>
<li><a href='#tab-node-05-dimension-reduction-7'>k = 8</a></li>
</ul>
<div id='tab-node-05-dimension-reduction-1'>
<pre><code class="r">dimension_reduction(res, k = 2, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-1-1.png" alt="plot of chunk tab-node-05-dimension-reduction-1"/></p>

</div>
<div id='tab-node-05-dimension-reduction-2'>
<pre><code class="r">dimension_reduction(res, k = 3, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-2-1.png" alt="plot of chunk tab-node-05-dimension-reduction-2"/></p>

</div>
<div id='tab-node-05-dimension-reduction-3'>
<pre><code class="r">dimension_reduction(res, k = 4, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-3-1.png" alt="plot of chunk tab-node-05-dimension-reduction-3"/></p>

</div>
<div id='tab-node-05-dimension-reduction-4'>
<pre><code class="r">dimension_reduction(res, k = 5, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-4-1.png" alt="plot of chunk tab-node-05-dimension-reduction-4"/></p>

</div>
<div id='tab-node-05-dimension-reduction-5'>
<pre><code class="r">dimension_reduction(res, k = 6, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-5-1.png" alt="plot of chunk tab-node-05-dimension-reduction-5"/></p>

</div>
<div id='tab-node-05-dimension-reduction-6'>
<pre><code class="r">dimension_reduction(res, k = 7, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-6-1.png" alt="plot of chunk tab-node-05-dimension-reduction-6"/></p>

</div>
<div id='tab-node-05-dimension-reduction-7'>
<pre><code class="r">dimension_reduction(res, k = 8, method = &quot;UMAP&quot;)
</code></pre>

<p><img src="figure_cola/tab-node-05-dimension-reduction-7-1.png" alt="plot of chunk tab-node-05-dimension-reduction-7"/></p>

</div>
</div>



Following heatmap shows how subgroups are split when increasing `k`:

```r
collect_classes(res)
```

![plot of chunk node-05-collect-classes](figure_cola/node-05-collect-classes-1.png)



If matrix rows can be associated to genes, consider to use `functional_enrichment(res,
...)` to perform function enrichment for the signature genes. See [this vignette](https://jokergoo.github.io/cola_vignettes/functional_enrichment.html) for more detailed explanations.


 

## Session info


```r
sessionInfo()
```

```
#> R version 4.1.0 (2021-05-18)
#> Platform: x86_64-pc-linux-gnu (64-bit)
#> Running under: CentOS Linux 7 (Core)
#> 
#> Matrix products: default
#> BLAS/LAPACK: /usr/lib64/libopenblas-r0.3.3.so
#> 
#> locale:
#>  [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C               LC_TIME=en_US.UTF-8       
#>  [4] LC_COLLATE=en_US.UTF-8     LC_MONETARY=en_US.UTF-8    LC_MESSAGES=en_US.UTF-8   
#>  [7] LC_PAPER=en_US.UTF-8       LC_NAME=C                  LC_ADDRESS=C              
#> [10] LC_TELEPHONE=C             LC_MEASUREMENT=en_US.UTF-8 LC_IDENTIFICATION=C       
#> 
#> attached base packages:
#> [1] grid      stats     graphics  grDevices utils     datasets  methods   base     
#> 
#> other attached packages:
#> [1] genefilter_1.74.0    ComplexHeatmap_2.8.0 markdown_1.1         knitr_1.33          
#> [5] matrixStats_0.59.0   cola_1.9.4          
#> 
#> loaded via a namespace (and not attached):
#>   [1] bitops_1.0-7           bit64_4.0.5            doParallel_1.0.16      RColorBrewer_1.1-2    
#>   [5] httr_1.4.2             GenomeInfoDb_1.28.1    data.tree_1.0.0        tools_4.1.0           
#>   [9] utf8_1.2.1             R6_2.5.0               irlba_2.3.3            DBI_1.1.1             
#>  [13] BiocGenerics_0.38.0    colorspace_2.0-2       GetoptLong_1.0.5       gridExtra_2.3         
#>  [17] tidyselect_1.1.1       bit_4.0.4              compiler_4.1.0         Biobase_2.52.0        
#>  [21] Cairo_1.5-12.2         xml2_1.3.2             microbenchmark_1.4-7   slam_0.1-48           
#>  [25] scales_1.1.1           askpass_1.1            stringr_1.4.0          digest_0.6.27         
#>  [29] XVector_0.32.0         pkgconfig_2.0.3        umap_0.2.7.0           fastmap_1.1.0         
#>  [33] highr_0.9              rlang_0.4.11           GlobalOptions_0.1.2    rstudioapi_0.13       
#>  [37] RSQLite_2.2.7          impute_1.66.0          generics_0.1.0         shape_1.4.6           
#>  [41] jsonlite_1.7.2         mclust_5.4.7           dplyr_1.0.7            dendextend_1.15.1     
#>  [45] RCurl_1.98-1.3         magrittr_2.0.1         GenomeInfoDbData_1.2.6 Matrix_1.3-4          
#>  [49] fansi_0.5.0            Rcpp_1.0.7             munsell_0.5.0          S4Vectors_0.30.0      
#>  [53] viridis_0.6.1          reticulate_1.20        lifecycle_1.0.0        scatterplot3d_0.3-41  
#>  [57] stringi_1.7.3          zlibbioc_1.38.0        blob_1.2.1             parallel_4.1.0        
#>  [61] crayon_1.4.1           lattice_0.20-44        Biostrings_2.60.1      splines_4.1.0         
#>  [65] annotate_1.70.0        circlize_0.4.13        KEGGREST_1.32.0        polylabelr_0.2.0      
#>  [69] pillar_1.6.1           rjson_0.2.20           codetools_0.2-18       stats4_4.1.0          
#>  [73] XML_3.99-0.6           glue_1.4.2             evaluate_0.14          png_0.1-7             
#>  [77] vctrs_0.3.8            foreach_1.5.1          polyclip_1.10-0        purrr_0.3.4           
#>  [81] gtable_0.3.0           openssl_1.4.4          assertthat_0.2.1       clue_0.3-59           
#>  [85] cachem_1.0.5           ggplot2_3.3.5          xfun_0.24              eulerr_6.1.0          
#>  [89] xtable_1.8-4           skmeans_0.2-13         RSpectra_0.16-0        viridisLite_0.4.0     
#>  [93] survival_3.2-11        tibble_3.1.2           Polychrome_1.3.1       iterators_1.0.13      
#>  [97] AnnotationDbi_1.54.1   memoise_2.0.0          IRanges_2.26.0         cluster_2.1.2         
#> [101] ellipsis_0.3.2         brew_1.0-6
```




