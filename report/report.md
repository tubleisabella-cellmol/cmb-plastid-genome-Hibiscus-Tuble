# Plastid Genome Characterization: *Hibiscus syriacus*

**Student:** Isabella Tuble

**Course/Section:** Cell and Molecular Biology, A

**Galaxy history:** Plastid_Hibiscus_Tuble

**Galaxy tool:** Fasta Statistics (usegalaxy.org)

**Date analysed:** 30 September 2026

## Summary

| Item | Value |
|---|---|
| Genus and species | *Hibiscus syriacus* L. |
| Family | Malvaceae |
| Accession | NC_026909.1 (RefSeq, provisional) |
| Genome size | 161,019 bp |
| GC content | 36.83% |
| Topology | Circular |
| LSC / SSC / IR (each) | 89,698 bp / 19,831 bp / 25,745 bp |
| Annotated genes in the RefSeq feature table | 99 unique (78 protein-coding, 21 tRNA); rRNA genes not annotated in the table |
| Notable features | Trans-spliced *rps12*, 11 other protein-coding genes with introns, no pseudogenes annotated |

The full summary table and gene lists are in `results/plastome_summary.md`. Galaxy output is in `results/galaxy_statistics.txt` and the screenshot is in `figures/`.

## Q1. Organism and record

- **Organism:** *Hibiscus syriacus* L.

- **Family:** Malvaceae (subfamily Malvoideae, order Malvales)

- **Accession/version:** NC_026909.1 (NCBI RefSeq, marked provisional; the reference sequence is identical to GenBank KP688069)

- **Database:** NCBI Nucleotide / RefSeq

- **Complete plastid genome size:** 161,019 bp

- **Genome report:** *The complete chloroplast genome sequence of Hibiscus syriacus*, Mitochondrial DNA Part A 27(5), 2016, doi:10.3109/19401736.2015.1079847

- **GenBank submitters:** Kim J.-H., Lee H., Kwon H.-Y. and Kim S.-H., Korea Forest Research Institute

## Q2. Evidence that this is a complete plastid genome

- The record is a single circular molecule of 161,019 bp. This is a typical plastome size, and it is far larger than a barcode marker such as *rbcL* or *matK*.

- The source feature is labelled `/organelle="plastid:chloroplast"`, and the record states "COMPLETENESS: full length".

- It carries the standard plastid gene set: photosystem genes (*psaA*, *psbA*), *rbcL*, *atp* and *pet* genes, *rpo* genes, ribosomal proteins and tRNAs. A nuclear fragment would not contain this combination.

- The genome has the LSC-IR-SSC-IR structure, and the region sizes add up exactly to the genome length (see Q3).

- Galaxy Fasta Statistics reported 1 sequence, 161,019 bp, 0 N bases and 0 gaps. The genome is therefore one continuous record, not a set of fragments.

## Q3. Genome organization

The plastome has the typical quadripartite LSC-IR-SSC-IR arrangement. The GenBank record does not annotate the regions, so the sizes below are taken from the genome report for this sequence (Mitochondrial DNA Part A 27(5), 2016, doi:10.3109/19401736.2015.1079847).

| Region | Size (bp) |
|---|---|
| Large single copy (LSC) | 89,698 |
| Small single copy (SSC) | 19,831 |
| Inverted repeat (IR), each copy | 25,745 |
| Total | 161,019 |

Check: 89,698 + 19,831 + 2 × 25,745 = 161,019 bp, which matches the length reported by Galaxy.

Gene positions in the GenBank record fit this layout. *psbA*, *rbcL* and the *psb*/*pet* clusters lie in the LSC (about positions 1-89,698), and so do *ndhJ*, *ndhK* and *ndhC*. *ycf2* lies in the first IR. *ndhA*, *ndhD*-*ndhI*, *psaC*, *ccsA*, *rpl32* and *rps15* lie in the SSC. *rps7*, *ndhB*, *rpl23* and *rpl2* lie in the second IR. The region boundaries are approximate (about 89,699-115,443 for the first IR, 115,444-135,274 for the SSC and 135,275-161,019 for the second IR), calculated from the published sizes. *rps19* crosses the LSC/IR boundary and *ycf1* crosses the IR/SSC boundary.

## Q4. Gene content

| Category | Count |
|---|---|
| Gene records in the feature table | 100 (99 unique names; *rps12* has two records because it is trans-spliced) |
| Unique protein-coding genes | 78 |
| tRNA genes | 21 |
| rRNA genes | none in this record's feature table; 4 reported in the genome report |
| Pseudogenes | none annotated |

Protein-coding genes by functional group:

| Group | Genes | Count |
|---|---|---|
| Photosystem I (*psa*) | *psaA, B, C, I, J* | 5 |
| Photosystem II (*psb*) | *psbA, B, C, D, E, F, H, I, J, K, L, M, N, T, Z* | 15 |
| ATP synthase (*atp*) | *atpA, B, E, F, H, I* | 6 |
| Cytochrome b6f (*pet*) | *petA, B, D, G, L, N* | 6 |
| Rubisco | *rbcL* | 1 |
| RNA polymerase (*rpo*) | *rpoA, B, C1, C2* | 4 |
| Small subunit ribosomal proteins (*rps*) | *rps2, 3, 4, 7, 8, 11, 12, 14, 15, 16, 18, 19* | 12 |
| Large subunit ribosomal proteins (*rpl*) | *rpl2, 14, 16, 20, 22, 23, 32, 33, 36* | 9 |
| NADH dehydrogenase (*ndh*) | *ndhA-K* (*ndhF* is labelled "ndh5" in the record) | 11 |
| Other conserved genes | *matK, clpP, accD, cemA, ccsA, ycf1, ycf2, ycf3, ycf4* | 9 |

The genome report lists 114 genes (81 protein-coding, 4 rRNA and 29 tRNA), which is more than the 78 protein-coding and 21 tRNA genes in the RefSeq feature table. The difference most likely reflects genes in the IR regions that are missing from this record's annotation. A later study of a related *H. syriacus* cultivar ('Mamonde', 161,025 bp) reports 131 genes (86 coding, 8 rRNA and 37 tRNA) and states that IR annotation had been missed in the earlier report.

Genes located in the inverted repeats appear in two copies because the IR is a duplicated segment of DNA. Every gene inside it is present once in each IR copy. This record lists only one copy of most IR genes, so its counts are lower than published totals.

## Q5. Protein-coding genes and their functions

| Gene | Functional group | Function |
|---|---|---|
| *psbA* | Photosystem II | D1 reaction-center protein that carries the electron-transfer cofactors of PSII |
| *psaA* | Photosystem I | P700 apoprotein A1, a core subunit of the PSI reaction center |
| *atpB* | ATP synthase | CF1 beta subunit, part of the catalytic head that makes ATP |
| *petB* | Cytochrome b6f | Cytochrome b6, a core subunit of the complex that passes electrons between PSII and PSI |
| *rbcL* | Carbon fixation | Large subunit of Rubisco, the enzyme that fixes CO2 in the Calvin cycle |
| *rpoB* | Transcription | Beta subunit of the plastid-encoded RNA polymerase |
| *rpl2* | Translation | Ribosomal protein L2 of the large subunit of the plastid ribosome |
| *matK* | RNA processing | Maturase that helps splice group II introns |
| *clpP* | Protein turnover | Proteolytic subunit of the Clp protease |
| *accD* | Lipid metabolism | Carboxyltransferase beta subunit of acetyl-CoA carboxylase (fatty acid synthesis) |

## Q6. RNA and RNA-processing features

- **rRNA genes:** plastomes normally carry four rRNA genes (*rrn16*, *rrn23*, *rrn4.5*, *rrn5*) that form the plastid ribosome. They are not listed in this record's feature table, but the genome report lists 4 rRNA genes. I therefore treat their absence from the table as an annotation gap, not as a real absence.

- **tRNA examples:** *trnH-GUG*, *trnK-UUU*, *trnL-UAA*, *trnV-UAC*, *trnfM-CAU* and *trnW-CCA* (21 tRNA genes in the table).

- **Genes with introns (protein-coding):** *clpP* and *ycf3* have two introns each. *rps16*, *atpF*, *rpoC1*, *petB*, *petD*, *rpl16*, *rpl2*, *ndhA* and
*ndhB* have one intron each.

- **tRNAs with introns:** *trnK-UUU*, *trnL-UAA* and *trnV-UAC*. The *trnK-UUU* intron contains the *matK* gene, which encodes a maturase used in intron
splicing.

- **Other RNA processing:** *rps12* is trans-spliced. Its exons are in separate places in the genome (one in the LSC and one in each IR copy) and are joined at the RNA level. *ndhD* is flagged in the record for RNA editing.

## Q7. Pseudogenes, gene losses, duplications and other unusual features

- **Pseudogenes:** none are annotated in this record.

- **Trans-splicing:** *rps12* is trans-spliced, with a 114 bp exon in the LSC and a 243 bp exon in each IR copy.

- **Duplications:** IR genes are duplicated by nature of the IR, but this record annotates only one copy of most of them.

- **Incomplete annotation:** the feature table has no rRNA genes, and two long stretches carry almost no annotation: about positions 98,800-120,900 (only an *rps12* exon at about 103.7-104.0 kb) and about 135,900-147,600 (only an *rps12* exon at about 146.8-147.0 kb). These stretches cover IR sequence, where the rRNA operon and several tRNA genes would be expected, so I treat them as an annotation gap. This is my interpretation and I did not confirm it against another annotation.

- ***ycf1*:** only a 618 bp piece of *ycf1* is annotated, near the IR/SSC border. The full gene is much longer, and the record does not mark this piece as a pseudogene.

- **Missing gene:** *infA* is not annotated.

- **Label inconsistencies:** *rpl16* carries the product "ribosomal protein S16", *trnT-GGU* is labelled *trnI-GGU*, and *ndhF* is named "ndh5".

- **Record status:** the RefSeq is marked provisional and has not had a final NCBI review.

## Q8. GC content and observations

- **GC content:** 36.83% (Galaxy Fasta Statistics; G + C = 59,303 of 161,019 bases).

- **Observation 1:** the genome is AT-rich (63.17% A+T). This is typical of plastomes and is close to the 36.8% reported in the original *H. syriacus* genome report and the 36.9% reported for *H. coccineus*.

- **Observation 2:** GC content is not evenly spread across the four regions. Studies of closely related *Hibiscus* plastomes report the IR regions as the most GC-rich (about 42.6-42.8%) and the SSC as the most AT-rich (about 31.1-31.5%), with the LSC in between (about 34.7%). The high IR value is commonly attributed to the GC-rich rRNA genes that lie in the IR. These regional values come from the related *H. syriacus* 'Mamonde' and *H. taiwanensis* plastomes, not from my own accession, because my Galaxy result covers the whole genome only.

- **Additional feature from the annotation:** the record retains the full set of NADH dehydrogenase genes (11 annotated, *ndhA-ndhK*), so no *ndh* gene loss is evident in this plastome. Many genes (for example *clpP*, *ycf3* and *rpl2*) are also split by introns.

## Q9. Plastid and mitochondrial genomes compared

**Similarities**

1. Both are organellar genomes of endosymbiotic origin. Plastids derive from a cyanobacterial ancestor and mitochondria from an alpha-proteobacterial ancestor.

2. Both are found outside the nucleus, inside double-membrane organelles, and are inherited outside the nuclear (Mendelian) system.

3. Both are small compared with the nuclear genome and encode only part of the organelle's proteins. Most organellar proteins are encoded in the nucleus and imported.

4. Both encode rRNAs, tRNAs and ribosomal proteins for their own bacteria-like translation system.

5. Both contribute to energy conversion. The plastome encodes ATP synthase subunits (*atp* genes) and the mitochondrial genome encodes respiratory-chain and ATP synthase subunits.

6. Both are present in many copies per cell.

7. In land plants, both contain introns (including group II introns) and undergo RNA editing. This record flags editing for *ndhD*.

**Differences**

1. **Role:** the plastid is the site of photosynthesis and carries out carbon fixation and several biosynthetic pathways, while the mitochondrion carries out respiration.

2. **Size:** plastomes are usually about 120-170 kb (161,019 bp here). Plant mitochondrial genomes are usually much larger, from hundreds of kb to several Mb.

3. **Organization:** plastomes have a conserved quadripartite map (LSC-IR-SSC-IR). Plant mitochondrial genomes are multipartite, with a master circle and smaller subgenomic, linear and branched molecules produced by recombination.

4. **Gene content:** plastomes carry roughly 110-130 unique genes, including the photosynthesis genes. Plant mitochondrial genomes carry roughly 50-70 genes, mainly for respiration, ribosomal proteins and cytochrome c biogenesis.

5. **tRNA genes:** plastomes encode most or all of their tRNAs, whereas plant mitochondrial genomes lack some and import tRNAs from the cytosol.

6. **Structural stability:** plastome gene order is highly conserved, while plant mitochondrial genomes rearrange frequently because of recombination between repeats.

7. **Substitution rate:** in plants, point substitutions accumulate more slowly in mitochondrial DNA than in plastid DNA, but mitochondrial genomes change structurally much more.

8. **Foreign DNA:** plant mitochondrial genomes often contain sequences transferred from the plastid, nucleus or other species, while plastomes rarely do.

**Comparison table**

| Feature | Plastid genome | Mitochondrial genome |
|---|---|---|
| Cellular location | Inside plastids (chloroplasts in green tissue) | Inside mitochondria |
| Main biological functions | Photosynthesis, carbon fixation, and synthesis of fatty acids, amino acids and pigments; the genome encodes photosystem, cytochrome b6f, ATP synthase, Rubisco and RNA polymerase subunits | Respiration and ATP production; the genome encodes respiratory-chain and ATP synthase subunits |
| Typical genome organization | Circular-mapping, quadripartite (LSC-IR-SSC-IR); circular in this record | Multipartite in plants: a master circle plus subgenomic circles and linear or branched molecules |
| Relative genome size | Small and uniform, about 120-170 kb (161,019 bp here) | Larger and highly variable in plants, from hundreds of kb to several Mb; much smaller in animals |
| Gene content | About 110-130 unique genes; 99 in this record's table and 114 in the genome report | About 50-70 genes in plants, fewer in animals |
| Copy number | Many plastids per cell and many genome copies per plastid, so hundreds to thousands of copies per cell (varies with tissue) | Many mitochondria per cell with several copies each, usually fewer copies per cell than the plastome |
| Inheritance | Usually maternal in angiosperms, but paternal or biparental in some lineages; I did not find a *Hibiscus*-specific study | Usually maternal in plants, with exceptions |
| Recombination / structural change | Low; changes are mostly IR expansion or contraction and inversions (for example, *ycf1* is shifted at the IR/SSC border in some *Hibiscus* species) | Frequent recombination between repeats, producing rearrangements and multiple molecule forms |
| Mutation / substitution pattern | Low to moderate point-substitution rate; conserved gene order | Very low point-substitution rate in plants but rapid structural change; frequent RNA editing |
| Common research applications | Phylogenetics, DNA barcoding (*rbcL*, *matK*), phylogeography, cultivar identification, plastid genetic engineering | Cytoplasmic male sterility in crop breeding, mitochondrial phylogenetics, studies of gene transfer and genome rearrangement |

## Q10. Practical value and limitations of plastid genomes

**Advantages compared with the nuclear genome**

1. **Small and simple.** Plastomes are about 160 kb, so they are cheap to sequence and easy to assemble (mine came as one 161,019 bp record).

2. **High copy number.** Plastid DNA is abundant in total DNA, so it can be recovered from small samples, degraded tissue and herbarium specimens with shallow sequencing.

3. **Conserved structure and gene content.** Gene order and content are similar across plants, which makes alignment and comparison straightforward and supports universal barcode markers such as *rbcL* and *matK*.

4. **Effectively haploid.** There is no heterozygosity, allele phasing or paralog problem, unlike in nuclear genes.

5. **Uniparental inheritance and little recombination.** In most angiosperms the plastome is maternally inherited, so it records a single lineage. This is
useful for tracing maternal ancestry, seed dispersal and hybrid parentage.

6. **No sex-chromosome complications.** Nuclear sex chromosomes (X/Y or Z/W) in dioecious plants have suppressed recombination, repeat-rich regions, unequal gene content and different coverage in males and females, which makes them hard to assemble and interpret. The plastome is the same in both sexes and has none of these problems. *Hibiscus* flowers are generally bisexual, so this matters less for my species but is an advantage for dioecious plants.

7. **Moderate evolutionary rate.** The plastome is informative for relationships from family to species level, and noncoding regions add resolution among close relatives.

8. **Abundant reference data.** Many plastomes are in NCBI, so a new sequence can be compared with related species at low cost.

9. **Applications in biotechnology.** Plastid genetic engineering can give high transgene expression, and maternal inheritance limits transgene spread through pollen.

**Limitations**

1. **One inheritance unit.** The plastome behaves as a single non-recombining locus, so it shows one maternal history that can differ from the species tree. It misses hybridization and paternal gene flow and can be affected by chloroplast capture.

2. **Low variation among close relatives.** A study of 95 *H. syriacus* cultivar plastomes reported only 193 SNPs and 61 indels, so plastid variation within a species is limited, although it was still enough to design some accession-specific markers.

3. **Few traits are encoded.** Most traits, including flower colour, disease resistance and development, are controlled by nuclear genes.

4. **Technical pitfalls.** Nuclear copies of plastid DNA can contaminate data, the IR causes assembly and annotation errors (this record's missing IR and rRNA annotation is an example), and heteroplasmy can occur.

5. **Inheritance is not universal.** Paternal or biparental plastid inheritance occurs in some lineages, which can complicate lineage interpretation.

**Example research questions**

- **Plastid data are better suited to:** which *Hibiscus* species is the closest relative of *H. syriacus*, and which maternal lineage did a given cultivar or hybrid derive from?

- **Nuclear data are better suited to:** which genes control flower colour or petal number in *H. syriacus* cultivars, or how much gene flow occurs between species?

## References

1. NCBI RefSeq record NC_026909.1, *Hibiscus syriacus* chloroplast, complete genome. https://www.ncbi.nlm.nih.gov/nuccore/NC_026909.1

2. *The complete chloroplast genome sequence of Hibiscus syriacus.* Mitochondrial DNA Part A 27(5), 2016. doi:10.3109/19401736.2015.1079847

3. *The complete chloroplast genome sequence of Hibiscus syriacus L. 'Mamonde' (Malvaceae).* Mitochondrial DNA Part B, 2018. doi:10.1080/23802359.2018.1553526

4. *The complete chloroplast genome of Hibiscus taiwanensis (Malvaceae).* https://pmc.ncbi.nlm.nih.gov/articles/PMC7687590

5. *The complete chloroplast genome sequence of Hibiscus coccineus.* https://pmc.ncbi.nlm.nih.gov/articles/PMC8774145

6. *Pan-chloroplast genomes for accession-specific marker development in Hibiscus syriacus.* Scientific Data, 2024. https://www.nature.com/articles/s41597-024-03077-7

7. Galaxy platform, https://usegalaxy.org (Fasta Statistics tool).

8. General background for Q9 and Q10: course lecture notes and textbook, Cell and Molecular Biology.
