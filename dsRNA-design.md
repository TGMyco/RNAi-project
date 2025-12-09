# **Designing double stranded RNA (dsRNA) for RNA-directed transcriptional silencing of RNA interference (RNAi) pathway genes**

### Thomas G. Michaels December 9 2025

RNA interference (RNAi) involves targeted degredation of mRNA transcripts in order to inactivate genes of interest. 
This interest may be to study the loss of function of a certain gene, or to debilitate the organism as a form of biological control.
In this case, we want to silence essential genes leading to  death or the impairment of pathogenicity in the nectrotrophic ascomycete fungus *Cryphonectria parasticia*. 
This fungus is the causal organism of the chestnut blight and is responsible for the death of 3-4 billion American chestnut trees (*Castanea dentata*) in the early 20th century.

## Step 1: Identify essential pathways and genes ##
In this case, I want to design chimeric dsRNA templates that will combine multiple target genes involved in essential pathways, including:
1. Chitin synthase - Chitin is an essential component of fungal cell walls
2. Vessicle trafficking genes - Required for maintenence of polarized growth and the movement of essential cell cargo.
3. Ergosterol synthesis - Ergosterol is a lipid required for formation of cell membranes in fungi. These pathway has been targeted by conventional chemical pesticides.

These pathways were suggested as targets by this study on the development of Spray-based RNAi in fungal plant pathogens [^1].
[^1]:Mosquera, S., Ginésy, M., Bocos-Asenjo, I.T., Amin, H., Diez-Hermano, S., Diez, J.J., and Niño-Sánchez, J. (2025). Spray-induced gene silencing to control plant pathogenic fungi: a step-by-step guide. J. Integr. Plant Biol. 67: 801–825.

This study includes links to case studies where specific genes in these pathways were targeted for RNAi. To start we will identify potential target genes from other studies

| Gene code | Pathway | Citation | Organism |
|---|---|---|---|
| CHS1 | Chitin synthesis | [^2] | Fusarium circinatum |
| CHS2 | Chitin synthesis | [^2] | Fusarium circinatum |
| CHS3 | Chitin synthesis | [^2] | Fusarium circinatum |
| VPS51 | Vessicle trafficking | [^3] | Multiple pathogens |
| DCTN1| Vessicle trafficking | [^3] | Multiple pathogens |
| SAC1 | Vessicle trafficking | [^3] | Multiple pathogens |
| ERG1 | Ergosterol synthesis | [^4] | Botrytis cinerea | 
| ERG11 | Ergosterol synthesis | [^4] | Botrytis cinerea | 
| ERG13 | Ergosterol synthesis | [^4] | Botrytis cinerea | 

[^2]: Spray-Induced Gene Silencing (SIGS) as a Tool for the Management of Pine Pitch Canker Forest Disease. Irene Teresa Bocos-Asenjo, Huma Amin, Sandra Mosquera, Sergio Díez-Hermano, Mireille Ginésy, Julio Javier Diez, and Jonatan Niño-Sánchez. Plant Disease 2025 109:1, 49-62 https://doi.org/10.1094/PDIS-02-24-0286-RE
[^3]: Qiao, L., Lan, C., Capriotti, L., Ah-Fong, A., Nino Sanchez, J., Hamby, R., Heller, J., Zhao, H., Glass, N. L., Judelson, H. S., Mezzetti, B., Niu, D. and Jin, H. (2021) Spray-induced gene silencing for disease control is dependent on the efficiency of pathogen RNA uptake. Plant Biotechnol. J., https://doi.org/10.1111/pbi.13589
[^4]: Duanis-Assaf, D., Galsurker, O., Davydov, O., Maurer, D., Feygenberg, O., Sagi, M., Poverenov, E., Fluhr, R. and Alkan, N. (2022) Double-stranded RNA targeting fungal ergosterol biosynthesis pathway controls Botrytis cinerea and postharvest grey mould. Plant Biotechnol. J., https://doi.org/10.1111/pbi.13708

## Step 2: Find gene sequences in target organism ##
Now we need to find the DNA sequences for these genes in C. parasitica
The reference genome for C. parasitica is available on Genbank. To find it go to [NCBI Genomic datasets site](https://www.ncbi.nlm.nih.gov/datasets/genome/) and search by the organism name.

There are 2 methods we can use to find the genes. The first is via a keyword search
1. Go to the [Mycocosm page for C. parasitica strain EP155](https://mycocosm.jgi.doe.gov/Crypa2/Crypa2.home.html)
2. Click on "Search" on the top menu ribbon
3. You can search for the exact name, or set the search terms to "Prefix" and enter the letters
4. 

The second method is to Blast search the reference genome for similar sequences.sequence similarity; this requires the sequences of the targets used in the other fungal RNAi studies.
