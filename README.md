# CBC_metagenomics
Code notebook for analyzing Stony Coral Tissue Loss Disease in the Caribbean
- script based on Thijs's workflow: https://github.com/ThijsSt/SCTLD-metagenomes

Analyzing shotgun seqs from CBC, Belize 2019-2024

### Workflow
#### 0. Quality control
- qc using trim galore and multiqc for vis
- removal of coral host, symbiont, and human dna 
#### 1. Assembly 
- De novo co-assembly: Assembles quality controlled F & R seq files of like samples into longer contigs 
#### 2. Mapping
- Quality control using metaquast. Aligns reads to contigs.
#### 3. Binning
- Group similar contigs into metagenome-assembled genomes (MAGs)
#### 4. Taxonomy
 - Use Kraken2 to complete taxonomic profiling of short reads
 - (In progress): use Anvio to visualize and ID MAGs (bins)

### all_sctld
- sctld metagenomics analysis with full sample set. all other folders correspond to prelim analysis
- follows general workflow
#### sampleinfo
- sample metadata, sample tables, and checks (md5check sum for seq corruption, and confirming that we got all sequences that we sent)
#### read-counts
- read counts from all steps
- *currently have only collected read counts from raw -> host & symbiont removal*
#### 0QC_trimming-all
#### 1Assembly-all
- removal of coral host, symbiont, and human dna
- de novo co-assembly 
#### 2Taxa-Kraken-all
- Batch scripts for running kraken and bracken (short read alignment to NCBI databases)
#### 2.1OTUtable
- used bracken output to make otu table and normalize

