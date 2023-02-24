# Identifying gene pathways associated with glioblastoma recurrence using single-cell RNA sequencing 
Links to the notebooks can be found in the text files. The doublet removal file describes the process of removing doublets. The Quality Control file describes filtration and clustering. 
The data set comes from the following paper: 
Abdelfattah, N., Kumar, P., Wang, C., Leu, J. S., Flynn, W. F., Gao, R., Baskin, D. S., Pichumani, K., Ijare, O. B., Wood, S. L., Powell, S. Z., Haviland, D. L., Parker Kerrigan, B. C., Lang, F. F., Prabhu, S. S., Huntoon, K. M., Jiang, W., Kim, B. Y. S., George, J., & Yun, K. (2022). Single-cell analysis of human glioma and immune cells identifies S100A4 as an immunotherapy target. Nature communications, 13(1), 767. https://doi.org/10.1038/s41467-022-28372-y

The data originates from a paper by Abdelfattah et. al from the Houston Methodist Research Institute (Abdelfattah et. al). The paper itself focuses its analysis on the relationship between immune cells and gliomas, which is different from our focus on development of GBM. The tumor samples itself used for sequencing were obtained from patients at the at Houston Methodist Hospital, Houston, Texas and MD Anderson Cancer Center. The data then underwent single cell RNA sequencing using a 10X chromium controller and Cell Ranger software to process the data for raw use. 

The data itself consists of two layers. The first layer is a matrix where the rows are the ~200,000 cells and the columns are the ~20,000 genes. At each intersection between cell and gene is value that represents the gene expression level of the gene at that cell represented as numerical value. The second layer is a metadata layer, describing clinical attributes to each cell. This includes describing the weather the cell comes from a male or female, or a recurrent tumor or de novo tumor. Our metadata consists of four columns—diagnosis (recurrent or de novo), location of the tumor, the tumor grade, and sex of the patient—all of which are categorical values. The data itself is stored in a data structure called an AnnData object.   
