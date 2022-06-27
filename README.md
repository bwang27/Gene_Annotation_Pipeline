# Gene_Annotation_Pipeline
1. Set up each configure file, feed input data, evidence data to the .ctl file, and set parameter as needed.

2. Run script ‘run_maker.sh’ to annotate the genomes.

3. Use the following command to create the final merged gff file. The “-n” option would produce a gff file without genome sequences.

gff3_merge -s -n -d genome.maker.output/genome_master_datastore_index.log>genome.noseq.gff

4. Generate AED plots.
/programs/maker/AED_cdf_generator.pl -b 0.025 chr1.noseq.gff > AED_rnd3
Plot the file AED_rnd3 in Excel or any plotting software. 

5. Load the gff file into IGV or JBrowse. Instructions for IGV and JBrowse can be found at:
IGV: http://software.broadinstitute.org/software/igv/UserGuide
JBrowse: https://biohpc.cornell.edu/lab/userguide.aspx?a=software&i=357#c




