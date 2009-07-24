---
title: Tree
permalink: wiki/Tree
layout: wiki
---

This module provides the classes for representing phylogenetic trees.

This code is not yet part of Biopython, and therefore the documentation
has not been integrated into the Biopython Tutorial yet either.

Installation
------------

This module is being developed alongside phyloXML support as a Google
Summer of Code 2009 project. To use TreeIO, see the
[PhyloXML](PhyloXML "wikilink") page for instructions on installing from
a [GitHub](GitUsage "wikilink") branch.

Usage
-----

See the [PhyloXML](PhyloXML "wikilink") page for examples of using Tree
objects.

### Utilities

Some additional tools are located in Bio.Tree.Utils.

``` python
from Bio.Tree import Utils
```

-   pretty\_print -- Produces a plain-text representation of the
    entire tree. Uses str() to display nodes by default; for the
    longer repr() representation, add the argument show\_all=True.

<!-- -->

    >>> phx = TreeIO.read('phyloxml_examples.xml', 'phyloxml')
    >>> Utils.pretty_print(phx)
    Phyloxml
        Phylogeny example from Prof. Joe Felsenstein's book "Inferring Phylogenies"
            Clade
                Clade
                    Clade A
                    Clade B
                Clade C
    ...

    >>> Utils.pretty_print(phx, show_all=True)
    Phyloxml()
        Phylogeny(description='phyloXML allows to use either a "branch_length"
    attribute or element to indicate branch lengths.', name='example from Prof. Joe
    Felsenstein's book "Inferring Phylogenies"')
            Clade()
                Clade(branch_length=0.06)
                    Clade(branch_length=0.102, name='A')
                    Clade(branch_length=0.23, name='B')
                Clade(branch_length=0.4, name='C')
    ...

...OK, there's only one utility in there right now, but as we write
more, that's where they'll go.