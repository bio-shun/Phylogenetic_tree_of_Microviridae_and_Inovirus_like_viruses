# Phylogenetic_tree_of_Microviridae_and_Inovirus_like_viruses
Phylogenetic trees of environmental Microviridae and inovirus-like viruses were generated based on VP1 and pI, respectively.


###Construction of the phylogenetic tree of environmental Microviridae based on VP1 protein:

##Step1. Collection of VP1 protein sequences from environmental Microviridae
	VP1 sequences (VP1_protein.faa) were collected from several studies on environmental Microviridae (Kirchberger et al. 2022; Yoshida et al. 2013; Malki et al. 2021; Pearson et al. 2016; Quaiser et al. 2015; Bryson et al. 2015). Detailed information on collected VP1 sequences is provided in Table S1 Microviridae.xlsx.
##Step2. Construction of the phylogenetic tree
	Muscle v5.1 (Edgar. 2004) was used to perform sequence alignment with the default mode (muscle -align VP1_protein.faa -output VP1_protein_aln.afa). The alignment was then automatically trimmed using TrimAL v1.4.rev15 (Capella-Gutiérrez et al. 2009), with parameters 'trimal -in VP1_protein_aln.afa -out VP1_protein_aln_trimal_output -automated1'. The tree was generated using Iqtree v2.2.0.3 (Minh et al. 2020), with parameters '-nt AUTO'. The constructed phylogenetic tree model was automatically evaluated, and the most suitable model was selected as the LG+F+R7 model (iqtree -s VP1_protein_aln_trimal_output -bb 1000 -nt AUTO -m MFP -pre output -T 36).
##Step3. Visualization of phylogenetic tree
	iTOL (https://itol.embl.de/) was used to visualize phylogenetic trees (VP1_protein.treefile). iTOL-profile was created based on the information of isolation environments (iTOL_Env.txt) and subfamily assignments (iTOL_Family.txt) of environmental Microviridae (Fig 3-Microviridae Phylogenetic trees.tif).

 
###Construction of the phylogenetic tree of Inovirus-like viruses based on pI proteins:

##Step1. Collection of genome sequences of Inovirus-like viruses
	The genome sequences of environmental Inovirus-like viruses and ICTV-recognized Inovirus-like viruses were collected from Roux et al. 2019 and ICTV database(https://ictv.global/), respectively. Detailed information on collected genome sequences of Inovirus-like viruses is provided in (Table S2 Inovirus-like viruses.xlsx).
##Step2. Identification of pI protein
	Python script (gb_faa.py) was used to extract all protein sequences from the genome sequences of Inovirus-like viruses. The pI proteins (PI_protein.faa) was then identified by HMMER v3.3.2 search (Finn R D et al. 2004) using PI.hmm model established by Roux et al. 2019.
##Step3. Construction of phylogenetic tree
	Alignment was conducted by muscle v5.1(Edgar. 2004) using -super5 mode for fast alignments of large batches of protein sequences (muscle -super5 PI_protein.faa -output PI_proetin_aln.afa). The phylogenetic tree was constructed using FastTree v2.1.11(Price et al.2010) software (FastTree -lg PI_proetin_aln.afa > PI_protein_tree).
##Step4. Visualization of phylogenetic tree
	iTOL (https://itol.embl.de/) was used to visualize phylogenetic trees (PI_protein_tree). iTOL-profile was created based on the information of isolation environments (iTOL_Env.txt) and subfamily assignments (iTOL_Family.txt) of environmental Inovirus-like viruses (Fig 4-Inovirus-like viruses Phylogenetic trees.tif).



Reference:

	Bryson SJ, Thurber AR, Correa AM et al. A novel sister clade to the enterobacteria microviruses (family Microviridae) identified in methane seep sediments. Environ Microbiol. 2015;17:3708-21.

	Capella-Gutiérrez S, Silla-Martínez J M, Gabaldón T. trimAl: a tool for automated alignment trimming in large-scale phylogenetic analyses. Bioinformatics. 2009;25:1972-1973.

	Edgar R C. MUSCLE: a multiple sequence alignment method with reduced time and space complexity. BMC bioinformatics. 2004;5:1-19.

	Finn R D, Clements J, Eddy S R. HMMER web server: interactive sequence similarity searching. Nucleic acids research. 2011;39: 29-37.

	Kirchberger PC, Martinez ZA, Ochman H. Organizing the Global Diversity of Microviruses. Mbio. 2022:13:e00588-22.

	Malki K, Sawaya N A, Tisza M J, et al. Spatial and temporal dynamics of prokaryotic and viral community assemblages in a lotic system (Manatee Springs, Florida). Applied and Environmental Microbiology. 2021;87:e00646-21.

	Minh B Q, Schmidt H A, Chernomor O, et al. IQ-TREE 2: new models and efficient methods for phylogenetic inference in the genomic era. Molecular biology and evolution. 2020;37:1530-1534.

	Pearson VM, Caudle SB, Rokyta DR. Viral recombination blurs taxonomic lines: Examination of single-stranded DNA viruses in a wastewater treatment plant. PeerJ. 2016;4:e2585.

	Price M N, Dehal P S, Arkin A P. FastTree 2–approximately maximum-likelihood trees for large alignments. PloS one. 2010;5:e9490.

	Quaiser A, Dufresne A, Ballaud F et al. Diversity and comparative genomics of Microviridae in Sphagnum-dominated peatlands. Front Microbiol. 2015;6:375.

	Roux S, Krupovic M, Daly RA et al. Cryptic inoviruses revealed as pervasive in bacteria and archaea across Earth’s biomes. Nat Microbiol. 2019;4:1895-906.

	Yoshida M, Takaki Y, Eitoku M et al. Metagenomic analysis of viral communities in (hado) pelagic sediments. Plos One. 2013;8:e57271.
