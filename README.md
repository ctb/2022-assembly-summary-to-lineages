# Extracting taxonomic lineages from NCBI based on assembly_summary files

This tool is used to create files for use with `sourmash tax` and
`sourmash lca index`, for taxonomic summaries.  The tool starts by
taking in an [assembly summary](https://ftp.ncbi.nlm.nih.gov/genomes/README_assembly_summary.txt) file, and ends with an output file
format like so:

```
accession,taxid,superkingdom,phylum,class,order,family,genus,species,strain
AAAC01000001,191218,Bacteria,Firmicutes,Bacilli,Bacillales,Bacillaceae,Bacillus,Bacillus anthracis,
AABL01000001,73239,Eukaryota,Apicomplexa,Aconoidasida,Haemosporida,Plasmodiidae,Plasmodium,Plasmodium yoelii,
AABT01000001,285217,Eukaryota,Ascomycota,Eurotiomycetes,Eurotiales,Aspergillaceae,Aspergillus,Aspergillus terreus,
AABF01000001,209882,Bacteria,Fusobacteria,Fusobacteriia,Fusobacteriales,Fusobacteriaceae,Fusobacterium,Fusobacterium nucleatum,
```

### Snakestart: a snakemake workflow

Install snakemake, and run it:

```snakemake```

This will generate an output file `example.lineages.csv` based
on the input file `example.assembly_summary.txt`.  Note that snakemake
will download all of the necessary support files too!

Code based on https://github.com/dib-lab/2018-ncbi-lineages.

CTB 20.4.2022
