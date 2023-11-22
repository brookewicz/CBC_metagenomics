# CBC_metagenomics
Code notebook for analyzing Stony Coral Tissue Loss Disease in the Caribbean
- script based on Thijs's workflow: https://github.com/ThijsSt/SCTLD-metagenomes

Analyzing mcav seqs from CBC, Belize

### Workflow
#### 1. Assembly 
- Assembles contigs to metagenome-assembled genome (MAG) from quality controlled F & R seq files. 
#### 2. Mapping
- Quality control using metaquast. Aligns reads to MAG.
#### 3. Binning
#### 4. Anvio - taxonomy and data analysis 
 - Binning and Anvio are not complete - trying to decide how to complete the binning step (within or independently of anvio)

#### Misc
### Symbiont sequencing (ITS2_seqs)
- Starts at assembled and fixed contig fasta file from Step 1: Assembly. Use cutadapt to trim sequences in the ITS2 regions to target symbiont sequences. Output is aligned fastq files for each sample to input to symbioportal

