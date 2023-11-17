

An RNA-seq protocol


Experiment planning 


Preparation prior to starting your RNA-seq experiment is essential. Questions to answer before starting include:11
What method of RNA purification are you using?
What read depth will you need?
Which platform will you use? 
Is there a reference genome available and which will you use?
How are you assessing the quality of your RNA?
Do you need to enrich your target RNA?
Will you barcode your RNA?
Have I got enough biological and technical replicates?
Single-end or paired-end sequencing?
What read length will you use?
Do I want to retain strand-specific information?

cDNA library preparation 


After these points have been considered, you can start preparing your cDNA library. This will require fragmentation of the cDNA, addition of the platform-specific “adapter sequences” and amplification of the cDNA, but the exact procedure will be very specific to the platform used at this stage. For strand-specific protocols, the amplification of the cDNA involves a reverse transcriptase-mediated first strand synthesis followed by a DNA polymerase-mediated second strand synthesis.11,12 Barcodes may also be added that enable multiplexing, so numerous samples can be sequenced in a single run. It can be beneficial to quantify your library at the end of the library preparation stage to ensure the protocol has been successful and check the quality and concentration of your library to enable optimal sequencing performance.

cDNA sequencing


Once the library is prepared, you can use your chosen sequencing platform to sequence your cDNA library to your desired depth and requirements. Once your transcript data has been produced, you can map the data to your reference genome or assemble it de novo if no reference is available. The alignment process can be complicated by the presence of splice variants and modifications, and the choice of reference genome used will also vary how difficult this stage is. Software packages such as STAR are useful at this stage, as are quality control tools like Picard or Qualimap.13 De novo assembly will allow for the discovery of novel transcripts in addition to those already known.

RNA-seq data analysis


After the alignment stage, you can focus on analyzing your data. Tools like Sailfish, RSEM and BitSeq13 will help you quantify your transcription levels, whilst tools like MISO, which quantifies alternatively spliced genes, are available for more specialized analysis.14 There is a library of these tools out there, and reading reviews and roundups are your best way to find the right tool for your research.

To sum up, modern-day RNA-seq is well established as the superior option to microarrays and will likely remain the preferred option for the time being.  

Challenges of RNA-seq


Significant progress has been made in the field of RNA-seq over the last decade or so. The associated costs have reduced significantly while throughput has increased, sequence fidelity is far superior to earlier iterations of the NGS technologies and the availability of data analysis tools and pipelines has improved tremendously. However, there remain a number of challenges for scientists to bear in mind when considering RNA-seq experiments. These include:

Isolating sufficient, high-quality RNA – while the sample quantity requirements for RNA-seq analysis have reduced drastically, it is still important to ensure you are able to obtain sufficient RNA to fulfill all your analysis requirements, including repeats if necessary. It is also important to bear in mind that, while you may isolate total RNA, depending upon your experimental question, you are likely only to be sequencing a fraction of this (typically messenger RNA (mRNA)), further reducing your sample quantity. This must also be of high quality and purity as poor samples are likely to lead to poor results, or in some cases failure within the library preparation protocol. The quality and concentration of RNA can be determined using UV-visible spectroscopy. Unlike DNA, RNA degrades rapidly so it important to treat samples with care at all stages of isolation and purification. Degradation may not be uniform, hindering the comparison of transcription levels between genes. Low-level transcripts may be lost from the sequenced population altogether.

The impact of sample pooling – pooling samples prior to library preparation (without the use of barcoding) can reduce sequencing effort and costs or enable sequencing in cases where sample quantities are very limited. However, it is important to account for this during data analysis, with one such pool considered to be one biological replicate, not however many samples went in to making up the pool. Variations between the pooled samples can lead to misleading results and statistical issues so possible implications should be considered during the experimental design process.

Trading-off sequencing depth against sample number – It may seem appealing to get as many samples done in a single sequencing run as possible to reduce costs and machine time. However, this comes at a cost. The more samples are multiplexed, the fewer reads will be obtained for each of those samples. With reducing read depth comes mounting uncertainty as to the reliability of the sequences obtained. Sequencing technologies are still far from perfect, and mistakes are made in reads. It is therefore important to find the sweet spot between obtaining sufficient read depth to give confidence in the quality and fidelity of the sequencing data obtained and maximizing sequencing capacity to ensure sufficient biological replicates can be analyzed to give meaningful data.
