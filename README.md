# ![ logo ](./img/mtm-mini.png) MetaTreeMap
MetaTreeMap (MTM) is a module developed to visualize phylogenic trees where each species (node) has a number of reads (quantity) that map on the reference genome of this species. Each species is represented by a rectangle and its area is proportional to the number of assigned reads. The final figure is nested rectangles representing tree branches.

# Citation

> Hebrard M, Taylor TD. MetaTreeMap: an alternative visualization method for
displaying metagenomic phylogenic trees. PLOS One 11(6):e0158261. (June 23, 2016) PMID 27336370

![ thumbnail ](./img/mtm-thumbnail.png)

# Web service
MTM can be use online at [this address](http://metasystems.riken.jp/visualization/treemap/index.htm).
For more information see the [user guide](http://metasystems.riken.jp/visualization/treemap/html/documentation.htm).

# Javascript Library
MTM can be use as a javascript library and include in your own webpage.

**Download** the minify version [here](http://metasystems.riken.jp/visualization/treemap/mtm.min.js). And include the library in your web page like this: 

```
<script type="text/javascript" src="./mtm.min.js"></script>
```

**Or** You can use our **CDN**, and including the latest version.

```
<script type="text/javascript" src="http://metasystems.riken.jp/visualization/cdn/mtm.min.js"></script>
```

**Add classes** to HTML elements that will contain the different views

```
<div class="mtm-menu"><!--option bar--></div>
<div class="mtm-treemap"><!--treemap view--></div>
<div class="mtm-table"><!--table view--></div>
```

**Call the script** with a list of default datafile(s)

```
<script type="text/javascript">mtm.load(["path/to/file1","path/to/file2"]);</script>
```

In addition you can pass a **config file** in second argument (see [Documentation](http://metasystems.riken.jp/visualization/treemap/html/documentation.htm#import-config) for more information).

```
<script type="text/javascript">mtm.load(["path/to/file1"],"my_config.json");</script>
```

**Exposed functions:**

* **mtm.version**: return the version number

# Repository

* **data**: example data files used as input for MTM. Sequensing data from Kurokawa et al, taxonomic assignation computed with [MetaBin](http://metabin.riken.jp/). In addition **taxonomy.tsv** is the list of NCBI taxa with ID and phylogenic rank information (file needed for convertor module).

> Kurokawa,K. et al. (2007) Comparative metagenomics revealed commonly enriched gene sets in human gut microbiomes. DNA Res., 14(4), 169-181. 

* **html**: Documentation and feedback form.
* **img**: images for documentation.
* **js**: javascript libraries and sources.
* **LICENCE**: full licence file.
* **README**: current abstract
* **index.htm**: The frontpage of the web interface.
* **mtm.min.js**: the minify version of MTM (used by the web interface)
