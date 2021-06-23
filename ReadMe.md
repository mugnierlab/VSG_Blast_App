## VSG Blast Shiny App

Quick Note: As of now this App only runs locally because it relies on BLAST being installed locally. 

Link to live App ( broken :( ):  https://abeav.shinyapps.io/final_project/

Link to video: https://drive.google.com/file/d/1vU3dod60CzUl2H2YgBEne2gtHtjWAAxv/view?usp=sharing

This app allows users to specifically BLAST, blastn and blastp, inputed sequences against all Variant Surgace Glycoproteins that have been sequenced (to our knowledge).This blast app uses a database of ~13,000 complete and partial VSGs. The database includes all VSG CDSs and protein sequences form all Trypanasoma species and from all available source. In addition, this database includes unpublished contigs assembled from PacBio sequencing of the EATRO 1125 strain of Trypanosoma brucei. 

These sequences were compiled and annotated by George Cross and his research group at The Rockefeller University. His website and research can be found [here](https://tryps.rockefeller.edu/).

### Usage

To run this app, first make sure you have BLAST and all the R packages installed. Open the RMD file and run the document, you can open this in a browser window. This app has a text input that users can put in one or more sequences in fasta format. You can select the blast type, either blastn or blastp. Blast results will appear in a table format at the top, the number of total hits per input sequence will appear in the bottom left, and a histogram of the results will appear in the bottom right. Finally, the user can download the blast results as a csv file using the download button. The tab at the top labeled "VSG Sequence Info" has additional information about the VSG database and how these sequences were compiled. 

### Dependencies 

* To run this app you must have blast downloaded locally. Follow NCBI's installation instructions [here](https://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download) 

    * You can also install blast via conda at the command line `conda install -c bioconda blast`
    
* This app also relies on several R Bioconda packages (Biostrings and BoicGenerics). 
    * `install.packages("BiocManager")`
    * `BiocManager::install("BiocGenerics")`
    * `BiocManager::install("Biostrings")`
    
* The app also uses an R package from github, [rBLAST](https://github.com/mhahsler/rBLAST). 
    * `devtools::install_github("mhahsler/rBLAST")`
    
### Sequence Sources

All DNA and protein sequence fastas can be downloaded [here](https://tryps.rockefeller.edu/Sequences.html). This website also has additional information about Trypanasoma strains and sequencing sources. 