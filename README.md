# SARS-CoV-2_DDGA
A SARS-CoV-2 Drug Disease Gene Association Dataset

Introduction
------------

Inspired by the White House Office of Science and Technology Policy
machine-readable Coronavirus literature collection<sup>4</sup>, we noticed a lack
of high quality, machine-readable datasets that contained information on
drug, gene, and disease associations for SARS-CoV-2. We decided to build
and release an open-source dataset for the community to explore two key
questions:

1.  What existing drugs have interaction potential with SARS-CoV-2?

2.  What diseases and symptoms overlap with target genes that have interaction potential with SARS-CoV-2?

To address this, we compiled an integrated dataset from the following
publications and resources:

-   A SARS-CoV-2-Human Protein-Protein Interaction Map Reveals Drug Targets and Potential Drug-Repurposing<sup>1</sup>

    -   Tagged, cloned and expressed 26 of 29 SARS-CoV-2 proteins in human cells. Human proteins that were physically associated with viral proteins were identified using affinity purification mass spectrometry

-   The Drug Repurposing Hub: a next-generation drug library and information resource<sup>2</sup>

    -   Hand curated collection of 4,707 compounds with literature-reported gene targets

-   The DisGeNET knowledge platform for disease genomics: 2019 update<sup>3</sup>

    -   Standardized database of disease associated genes and phenotypes from multiple sources

Dataset Description
-------------------

Our integrated dataset links 332 human genes which encode proteins that
interact with tagged SARS-CoV-2 proteins in human cells to 181
drug/chemical compounds (and associated SMILES) and 953 diseases. The
columns that can be found in the integrated dataset are described below.
The source dataset for each column is indicated in the superscript.

The data is made available as a single, integrated zipped .csv file.

Column Name | Description
--- | ---
Bait-Prey Information (Bait)<sup>1</sup> | Tagged viral expressed protein
Preys<sup>1</sup> | Identifier for the prey gene
PreyGene<sup>1</sup> | Gene corresponding to the associated human protein identified as an interactor with a tagged viral protein. This is a key join column that links all of the drug, gene, protein, and disease information together.
MIST<sup>1</sup> | Protein-protein interaction score as computed by MiST (MassSpectrometry interaction statistics)
Saint\_BFDR<sup>1</sup> | False discovery rate as computed by SAINTexpress(Significance Analysis of INTeractome software)
AvgSpec<sup>1</sup> | Average spectral counts
Uniprot Protein Description<sup>1</sup> | Description of host protein from Uniprot database
Uniprot Protein Function<sup>1</sup> | Function of host protein from Uniprot database
Structures (PDB)<sup>1</sup> | Three-dimensional structural database for large biological molecules
Uniprot Function in Disease<sup>1</sup> | Function in disease of host protein from Uniprot database
Drug<sup>2</sup>/Compound<sup>1</sup> | Name of drug or compound
Drug Status<sup>2</sup> | Drug development stage(eg. Preclinical, Clinical Trial, Approved)
Pubchem\_cid<sup>2</sup> | Pubchem ID of drug
SMILES<sup>1,2</sup> | SMILES of drug or compound
ZINC\_ID<sup>1</sup> | ZINC database ID
Broad\_id<sup>2</sup> | Broad Institute identifier for the drug
Pert\_iname<sup>2</sup> | The internal (CMap-designated) name of a perturbagen. By convention, for genetic perturbations CMap uses the HUGO gene symbol
Purity<sup>2</sup> | Purity of drug
Expected mass<sup>2</sup> | Expected mass of drug
InChIKey<sup>2</sup> | International Chemical Identifier of compound
Pathway<sup>1</sup> | Name of associated pathway from gene
DSI<sup>3</sup> | Disease specificity index
DPI<sup>3</sup> | Disease pleiotropy index
diseaseName<sup>3</sup> | Name of the disease
diseaseType<sup>3</sup> | DisGeNET disease type: disease, phenotype and group
diseaseSemanticType<sup>3</sup> | UMLS Semantic Type(s) of the disease
Score<sup>3</sup> | DisGENET score for the Gene-Disease association
CAS number<sup>5</sup> | Unique numerical identifier assigned by the Chemical Abstracts Service (CAS) to every chemical substance described in the open scientific literature
year of approval<sup>5</sup> | Year drug approved
Status<sup>5</sup> | Label if the drug is discontinued
routes of administration<sup>5</sup> | Route of administration 
Volume of distribution (VD)<sup>5</sup> | Distribution volume in liters
Clearance (Cl)<sup>5</sup> | volume of blood, serum, or plasma completely cleared of drug per unit of time (liter/hour)
Plasma Protein Binding (PPB)<sup>5</sup> | Plasma proteein binding assay
Half-life (t1/2)<sup>5</sup> | Half-life in 
F<sup>5</sup> | Bioavailability as a percetnage
Cmax<sup>5</sup> | maximum (or peak) serum concentration
Cmax Unit<sup>5</sup> | units of maximum (or peak) serum concentration
Tmax<sup>5</sup> | time at which Cmax is attained in hours
comment on solubility<sup>5</sup> | Solubility of drug


Future Work and Next Steps
--------------------------

We are looking for additional collaborators that are interested in a
targeted expansion of this dataset to other data related to SARS-CoV-2
and therapeutic candidates. Specifically, this dataset will next be
expanded to include homologous SARS-CoV genes and their interactions
with host proteins. This will allow us to understand the specificity of
prey genes and potential therapeutics between SARS-CoV and SARS-CoV-2.
We will further curate additional disease-symptom associations to
discover molecular links to the wide range of symptoms across hosts.

This dataset will be versioned and regularly updated as new information
about SARS-CoV-2 becomes available.

References
-----------

1\. Gordon, David E., et al. \"A SARS-CoV-2-Human Protein-Protein
Interaction Map Reveals Drug Targets and Potential Drug-Repurposing.\"
BioRxiv (2020).

2\. Corsello, Steven M., et al. \"The Drug Repurposing Hub: a
next-generation drug library and information resource.\" Nature medicine
23.4 (2017): 405-408.

3\. Piñero, Janet, et al. \"The DisGeNET knowledge platform for disease
genomics: 2019 update.\" Nucleic acids research 48.D1 (2020): D845-D855.

4\. "CORD-19: Semantic Scholar." *CORD-19 \| Semantic Scholar*, pages.semanticscholar.org/coronavirus-research.

5\. 
