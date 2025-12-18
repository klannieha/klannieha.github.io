## Evaluation and Optimization of DIA-MS for Prostate Cancer Urine Proteomics Analysis

Biofluids such as urine contain molecules in circulation and from nearby organs that can be indicative of disease states. However, comprehensive profiling of the proteomes in urine has been challening due to high dynamic range and variability between samples. Data-independent acquisition mass spectrometry (DIA-MS) has been popularized over recent decades as a high throughput and sensitive bottom-up proteomics workflow with improved data completeness compared to conventional MS methods. Hence, characteirizing the proteome of patient-derived urines with DIA-MS is an emerging area of interest for biomarker discovery. Thus far, there is limited consensus on DIA-MS acquisition and analysis approaches. In this project, I benchmarked several published DIA-MS acquisition schemes, as well as various computational analysis workflows using a clinically heterogeneous cohort from patients with localized prostate cancer, to identify an optimal DIA-MS workflow for large-scale urine proteomics analyses.


### 1. Optimize DIA-MS acquisition scheme for improved throughput

To evaluate various published DIA-MS methods, I evaluated metrics such as the peptide and protein detection rates, coefficient of variations, using pooled patient urine samples.

<picture>
  <img alt="Schematic of method optimization" src="images/thesis_chapter1_methodOpt_schematic.png">
</picture>

In total, I tested 25 methods (each in triplicates) across various liquid chromatography run time to identify a method that can be comparable to conventional DDA-MS with higher throughput. We identified a 45-minute method that is double the throughput without loss in peptide detection.

<picture>
  <img alt="Results of various DIA methods tested compared against DDA" src="images/thesis_chapter1_methodOpt_summary.png">
</picture>


### 2. Benchmark various computational strategies for the most comprehensive results

Currently, there is no consensus of a database searching approach in DIA-MS. In the context of urine proteomics, I compared search results from various library generation approaches against a library-free algorithm and a publicly available library.

<picture>
  <img alt="Schematic of library generation" src="images/thesis_chapter1_library_schematic.png">
</picture>


Across all the database searching approahces, the method using sample-specific library (uEPS) generated from individual DDA runs of each sample resulted in the most consistently detected peptides. The search times for this method is also less than 1 min per sample, enabling swift and efficient large-scale cohort analyses.

<picture>
  <img alt="Search results across tested methods" src="images/thesis_chapter1_library_results.png" >
</picture>

Therefore, altogether, the 45-minute DIA-MS method coupled with the sample-specific library search is chosen as the optimal method.

### 3. Comparison between 45-min DIA against conventional 2-hr DDA method

Having a 45-minute DIA method optimized for urine proteomics analysis, I sought to compare the resulting data matrix against our conventional 2-hr DDA method using the same samples. The results showed that our optimized DIA method was able to identify more peptides and proteins per sample, generate more complete (less missing values) dataset, as well as produce quantitatively comparable intensity compared to DDA.

<picture>
  <img alt="Comparisons of matched samples between DIA and DDA" src="images/thesis_chapter1_dda_dia_results.pdf">>
</picture>

Not only that DIA showed advantageous results in peptide and protein detection rates, it was able to detect more peptides and proteins that are of lower abundance, despite shorter gradient separation.

<picture>
  <img alt="Detection rates of proteins across abundance quartile (1 is lowest abundance, 4 is highest)" src="images/thesis_chapter1_dda_dia_quantile.png">
</picture>

Not only that DIA showed advantageous results in peptide and protein detection rates, it was able to detect more peptides and proteins that are of lower abundance, despite shorter gradient separation.

<picture>
  <img alt="Detection rates of proteins across abundance quartile (1 is lowest abundance, 4 is highest)" src="images/thesis_chapter1_dda_dia_quantile.png">
</picture>

### 4. Expanding proteome depth using sample-relevant spectral libraries

While I have shown that DIA-MS can improve protein detection and sample throughput, lower abundance and less frequently detected prostate-derived proteins may be missed in spectral libraries derived from unfractionated urine due to the high dynamic range of the sample type. Leveraging previously published urine-derived extracellular vesicles dataset, we generated and compared results of DIA data searched against various libraries from various urine fractions.



For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
