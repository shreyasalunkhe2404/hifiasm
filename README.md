# Hifiasm
Genome Assembly Tool
Downloading software using conda
conda create -n hifiasm
conda activate hifiasm
conda install -c bioconda hifiasm

To assemble a PacBio genome
hifiasm -o output_hifiasm.asm -t 30 /path/to/.fastq  --primary

To assemble the ONT genome
hifiasm -o output_hifiasm.asm --ont -t 30 /path/to/.fastq  

To remove haplotigs
hifiasm -o output_hifiasm.asm --ont --nhap no_of_individuals_used-t 30 /path/to/.fastq 
