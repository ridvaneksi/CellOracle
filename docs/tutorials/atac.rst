.. _atac:

ATAC-seq data preprocessing
===========================

In this step, we process scATAC-seq data (or bulk ATAC-seq data) to get open accessible promoter/enhancer DNA sequence.
We can get active proximal promoter/enhancer genome sequence by picking up ATAC-seq peaks that exist around the transcription starting site (TSS).
Distal cis-regulatory elements can be picked up using  `Cicero <https://cole-trapnell-lab.github.io/cicero-release/docs/#installing-cicero>`_ .
Cicero analyzes scATAC-seq data to calculate a co-accessible score between peaks.
We can identify cis-regulatory elements using Cicero co-access score and TSS information.

If you have bulk ATAC-seq data instead of scATAC-data, we'll get only proximal promoter/enhancer genome sequence.



A. Extract TF binding information from scATAC-seq data
----------------------------------------------------
If you have a scATAC-seq data, you can get information of distal cis-regulatory elements.
This step uses Cicero and does not use celloracle. Please refer to `the documentation of Cicero <https://cole-trapnell-lab.github.io/cicero-release/>`_ for the detailed usage.

R notebook

.. toctree::

   ../notebooks/01_ATAC-seq_data_processing/option1_scATAC-seq_data_analysis_with_cicero/01_atacdata_to_cicero

Next, the results of Cicero analysis will be processed to make TSS annotations.

Python notebook

.. toctree::

   ../notebooks/01_ATAC-seq_data_processing/option1_scATAC-seq_data_analysis_with_cicero/02_preprocess_peak_data



B. Extract TF binding information from bulk ATAC-seq data or Chip-seq data
--------------------------------------------------------------------------
Bulk DNA-seq data can be used to get open accessible promoter/enhancer sequence.

Python notebook

.. toctree::

   ../notebooks/01_ATAC-seq_data_processing/option2_Bulk_ATAC-seq_data/01_preprocess_Bulk_ATAC_seq_peak_data