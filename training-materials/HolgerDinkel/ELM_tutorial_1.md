---
title: "Short Linear Motifs and the Eukaryotic Linear motif resource"
author: Toby Gibson, Manjeet Kumar & Holger Dinkel
geometry: margin=2cm
---



**Resources**:


- ELM <http://elm.eu.org>
- UniProt <http://www.uniprot.org/>
- PeCan <https://pecan.stjude.cloud/proteinpaint/>
- ProViz <http://proviz.ucd.ie>

# ELM exercises

**Objective**: Get familiar with the ELM (Eukaryotic Linear Motif) prediction tool.

## Search in ELM by copy/pasting the following sequence and using the following parameters:

> \>P12931
> 
> MGSNKSKPKDASQRRRSLEPAENVHGAGGGAFPASQTPSKPASADGHRGPSAAFAPAAAE
> PKLFGGFNSSDTVTSPQRAGPLAGGVTTFVALYDYESRTETDLSFKKGERLQIVNNTEGD
> WWLAHSLSTGQTGYIPSNYVAPSDSIQAEEWYFGKITRRESERLLLNAENPRGTFLVRES
> ETTKGAYCLSVSDFDNAKGLNVKHYKIRKLDSGGFYITSRTQFNSLQQLVAYYSKHADGL
> CHRLTTVCPTSKPQTQGLAKDAWEIPRESLRLEVKLGQGCFGEVWMGTWNGTTRVAIKTL
> KPGTMSPEAFLQEAQVMKKLRHEKLVQLYAVVSEEPIYIVTEYMSKGSLLDFLKGETGKY
> LRLPQLVDMAAQIASGMAYVERMNYVHRDLRAANILVGENLVCKVADFGLARLIEDNEYT
> ARQGAKFPIKWTAPEAALYGRFTIKSDVWSFGILLTELTTKGRVPYPGMVNREVLDQVER
> GYRMPCPPECPESLHDLMCQCWRKEPEERPTFEYLQAFLEDYFTSTEPQYQPGENL

-   Cell Compartment: **Not specified**

-   Motif Probability Cutoff: **100**

-   Context information: **(leave blank)**

1.  Pay attention to many instances you find
1.  What can you say about the structure of the protein?

    a.  Do you find any domains?
    a.  Do you find any disordered regions?

## Repeat the previous search (again accession P12931) using these parameters:

-   Cell Compartment: **cytosol**

-   Motif Probability Cutoff: **0.01**

-   Context information: **Homo sapiens**

1.  How many instances (roughly) do you find now?
1.  How many of the instances are \'annotated\'?
1.  Do the structural predictors/filters (SMART, GlobPlot, IUPRED,
    Secondary Structure) agree in terms of which regions are
    structured/disordered?
1.  Compare the location of the annotated instances with structural
    information at hand (IUPRED, Secondary Structure).

## Submit the sequence of Paxillin (P49023) to ELM, using default parameters.

1.  Compare the results with a search for the same sequence when using
    the cellular compartment 'plasma membrane'

## Search protein SRC\_MOUSE (P05480) for ELMs.

1.  Do you find "annotated instances"?
1.  If not, what's the closest to an 'annotated instance' that you can
    find? Investigate where this information might come from.

## Submit the entry name \'P53\_HUMAN\'

1.  Do the cell compartments make sense?
1.  How many degrons are there in p53?
1.  Is there a CDK site in p53? Is there a Cyclin Box in p53?

## (Optional) Search ELM using the protein name \'MDM4\_HUMAN\' and look for the \'USP binding motif\' DOC\_USP7\_MATH\_1.

1.  How many such motif instances are found in this protein sequence?

## (Optional) Repeat this exercise with protein \'AMPH\_HUMAN\' and ELM class \'LIG\_Clathr\_ClatBox\_1\'

1.  Try to assess the biological relevance of each of these instances.
1.  Is the annotation for the biological relevance in accordance with
    the globular structure?

## You're studying the cell surface expression of a receptor and find out that some isoforms are expressed at the surface (Q05586-2) while another isoform is retained in the endoplasmatic reticulum (Q05586-5). You want to investigate a possible role of linear motifs in this phenomenon.

1. First, align these sequences to see which parts are similar/identical and which are different (go to http://www.uniprot.org/uniprot/Q05586, scroll down to 'sequences', select isoforms 2 and 5 and click 'align').
1. Then use http://elm.eu.org to scan these sequences for linear motifs, using cell compartment filter 'cytosol'. You're looking for targeting motifs (TRG\_\*).
1. By looking through the annotations of these targeting ELM classes, can you find motif instances that might be responsible for the different behaviour of the isoforms?
1. If there are multiple instances of that motif found per protein, can you use differential information (comparing the motifs found in the different isoforms) to narrow down the number of candidate instances?
1. Next, you sequence another isoform (Q05586-4) which also features this motif at a homologous position, but strangely does not get expressed at the cell surface. You discuss this with your colleague and he tells you that he recently found out that this protein also binds to the PDZ domain of DLG4. Can you come up with a hypothesis how this all fits together?


# PeCan exercise

## Go to [ELM](http://elm.eu.org/searchdb.html) and enter ETV1\_HUMAN as search term in the search box on top right; you should find a single annotated true positive instance of a degron. 

1. Where/What ELM class is it? Note down it's amino acid position.

Next go to [PeCan](https://pecan.stjude.cloud/proteinpaint/) and enter ETV1 as search term. 

1. Do you find any pediatric mutations? 
1. How about Cosmic? Select only "Fusion transcript" mutations; can you find any near the degron motif? 
1. Which tissue types are these mutations found in? 
1. Are there differences in fusions and frameshifts in tissue types?

## Go to [ELM](http://elm.eu.org/searchdb.html) and enter NOTC1\_HUMAN as search term. 

1. Find the annotated FBW7 degron (TP) and note down its position.

## Now go to [PeCan](https://pecan.stjude.cloud/proteinpaint/) and enter notch1 as search term. 
Select only "Frameshift" and "nonsense" mutations; if possible load COSMIC data as well; 
analyse the area around the degron; additionally, by adding "missense" is there another hotspot?



# ProViz exercise

ProViz aggregates and displays useful information from many resources
where relevant to linear motif discovery.

## Go to the **ProViz server** [http://proviz.ucd.ie](http://proviz.ucd.ie) and put p53 into the "Search for a Protein" field

1. Explore the results, then check out these operations and questions:
   1. Are there any methyllysine modifications?
   1. What is a cumulative switch?
   1. Are there any motifs in p53 than can antagonise MDM2 ubiquitination?
   1. Are there any splice variants in the DNA-binding domain? Do any motifs get removed in splice variants? Do you think p53 researchers study all the splice variants?
   1. What do the long structure modules correspond to?
   1. Can tetrameric p53 be exported from the nucleus?
   1. Click on the structure element of a short segment of p53. It goes to the PDB website (RCSB). Display the structure in the browser and adjust the viewing controls.  
   1. What is the difference between mutagenesis sites and sequence variants?
   1. Which residue has the most sequence variants listed?
   1. Are there any sequence variants in the MDM2 degron (towards the N-terminus)?

