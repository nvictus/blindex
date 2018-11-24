# assebliotheque

Inspired by https://github.com/dpryan79/ChromosomeMappings.

1. [Find the ftp directory](https://www.ncbi.nlm.nih.gov/genome/doc/ftpfaq/#howtofind) of your favorite reference assembly. The field named "ftp_path" provides the path to the FTP directory containing the data for each assembly. Find the appropriate file with the assembly summary.

* Either the two master assembly summary files:
	- ftp://ftp.ncbi.nlm.nih.gov/genomes/ASSEMBLY_REPORTS/assembly_summary_genbank.txt
	- ftp://ftp.ncbi.nlm.nih.gov/genomes/ASSEMBLY_REPORTS/assembly_summary_refseq.txt
* Or an assembly summary file for a taxonomic group from the appropriate directory under genbank or refseq. e.g.
	- ftp://ftp.ncbi.nlm.nih.gov/genomes/genbank/bacteria/assembly_summary.txt
* Or an assembly summary file for a species from the appropriate directory under genbank or refseq. e.g.
	- ftp://ftp.ncbi.nlm.nih.gov/genomes/genbank/bacteria/Salmonella_enterica/assembly_summary.txt

2. Take the commented metadata and convert it into a `{assembly}.yaml` file. Normalize the property names to those in GRCh38.

3. Extract the columns in into a `{assembly}` TSV file and normalize the column names to those in GRCh38. If chromosome lengths are not available, you can get them from UCSC and join them into the table.


## Chromosome order

Ordered naturally by chromosome/plasmid.
Fully **assembled** chromosomes/plasmids are followed by **unlocalized** scaffolds, followed by **unplaced** scaffolds, followed by **alt** scaffolds.


## Patch releases

Do not include patch sequences! F that noise.


## TODO

* yaml and table validator scripts
