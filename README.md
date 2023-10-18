# Singularity-def-files
A repository to store the `def` files for creating an singularity image for a given tool.

# How to build the image.
```
sudo singularity build ViPTreeGen__1.1.3.simg VIPTreeGen__1.1.3.def
```
# How to run the image
```
singularity exec ViPTreeGen__1.1.3.simg ViPTreeGen input.fasta output_dir

or

If the following error arises after running the above command
[error]: first argument should be a fasta file.
Then try this

singularity exec -B /path/to/dir/containing/input_file:/mnt ViPTreeGen__1.1.3.simg ViPTreeGen --ncpus 30 /mnt/input.fasta /mnt/output_dir
```
