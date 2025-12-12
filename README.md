# Hifiasm
Genome Assembly Tool

## Downloading software using conda

```bash
conda create -n hifiasm
conda activate hifiasm
conda install -c bioconda hifiasm

# To assemble a PacBio genome

hifiasm -o output.asm -t 30 /path/to/.fastq  --primary

# To assemble the ONT genome

hifiasm -o output.asm --ont -t 30 /path/to/.fastq  

# To remove haplotigs

hifiasm -o output.asm --ont --nhap no_of_individuals_used-t 30 /path/to/.fastq 

# Assemble using multiple FASTQ files

hifiasm -o outpt.asm -t 40 reads1.fastq.gz reads2.fastq.gz reads3.fastq.gz

# Converting output GFA files to a FASTA file

awk '/^S/{print ">"$2"\n"$3}' output.asm.p_ctg.gfa > output.p_ctg.fa
