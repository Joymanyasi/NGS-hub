# The Case of the Resilient Chicken

## An NGS Learning Journey Through the Kienyeji Story


**For:** Beginner students in bioinformatics and genomics

**Author:** Joy Manyasi Kabaka | ORCID: 0000-0002-2253-3970


**Based on:** Avian Organoid Transcriptomics Reanalysis — GSE283090

---

> *This is a true scientific story. The chickens are real. The data is real.
> The problem is urgent. And you ,the student  you are the scientist.*

---

**How this story flows:**

- Chapter 1 — We meet the biological problem: kienyeji are resilient but science cannot explain why
- Chapter 2 — We discover the tool: Next Generation Sequencing reads genetic instructions
- Chapter 3 — We find the tool problem: the White Leghorn reference genome hides kienyeji biology
- Chapter 4 — We examine existing data: broiler and layer cells already differ significantly
- Chapter 5 — We interrogate the key gene: ANP32A may explain kienyeji disease resistance
- Chapter 6 — We ask the harder question: who owns this knowledge and who benefits?

---

## Chapter 1 — The Biological Problem

Meet Mama Nereah.

She lives on a small farm in Malava, Kenya. Every morning she wakes up before sunrise to check on her chickens ,  of about 300 birds she has raised from chicks. These are not ordinary chickens. They are kienyeji  indigenous Kenyan chickens whose ancestors have roamed East African homesteads for centuries. They are her pride and source of livelihood.

Her neighbor James decided two moths ago to switch from kienyeji to commercial broiler chickens. The extension officer told him broilers grow faster, produce more meat, and would earn him more money at the market. James invested everything  his savings, a loan from the cooperative  on the new breed.

Then  there was an unfortunate event that occued,a mysterious disease that threatened the lives of the birds.

A respiratory illness swept through the region. James lost nearly his entire breed in three weeks. The commercial chickens, bred in controlled sanitized environments, had never encountered this pathogen before. They had no natural defenses against it.

Mama Nereah lost only  few birds, but most of her kienyeji survived.

This is not surprising to anyone who has farmed in East Africa. Kienyeji have lived alongside local pathogens for centuries. Generation after generation, the birds that survived disease passed their resistance on to their offspring. Over hundreds of years, their DNA accumulated changes small but powerful ,that gave them a natural edge against local diseases, heat stress, and harsh conditions that devastate commercial flocks.

Smallholder farmers across East Africa have known this for generations. Kienyeji are tougher. They survive on less food, tolerate heat, and resist local diseases that imported flocks cannot handle.

**But here is the problem: science has not caught up with what farmers already know.**

We do not know which specific genes make kienyeji resilient. We have no organoid models built from kienyeji cells. We have no breed-specific tools to study their immunity. And this is where the story gets complicated , because even when scientists try to study kienyeji using genomic tools, those tools were built for a completely different breed. A breed that has never scratched in East African soil.

That breed is called the White Leghorn.

And understanding why the White Leghorn is a problem is the first step toward building science that actually serves Mama Nereah.

---

### What You Will Learn in This Chapter

**What is a gene?**

Every living thing , is built from instructions. These instructions are written in a molecule called DNA. DNA is made of four chemical letters: A, T, G, and C. The order of these letters spells out instructions for building and running a living body.

A gene is one specific set of instructions. It might tell the body how to build a protein that fights a virus, how to regulate temperature, or how to absorb nutrients from food.

Mama Nereah's kienyeji chickens have genes that commercial chickens do not have  or have in different versions. Some of those genes are likely the difference between survival and death when a local pathogen arrives.

**What is a breed?**

Kienyeji chickens were shaped by their environment over hundreds of years  bred by survival, not by a laboratory. The birds that could handle heat, resist local diseases, and thrive on minimal food were the ones that reproduced. Their DNA accumulated changes that made them uniquely adapted to East African conditions.

Commercial breeds like the White Leghorn and broiler were bred for one thing — producing eggs or meat as fast as possible in controlled environments. They are genetically uniform. They are optimized for the factory farm, not the field.

**The core question this research asks:**

If kienyeji are so resilient, which genes are responsible? And why have our scientific tools  built around the White Leghorn  been unable to find the answer?

That is the mystery we are going to solve.

---

### Reflection Questions — Chapter 1

1. Can you think of other examples where a locally adapted variety of a plant, animal, or food crop performs better than an imported commercial variety in your region?

2. Why do you think scientists have studied commercial chickens more than indigenous chickens for so many decades?

3. If kienyeji resilience is already known to farmers, what would be the scientific value of identifying the specific genes responsible?

---

## Chapter 2 — The Tool: Next Generation Sequencing

Mama Nereah knows her kienyeji survive. Farmers know it. Extension officers know it. But knowing that something works and understanding the molecular mechanism behind it are two very different things.

If we identify the genes behind kienyeji resilience, we can:
- Breed even more resistant chickens deliberately
- Develop vaccines tailored to local African breeds
- Protect smallholder farmers from devastating outbreaks
- Build genomic tools that serve African farmers not just Western factory farms

To find those genes, we need to read the kienyeji instruction manual. The tool we use to read DNA is called Next Generation Sequencing , NGS.

---

### What is Sequencing?

For most of human history, we could not read DNA at all. The molecule was too small, too complex, too long. The entire chicken genome contains about 1 billion letters — A, T, G, C  and reading them one by one would take thousands of years by hand.

In the 1970s, scientists developed the first DNA sequencing methods. They were slow and expensive. Sequencing a single human genome cost about 3 billion dollars in the year 2000.

Then came Next Generation Sequencing , NGS. Suddenly, instead of reading one DNA fragment at a time, machines could read millions of fragments simultaneously. The cost dropped from billions to hundreds of dollars. The time dropped from years to days.

Today, NGS is the engine behind almost all modern genomics research.

---

### What Does NGS Actually Do?

Here is what happens when a scientist sequences a sample:

**Step 1 — Extract the DNA or RNA**
The scientist takes a tissue sample , in our story, cells from a chicken's intestine  and breaks open the cells to release the genetic material inside.

**Step 2 — Fragment the DNA**
The long strands of DNA are broken into millions of short pieces called reads. Each read is typically 50 to 300 letters long.

**Step 3 — Sequence the fragments**
The sequencing machine reads each fragment and records the letter sequence. This produces millions of short sequences.

**Step 4 — Store the data**
All these sequences are saved in a file format called FASTQ.

---

### What Does a FASTQ File Look Like?

Every read in a FASTQ file has exactly four lines:

Line 1 — the read name, like a barcode for each fragment
Line 2 — the DNA sequence itself, for example ATCGGTAGCTAGCTAGCTAGCTAGCTAGCTAG
Line 3 — a plus sign separator
Line 4 — quality scores showing how confident the machine is about each letter

A single experiment might produce a FASTQ file with 50 million of these four-line blocks. That is why we need computers to analyze them.

---

### RNA-seq — Reading What the Cell is Doing Right Now

To understand disease resistance, we do not just want to know which genes exist. We want to know which genes are switched ON when a pathogen arrives. For that, we sequence RNA not DNA.

Here is the difference:

DNA is the permanent instruction manual. Every cell in a chicken's body has the same DNA.

RNA is a temporary copy of one specific instruction, made when the cell needs to use it. When a cell is fighting a virus, it switches on specific genes and makes RNA from them.

By sequencing RNA , a technique called RNA-seq  scientists can see which genes are active in a specific cell at a specific moment.

In the dataset we are studying (GSE283090), scientists took intestinal cells from broiler and layer chicken embryos, grew them into tiny three-dimensional gut models called organoids, and sequenced the RNA from 43,587 individual cells.

Each cell told its own story. But none of them were kienyeji cells. Understanding why that matters is what Chapter 3 is about.

---

### Reflection Questions — Chapter 2

1. Why do you think scientists sequence RNA instead of DNA when they want to understand how a cell responds to disease?

2. If you had 43,587 cells and each produced a FASTQ file, what challenges would you face in analyzing all that data?

3. The dataset GSE283090 comes from broiler and layer chickens not kienyeji. Before reading Chapter 3, can you guess why that is a problem for understanding kienyeji resilience?

---

## Chapter 3 — The Tool Problem: The White Leghorn Reference

We have NGS data. But raw sequencing data — millions of short fragments  is meaningless on its own. To make sense of it, scientists need to map those fragments back to a reference genome.

And this is where the first major problem enters our story.

---

### What is a Reference Genome?

When you sequence a sample, you get millions of short fragments but you do not know where in the genome each fragment came from. It is like shredding a book into confetti and then trying to reassemble it. You need the original book as a guide.

To reassemble the reads, scientists align them to a reference genome — a complete pre-assembled version of the genome of that species used as a map.

For chickens, the standard reference genome is called GRCg6a. It was built from a single individual , one White Leghorn chicken.

---

### Why the White Leghorn is a Problem

The White Leghorn is a highly inbred commercial breed developed in Europe and North America for industrial egg production. It has been selectively bred for generations to be genetically uniform. It has never lived in East Africa. It has never been exposed to endemic East African pathogens. It has never had to survive heat stress or Newcastle Disease Virus without veterinary intervention.

Yet every piece of chicken genomic data analyzed anywhere in the world  including any future kienyeji data  gets mapped against this single White Leghorn individual's genome.

Here is what that means in practice:

Kienyeji chickens carry genetic variants , small differences in their DNA letter sequence that evolved over centuries of East African survival. When scientists align kienyeji RNA reads to the White Leghorn reference, reads that contain kienyeji-specific variants do not align well. The software either discards them or misplaces them.

The result: the most important kienyeji biology becomes invisible.

The very genes that explain kienyeji resilience  the ones that evolved to survive local pathogens and heat  are missed entirely because the White Leghorn reference genome has no place for them.

This means that every genomic study of kienyeji conducted so far has been working with an incomplete and systematically biased picture.

---

### So What Do We Do?

We cannot immediately build a kienyeji-specific reference genome  that requires significant resources and time.

But we can do something valuable right now, take the best publicly available avian organoid dataset , GSE283090  and reanalyze it using a variant-aware pipeline that accounts for breed-specific genetic differences instead of forcing everything through the White Leghorn lens.

This reanalysis does two things:

First — it demonstrates that even commercial breeds differ significantly at immune and stress response genes when analyzed carefully. If broiler and layer already differ this much, kienyeji would differ even more.

Second — it builds and documents the pipeline that will be used when kienyeji data becomes available, ensuring that future analysis captures what standard tools miss.

This is the scientific contribution of our GitHub repository. Not kienyeji data yet  but the proof of concept and the tools that make kienyeji genomics possible.

---

### A Concrete Example — The ANP32A Gene

One gene central to our analysis is ANP32A.

ANP32A produces a protein that interacts with the avian influenza virus inside the cell. Whether a chicken is susceptible or resistant to avian influenza depends partly on which version of ANP32A it carries.

A single letter change at position 129 , the N129D variant  makes ANP32A much less useful to the virus. Chickens carrying this variant are more resistant.

The White Leghorn reference genome carries one version of ANP32A. Kienyeji chickens — shaped by centuries of pathogen exposure  may carry a more protective version.

But if we align kienyeji data to the White Leghorn reference, we may miss that variant entirely. The White Leghorn dictionary does not contain that word.

Our reanalysis begins to expose this gap using existing data.

---

### Reflection Questions — Chapter 3

1. In your own words, explain why the White Leghorn reference genome is a problem for studying kienyeji chickens.

2. Can you think of another situation in medicine where using the wrong reference population led to wrong conclusions? Hint: think about clinical drug trials and African patients.

3. Our solution is to reanalyze existing commercial breed data as a first step. Why is this a valid scientific approach even before kienyeji data is available?

---

## Chapter 4 — The Existing Evidence: GSE283090

We cannot yet analyze kienyeji cells directly. But we can analyze the best available public dataset — GSE283090 — and ask: do different chicken breeds already show significant differences at the cellular level?

If the answer is yes, the case for kienyeji-specific models becomes scientifically undeniable.

---

### What is GSE283090?

GSE283090 is a dataset published in April 2025 by scientists at the Roslin Institute, University of Edinburgh. They took intestinal cells from broiler and layer chicken embryos, grew them into three-dimensional gut models called organoids, and sequenced the RNA from 43,587 individual cells using single-cell RNA sequencing.

This is currently the most comprehensive public avian intestinal organoid dataset in the world.

It does not contain kienyeji cells. But it contains something very useful , a comparison between two commercial breeds that already have different genetic backgrounds.

---

### What is Single-Cell RNA Sequencing?

Traditional RNA sequencing takes RNA from thousands of cells mixed together and measures average gene expression. It hides differences between individual cells.

Single-cell RNA sequencing , scRNA-seq  sequences the RNA from each individual cell separately, giving each cell its own barcode so you can track it through the analysis.

The result is a data matrix with rows representing individual cells, columns representing individual genes, and values showing how much RNA of each gene was found in each cell.

---

### What is Clustering and What is a UMAP?

With 43,587 cells and 16,000 genes, you cannot look at each cell individually. Instead, you use a mathematical technique called clustering to group cells that look similar together.

The result is visualized using a UMAP plot where each dot is one cell, dots close together express similar genes, and different clusters represent different cell types.

This is what Script 02 in our pipeline produces.

---

### What Cell Types Were Found in GSE283090?

When the Roslin scientists clustered the 43,587 cells, they found:

Epithelial cells lining the intestine including enterocytes that absorb nutrients, goblet cells that produce protective mucus, Paneth cells that release antimicrobial molecules, tuft cells that sense parasites, and enteroendocrine cells that release hormones.

Mesenchymal structural support cells including fibroblasts, smooth muscle cells, telocytes, and pericytes.

Immune cells including macrophages, monocytes, T cells, and NK cells.

---

### The Critical Finding

Broiler and layer cells clustered differently.

Even though both are commercial chickens with a shared industrial history, their intestinal cells showed significant differences in gene expression  especially in epithelial cells.

This is the evidence we need. If two commercial breeds that are relatively similar already differ significantly at the cellular level, then kienyeji  with centuries of divergent evolution in East Africa — would differ far more dramatically.

The commercial breed data we have is not a proxy for kienyeji. It is a map of entirely different biological territory. And that is exactly the argument our reanalysis makes.

---

### Reflection Questions — Chapter 4

1. Why is it important to look at individual cell types rather than mixing all cells together before comparing breeds?

2. The broiler and layer breeds already differ in intestinal gene expression. What does this mean for the assumption that one reference genome fits all chicken breeds?

3. Which cell types do you think would be most important for understanding kienyeji disease resistance and why?

---

## Chapter 5 — The Key Gene: ANP32A and the Immune Panel

We have established that different chicken breeds differ at the cellular and molecular level. Now we zoom in on the specific genes that matter most for kienyeji resilience.

---

### Meet ANP32A

ANP32A stands for Acidic Nuclear Phosphoprotein 32 Family Member A. It is a protein found in the nucleus of cells — the control center where DNA is stored.

In normal circumstances, ANP32A helps regulate how DNA is read. But when an avian influenza virus enters a cell, ANP32A becomes a critical battleground.

The influenza virus hijacks ANP32A and uses it as a tool to copy its own genetic material inside the host cell. The more efficiently the virus can use ANP32A, the faster it replicates and the sicker the bird becomes.

A single letter change at position 129 of the ANP32A protein  from N to D, known as the N129D variant  makes the protein much less useful to the virus. Chickens carrying this N129D variant are more resistant to avian influenza because the virus cannot replicate as efficiently.

The White Leghorn reference genome carries one version of ANP32A. Kienyeji chickens, shaped by centuries of exposure to endemic avian pathogens, may carry the more protective N129D variant  or other protective variants that commercial breeds do not have.

We do not know yet. Standard tools aligned to the White Leghorn reference may be hiding the answer. Our reanalysis begins to expose that gap.

---

### What is Differential Expression?

To find out whether ANP32A and other immune genes behave differently between breeds, we use differential expression analysis.

The question is simple: is this gene expressed more in group A than in group B?

In our analysis using GSE283090, we ask: do immune response genes, viral restriction genes, and thermal stress genes behave differently between broiler and layer intestinal cells?

If yes  even between two commercial breeds then, the gap between commercial breeds and kienyeji is even larger. And breed-specific models are not just useful. They are essential.

This is what Scripts 03 and 04 in our pipeline investigate.

---

### How to Read a Volcano Plot

Script 04 produces a volcano plot , the standard way to visualize differential expression results.

The X axis shows Log2 Fold Change  how much more or less a gene is expressed in one group compared to the other. Points to the right are higher in broiler. Points to the left are higher in layer.

The Y axis shows statistical significance  how confident we are that the difference is real. Points higher up are more statistically significant.

Red points are genes that are both strongly changed AND statistically significant  these are the key findings. Grey points changed but not significantly  less important.

---

### The Kienyeji Gene Panel

In Script 04 we specifically interrogate genes relevant to what makes kienyeji special:

| Gene | Why It Matters for Kienyeji |
|------|----------------------------|
| ANP32A | Influenza host restriction — protective variant may exist in kienyeji |
| MX1 | Antiviral interferon response |
| HSP90AA1 | Heat shock — thermal adaptation to East African climate |
| HSPA8 | Heat shock protein — cellular stress response |
| TLR4 | Pathogen recognition receptor |
| TLR7 | RNA virus sensing |
| IL6 | Inflammatory response regulation |
| IFNG | Interferon gamma — antiviral defense |
| IRF7 | Interferon regulatory factor |

---

### Putting It All Together

Here is the complete logic chain of our research:

White Leghorn reference genome biases all chicken genomic analysis.

GSE283090 broiler and layer data was also analyzed using this biased reference.

Our reanalysis uses a variant-aware pipeline to expose what standard tools miss.

Finding broiler and layer already differ significantly at immune genes.

Implication: kienyeji would differ even more.

Proposal: a kienyeji-specific organoid model is urgently needed.

Goal: build tools that reveal kienyeji resilience genes.

Benefit: vaccines and breeding programs that serve East African smallholders.

This is your research story. This is what is on GitHub. This is what is being presented at the HEARTS4C-2 conference.

---

### Reflection Questions — Chapter 5

1. Why might kienyeji chickens carry a more protective version of ANP32A than White Leghorn chickens?

2. If you were designing a vaccine specifically for kienyeji chickens, why would it matter whether their ANP32A is different from the commercial breed version?

3. Look at the complete logic chain above. Where do you think the biggest scientific gap currently is? What would you prioritize filling first?

---

## Chapter 6 — Justice for Kienyeji: Data Sovereignty

We have followed the science. We have found the tool problem. We have demonstrated the gap. We have built the pipeline.

But there is one more dimension to this story that most bioinformatics courses never teach and it may be the most important chapter of all.

---

### Who Owns the Data?

When a scientist sequences a kienyeji chicken from Mama Nereah's farm, something extraordinary happens. The genetic information from that bird ,information that represents centuries of adaptation, shaped by the land, the climate, and the stewardship of Kenyan smallholder farmers  is converted into digital data.

That data can be uploaded to a server anywhere in the world. It can be downloaded by researchers in Europe or North America. It can be used to develop vaccines, diagnostic tools, or commercial products — without Mama Nereah ever knowing, without her community ever benefiting, and without Kenya ever seeing a shilling.

This is not hypothetical. It has happened before  with plant genetic resources, with medicinal plant knowledge, with human genetic samples from African populations.

The resilience genes that make kienyeji valuable  evolved over centuries and stewarded by generations of East African farmers  could become the foundation of a commercial product that Mama Nereah can never afford to buy.

That is not science serving society. That is extraction.

---

### What is DSI?

Digital Sequence Information , DSI  refers to digital genetic data derived from biological samples including DNA sequences, RNA sequences, protein sequences, and any other digitized biological information.

DSI is at the center of a global debate about who owns genetic resources and who benefits from their use.

---

### The Nagoya Protocol

In 2010, the international community adopted the Nagoya Protocol under the Convention on Biological Diversity. It was designed to ensure that benefits arising from the use of genetic resources are shared fairly with the countries and communities from which those resources come.

The protocol requires prior informed consent from the community before collecting samples, mutually agreed terms for how the data will be used, and benefit sharing — returning value to the source community.

In practice, compliance is uneven. Many researchers collect samples, sequence them, upload the data, and move on without establishing benefit-sharing agreements.

---

### How Our Framework Does It Differently

Our kienyeji research is designed with governance from the start. Every design decision asks: who benefits?

Sequences generated from kienyeji birds will be deposited under Kenyan institutional custodianship — not overseas servers.

Communities that provide birds will be involved in formal consent processes before any sampling begins.

Any tools developed from this data , vaccines, diagnostics, improved breeds  will be designed to be accessible to the smallholder farmers whose birds made the science possible.

The GitHub repository is public so the methods remain open and cannot be locked behind commercial patents.

This is what African data sovereignty looks like in practice. It is the difference between research that extracts from Africa and research that builds Africa.

---

### Algorithmic Justice

The algorithms we use in bioinformatics,— the reference genomes, the clustering methods, the variant databases  were built on data from commercial Western breeds in Western institutions.

When we run African samples through these algorithms, we run them through tools that were not designed for them. The results are biased. The conclusions may be wrong. And when those biased conclusions inform vaccine development, livestock policy, or breeding programs in Africa, the cost is paid by farmers like Mama Nereah and neighbors like James.

Algorithmic justice means building tools that work fairly for all populations  not just the ones that were convenient to study first.

Our variant-aware pipeline is a deliberate step in that direction.

---

### What Can You Do?

1. Learn the tools — R, Python, Seurat, GATK
2. Use African datasets — seek out publicly available African genomic data and analyze it
3. Ask governance questions — when you read a paper, ask where did the samples come from, who consented, and who benefits from the findings
4. Build local capacity — share what you learn with your community, your students, your colleagues
5. Cite African researchers — amplify African science

---

### Final Reflection — Chapter 6

1. Have you ever heard of a case where knowledge or resources from your community were used by outsiders without benefit sharing? How did it make you feel?

2. If you were advising the Kenyan government on a DSI policy for livestock genomic resources, what three rules would you put in place?

3. Now that you have followed this entire story  from Mama Nereah's farm , what is the one thing you will remember most?

---

## Epilogue — Back to Mama Nereah

The science is not finished.

The kienyeji organoid has not been built yet. The ANP32A variants have not been fully characterized. The breed-specific vaccine has not been made. The reference genome bias has not been fully corrected.

But the framework exists. The pipeline is on GitHub. The argument has been made  scientifically and ethically.

And somewhere in Malava, Mama Nereah's chickens are scratching in the red soil, carrying in their cells a genetic story that has never been fully told.

A story of resilience. Of adaptation. Of centuries of survival in conditions that would devastate any commercial flock.

That story deserves to be told properly  with the right tools, the right reference genome, and the right people asking the questions.

The scientists who do this work  the ones who understand the biology, master the tools, ask who benefits, and insist on justice for the communities whose stewardship made the genetic diversity possible  will change what it means to do genomics in Africa.

You could be one of them.

---

## Quick Reference — Key Terms

| Term | Simple Definition |
|------|------------------|
| DNA | The instruction manual for all living things |
| Gene | One specific instruction in the manual |
| RNA | A temporary copy of one instruction, made when the cell needs it |
| NGS | A technology that reads millions of DNA/RNA fragments at once |
| FASTQ | The file format that stores raw sequencing reads |
| Reference genome | A complete genome used as a map for aligning reads |
| White Leghorn | A commercial inbred breed whose genome is the standard chicken reference |
| Alignment | Matching short reads back to their position in the reference |
| Variant-aware pipeline | An alignment method that accounts for breed-specific genetic differences |
| scRNA-seq | Sequencing RNA from individual cells separately |
| Organoid | A tiny 3D organ model grown from real cells in a lab |
| UMAP | A plot that shows how cells group by gene expression |
| Clustering | Grouping similar cells together mathematically |
| Differential expression | Comparing which genes are more or less active between groups |
| Volcano plot | A graph showing differential expression results |
| ANP32A | A gene involved in influenza susceptibility and resistance |
| N129D variant | A protective change in ANP32A that reduces viral replication |
| DSI | Digital Sequence Information — digitized genetic data |
| Nagoya Protocol | International law for fair sharing of genetic resource benefits |
| Kienyeji | Indigenous East African chicken breeds |
| Algorithmic justice | Ensuring bioinformatics tools work fairly for all populations |

---

*This narrative was developed as part of the kienyeji avian organoid transcriptomics reanalysis project. GitHub: https://github.com/Joymanyasi/avian-organoid-transcriptomics-reanalysis*
