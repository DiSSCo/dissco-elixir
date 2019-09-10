# DiSSCo-ELIXIR

This repository is for links and information to facilitate the upcoming workshop and further [DiSSCo](https://www.dissco.eu/)-[ELIXIR](https://elixir-europe.org/) initiatives. 


## First workshop 

Organised by [DiSSCo](https://www.dissco.eu/) and [ELIXIR](https://elixir-europe.org) and hosted by [CETAF](https://cetaf.org/). 

**Museum specimen <-> molecular data linkage: why and how?**



## Background and Context 


### What's in a name 


```
> get_uid(c("Agathis Montana"))
More than one UID found for taxon 'Agathis+Montana'!

            Enter rownumber of taxon (other inputs will return 'NA'):

  status    rank              division                  scientificname
1 active species wasps, ants, and bees Agathis montana Shestakov, 1932
2 active species           seed plants   Agathis montana de Laub. 1969
  commonname    uid   genus                 species subsp modificationdate
1            144212 Agathis montana Shestakov, 1932       2018/11/09 00:00
2             60852 Agathis   montana de Laub. 1969       2018/11/09 00:00

```
Is it a plant or a wasp? 

[https://www.ebi.ac.uk/ena/data/view/Taxon:60852](https://www.ebi.ac.uk/ena/data/view/Taxon:60852)

>Agathis montana is a valid species name in both the botanical and zoological codes. In order to resolve this ambiguity, sequence entries from these two species will be annotated with the binomial name and the taxonomic authority, i.e.:/organism="Agathis montana de Laub. 1969" (for the conifer)/organism="Agathis montana Shest. 1932" (for the wasp)"


Taxonomic research is still one of the most important aspects of species identification. Museum and herbarium specimens are important source for such research and individual level trait measurement through time. We now have billions of specimens available but not all of them are digitized and trait data is not always available. 

Fruthermore, taxonomic identificaiton is a slow process. So researchers are looking into multiple sources: morphological, ecological and molecular and [integrated](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2657783/) approach.  DNA sequencing is one of the fastest way of gathering evidence for taxonomic decision -- for example incorporating DNA evidence into [taxonomic decisions](https://doi.org/10.13156/arac.2018.18.2.94) 
[via DNA barcodes](https://dx.doi.org/10.3897%2Fzookeys.757.24453). But several papers (for example ([here](https://doi.org/10.1007/s13225-019-00428-3) and [here](https://doi.org/10.1046/j.1469-8137.2003.00894.x)) highlighted issues in sequence based identification. 

In essence we are dealing with two different workflows from two different domains ("traditional" collection and taxonomic research versus newer DNA sequencing methods). 

<img src="dna-taxonomy-link-hubert-hanner.png" alt="Conceptual Link Between DNA barcoding and taxonomy" align="centrer" width="440" height="300"/>

*[Figure]([http://doi.org10.1515/dna-2015-0006) by Hubert, Nicolas, and Robert Hanner.*
	

This [2015 publication](https://doi.org/10.1093/nar/gku1127) highlights various aspect of data storage, workflow, institutional involvement and most importantly FAIR research data life cycle. 


>GenBank is an archive of sequence data, particularly important for sequences associated with publications in the scientific literature. In this case the GenBank entries serve as supplementary material to the publication, and are ‘owned’ by the submitter/author. In this role, it is vital to preserve the original data so that the analysis from the paper can be evaluated and replicated. GenBank also serves as the general reference set of sequence data for current research in biology. There is a tension between these two goals. We try to keep sequences and metadata current, and archive versions of every update to the sequence entries to support the archival requirement. We update the taxonomy with respect to synonymy, but rely on the submitters for the correct original taxonomic identification of their specimens and for the appropriate annotation of their source material (in isolate, strain, culture-collection and specimen-voucher qualifiers). This means that there are misidentified sequences in GenBank, and entries with other annotation problems. It is important to have these corrected (or flagged as problematic) to support the reference database requirement. Third-party updates are passed along to the original submitters but are not implemented in GenBank without the submitters’ permission; entries with egregious errors may be suppressed or flagged as ‘unverified’. Sequence from type can help to alleviate these problems by providing a backbone of reliably identified sequence data. 

Is it then just about data linkage?  Some of these issues might have been resolved or partially addressed since 2015 but we still have a ways to go. 
[Recent publication](https://doi.org/10.3897/biss.3.37288) by Devine and Coddington indicates other gaps in the data landscape. 


>Taxonomic gap analysis results for all of life on Earth as of 06 March 2019. Total counts were derived from the Catalogue of Life (Roskov et al. 2019). Counts of physical samples were derived from the union of the GGBN Data Portal (GGBN 2011) and the Global Catalogue of Microorganisms (Wu et al. 2013). DNA barcode sequence data counts were downloaded from
GenBank (Clark et al. 2015). Percentages represent the percent of the total in that category.
![taxonomic gap](taxonomic-gap-devine.png)

It is also not just about data findability. There's plenty of data out there. A [2019 assessment](https://doi.org/10.1371/journal.pone.0217084) of the accuracy and reliability of [BOLD](http://www.boldsystems.org/) and [GenBank](https://www.ncbi.nlm.nih.gov/genbank/) highlights issues accuracy and reliability:

> To achieve this, 1) curated reference materials for plants, macro-fungi and insects were obtained from national collections, 2) relevant barcode sequences (rbcL, matK, trnH-psbA, ITS and COI) from these reference samples were generated and used for searching against both databases, and 3) optimal search parameters were determined that ensure the best match to the known species in either database. While GenBank outperformed BOLD for species-level identification of insect taxa (53% and 35%, respectively), both databases performed comparably for plants and macro-fungi (~81% and ~57%, respectively). Results illustrated that using a multi-locus barcode approach increased identification success. This study outlines the utility of the BLAST search tool in GenBank and the BOLD identification engine for taxonomic identifications and identifies some precautions needed when using public sequence repositories in applied scientific disciplines.
> 

Themes: 

1. Data management and curation
2. Service interoperability  
2. Workflow (museums are used to collection based workflows which is very different than DNA barcoding based workflow. Some large museums do both). 
3. Standards and best practices 
4. FAIR (more than just linking the datasets)/ 
5. Integrative approach and idea of extended specimen. 


## Current Technical Landscape 

* Data sources (repository, databases) 
* API 
* linking (knowledge graph). Buildig the [DiSSCo knowledge graph](https://alexhardisty.wordpress.com/2019/07/25/building-the-dissco-knowledge-graph/) (by Alex Hardisty)

The fate of a small marine worm (based on the above knowledge graph) 


![holorchis castex](holorchis-castex.png)


https://data-blog.gbif.org/post/gbif-molecular-data/
https://www.gbif.org/faq?question=how-can-i-publish-molecular-data-to-gbif

### Services 

EBI 
Idenfiers.org 
GBIF-API 


### Species interaction 


Taxon Map 

```
NCBITaxon:7159  Aedes aegypti   GBIF:1651891    Aedes aegypti
NCBITaxon:7159  Aedes aegypti   OTT:269666      Aedes aegypti
NCBITaxon:7159  Aedes aegypti   WD:Q1148004     Aedes aegypti
NCBITaxon:7159  Aedes aegypti   INAT_TAXON:155453       Aedes aegypti
NCBITaxon:7159  Aedes aegypti   IRMNG:10192831  Aedes aegypti
NCBITaxon:7159  Aedes aegypti   ITIS:126240     Aedes aegypti
NCBITaxon:7159  Aedes aegypti   NCBI:7159       Aedes aegypti
NCBITaxon:7159  Aedes aegypti   GBIF:1651891    Aedes aegypti
```



## Standards 

1. [GGBN Data Standard](https://wiki.ggbn.org/ggbn/GGBN_Data_Standard) 
2. [Bioschema](https://bioschemas.org/) 
3. [MOD-CO](https://academic.oup.com/database/article/doi/10.1093/database/baz002/53039720)

>With the advent of advanced molecular meta-omics techniques and methods, a new era commenced for analysing and characterizing historic collection specimens, as well as recently collected environmental samples. Nucleic acid and protein sequencing-based analyses are increasingly applied to determine the origin, identity and traits of environmental (biological) objects and organisms. In this context, the need for new data structures is evident and former approaches for data processing need to be expanded according to the new meta-omics techniques and operational standards. Existing schemas and community standards in the biodiversity and molecular domain concentrate on terms important for data exchange and publication. Detailed operational aspects of origin and laboratory as well as object and data management issues are frequently neglected. Meta-omics Data and Collection Objects (MOD-CO) has therefore been set up as a new schema for meta-omics research, with a hierarchical organization of the concepts describing collection samples, as well as products and data objects being generated during operational workflows. 
https://academic.oup.com/database/article/doi/10.1093/database/baz002/5303972



### Workflow 

https://onlinelibrary.wiley.com/doi/full/10.1111/zsc.12279

https://www.ebi.ac.uk/ena/submit/taxonomy

https://rdrr.io/cran/taxize/man/get_gbifid.html


## Recent Papers 

- [Parasites Lost ](https://doi.org/10.1002/fee.2017)

Parasites lost: using natural history collections to track disease change across deep time. Frontiers in Ecology and the Environment 17: 157– 166.


>"Specimens held in natural history collections represent a chronological archive of life on Earth and may, in many cases, be the only available source of data on historical disease patterns. It is possible to extract information on past disease rates by studying trace fossils (indirect fossilized evidence of an organism's presence or activity, including coprolites or feces), sequencing ancient DNA of parasites, and examining sediment samples, mummified remains, study skins (preserved animal skins prepared by taxidermy for research purposes), liquid‐preserved hosts, and hosts preserved in amber. Such use of natural history collections could expand scientific understanding of parasite responses to environmental change across deep time (that is, over the past several centuries), facilitating the development of baselines for managing contemporary wildlife disease."
>

- [Entomological Collections in the Age of Big Data](https://www.annualreviews.org/doi/full/10.1146/annurev-ento-031616-035536)


- [A DNA barcode library for 5,200 German flies and midges (Insecta: Diptera) and its implications for metabarcoding‐based biomonitoring](https://onlinelibrary.wiley.com/doi/full/10.1111/1755-0998.13022)

> This study summarizes results of a DNA barcoding campaign on German Diptera, involving analysis of 45,040 specimens. The resultant DNA barcode library includes records for 2,453 named species comprising a total of 5,200 barcode index numbers (BINs), including 2,700 COI haplotype clusters without species‐level assignment, so called “dark taxa.” 
...
The present study has three main goals: (a) to provide a DNA barcode library for 5,200 BINs of Diptera; (b) to demonstrate, based on the example of bulk extractions from a Malaise trap experiment, that DNA barcode clusters, labelled with globally unique identifiers (such as OTUs and/or BINs), provide a pragmatic, accurate solution to the “taxonomic impediment”; and (c) to demonstrate that interim names based on BINs and OTUs obtained through metabarcoding provide an effective method for studies on species‐rich groups that are usually neglected in biodiversity research projects because of their unresolved taxonomy.


- [Using taxonomic consistency with semi‐automated data pre‐processing for high quality DNA barcodes](https://besjournals.onlinelibrary.wiley.com/doi/full/10.1111/2041-210X.12824)

