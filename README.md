# cables.csv to graph to svg

the short version

install igraph 0.6 with python bindings

_[optional]_ create list of MRNs and edges as plain text files:

    $ python extract.py cables.csv

create the large graph and split into smaller .gml files:
    
    $ python c2g.py

create html with inline svg from any .gml:

    $ pthon g2svg.py -g any.gml

or:

    $ ls *gml > list-of-gml-files
    $ pthon g2svg.py -i list-of-gml-files

# note

* copy and customize the default svg.tmpl and run `g2svg.py` with `-t example.svg`.
* svg.tmpl referes to svg.js and svg.css
* use [ReVerb](http://reverb.cs.washington.edu/) to extract sentences from the cables and use `g2svg.py -r example.reverb`. To generate input files for ReVerb: `python c2txt.py cables.csv MRN1 MRN2 ...`.
* `python g2svg.py -h` for more options.
* you _don't_ need to run `extract.py`, the code comes with all generated data/ files.

# copyleft

GPLv3

# contact

need help? ask!

https://twitter.com/c2graph

