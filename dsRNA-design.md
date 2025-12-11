# **Designing chimeric double stranded RNA (dsRNA) for RNA interference (RNAi)**

### Thomas G. Michaels December 9 2025

RNA interference (RNAi) involves targeted degredation of mRNA transcripts in order to inactivate genes of interest. 
This interest may be to study the loss of function of a certain gene, or to debilitate the organism as a form of biological control.
In this case, we want to silence essential genes leading to death or the impairment of pathogenicity in the nectrotrophic ascomycete fungus *Cryphonectria parasticia*. 
This fungus is the causal organism of the chestnut blight and is responsible for the death of 3-4 billion American chestnut trees (*Castanea dentata*) in the early 20th century.

## Step 1: Identify essential pathways and genes ##
In this case, I want to design chimeric dsRNA templates. Chimeric means multiple genes will be targeted in a singular sequence by combining fragments of the coding sequence from each gene. 
The pathways I have choosen to target are:
1. Chitin synthase - Chitin is an essential component of fungal cell walls. 
2. Vessicle trafficking genes - Required for maintenence of polarized growth and the movement of essential cell cargo.
3. Ergosterol synthesis - Ergosterol is a lipid required for formation of cell membranes in fungi. These pathway has been targeted by conventional chemical pesticides.

These pathways were suggested as targets by this study on the development of Spray-based RNAi in fungal plant pathogens [^1].
[^1]:Mosquera, S., Ginésy, M., Bocos-Asenjo, I.T., Amin, H., Diez-Hermano, S., Diez, J.J., and Niño-Sánchez, J. (2025). Spray-induced gene silencing to control plant pathogenic fungi: a step-by-step guide. J. Integr. Plant Biol. 67: 801–825.

Within these major pathways, there are many genes we can target; a good place to start is to examine other fungal RNAi studies and find which genes were successfully silenced. 
I have listed candidate genes and the source studies below.

| Gene code | Pathway | Citation | Organism |
|---|---|---|---|
| CHS1 | Chitin synthesis | [^2] | *Fusarium circinatum* |
| CHS2 | Chitin synthesis | [^2] | *Fusarium circinatum* |
| CHS3 | Chitin synthesis | [^2] | *Fusarium circinatum* |
| VPS51 | Vessicle trafficking | [^2] | *Fusarium circinatum* |
| DCTN1| Vessicle trafficking | [^2] | *Fusarium circinatum* |
| SAC1 | Vessicle trafficking | [^2] | *Fusarium circinatum* |
| ERG1 | Ergosterol synthesis | [^3] | *Botrytis cinerea* | 
| ERG11 | Ergosterol synthesis | [^3] | *Botrytis cinerea* | 
| ERG13 | Ergosterol synthesis | [^3] | *Botrytis cinerea* | 

[^2]: Spray-Induced Gene Silencing (SIGS) as a Tool for the Management of Pine Pitch Canker Forest Disease. Irene Teresa Bocos-Asenjo, Huma Amin, Sandra Mosquera, Sergio Díez-Hermano, Mireille Ginésy, Julio Javier Diez, and Jonatan Niño-Sánchez. Plant Disease 2025 109:1, 49-62 https://doi.org/10.1094/PDIS-02-24-0286-RE
[^3]: Duanis-Assaf, D., Galsurker, O., Davydov, O., Maurer, D., Feygenberg, O., Sagi, M., Poverenov, E., Fluhr, R. and Alkan, N. (2022) Double-stranded RNA targeting fungal ergosterol biosynthesis pathway controls Botrytis cinerea and postharvest grey mould. Plant Biotechnol. J., https://doi.org/10.1111/pbi.13708

## Step 2: Find gene sequences in target organism ##
Now we need to find the DNA sequences for these genes in C. parasitica.
This will be done using BLAST searches with a translated protein query. 
It is easiest to use protein queries because the translation from amino acid back to nucleotides theoretically does not contain any non-coding DNA, such as Exons or other untranslated regions.
This is essential in order to ensure the dsRNA will actually bind to an actively transcribed region of the target mRNA.

First, find the Protein accession #s listed in the studies.
| Organism | Gene Code | Protein Accession # | Citation |
|---|---|---|---|
| *Fusarium circinatum* | CHS1 | KAF5654678.1 | [^2] |
| *Fusarium circinatum* | CHS2 | KAF5678417.1 | [^2] |
| *Fusarium circinatum* | CHS3 | KAF5658513.1 | [^2] |
| *Fusarium circinatum* | VPS51 | KAF5683607.1 | [^2] |
| *Fusarium circinatum* | DCTN1| KAF5656821.1 | [^2] |
| *Fusarium circinatum* | SAC1 | KAF5666971.1 | [^2] |
| *Botrytis cinerea* | ERG1 | XP_001547476.1 | [^3] |
| *Botrytis cinerea* | ERG11 | XP_001549961.1 | [^3] |
| *Botrytis cinerea* | ERG13 | XP_001552422.2| [^3] |

Unfortunately, it is not always easy to find protein accession #s, as some studies directly extract the target sequences from the organism and sequence the DNA without using reference genomes. However, the RNA template sequence should always be provided somehwere in the study, in which case you may simply need to BLAST the nucelotides. 



Now that we have the protein sequences, it is time to perform a BLASTp search on the JGI annotated C.parasitica genome. The BLASTp search interface can be reached [here](https://mycocosm.jgi.doe.gov/pages/blast-query.jsf?db=Crypa2).

Paste the target protein FASTA sequence into the query box, set the alignment program to blastp: protein vs protein, and set the database to Cryphonectria parasitica v2.0 gene catalog 20091217 (proteins)
