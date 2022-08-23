# emse_data
NOTE: Due to GitHub size limitations, we are unable to upload the entirety of our data to GitHub. Please access the data described below via our Microsoft OneDrive link: https://mstate-my.sharepoint.com/:f:/g/personal/krn65_msstate_edu/ErpIY6uOnthBuEOmQYuXG6oBFvnjM7-ENk_qWn6x9ICDBg?e=PuNnjH

If this link becomes unavailable at any point, please contact and let us know so we can update.

We present data used for experiments in the Empirical Software Engineering (EMSE) journal manuscript: "An Empirical Study of Text-based Machine Learning Models for Vulnerability Detection" by Kollin Napier, Dr. Tanmay Bhowmik, and Dr. Shaowei Wang (Napier et al.).

The data includes `fixed` and `vulnerable` instances of functions extracted and paired from source code of various projects. In some cases, the data has been processed with one of three data processing methods we introduced in our study: 1) Full Context (FC) (raw data from extracted function, minus comments), 2) Condensed data from FC method that removes duplicate pieces of split functions based on whitespace, referred to as No Context (NC) in our manuscript. 3) Condensed data from FC method that removes duplicate pieces of split functions based on semicolons (lines of source code). Additionally, if available, add context of two (2) lines which occurred before and after a current line. We refer to this data processing method as Lines Context (LC).

The data is split into folders corresponding to the experiments performed in the study.

The `1-preliminary_experiment.zip` file contains two (2) .TXT (text) files and four (4) folders (directories). The two .TXT files contain all extracted fixed and vulnerable functions which we used as pairings. The pairings are defined line for line between the two files. For example, line 1 in `fixed-full_context.txt` is the counterpart of line 1 in `vulnerable-full_context.txt`. Three (3) folders (directories) contain random samplings for each of the three (3) data processing methods: Full Context (`FC`), No Context (`NC`), and Lines Context (`LC`). The random samplings are split into increments of 500, 1000, 2500, 5000, 10,000 and 20,000. Each increment was generated five (5) separate times to create five iterations of randomly sampled data. We utilized this approach to help generate an average prediction score towards our evaluation of average precision scores from our supervised machine learning models. Additionally, when training and testing models, we initially employed a training, testing, splitting strategy for the `FC` data. However, to provide a better "real world" approach when using our condensed function data, we elected to train on `NC` or `LC` and test on `FC`. The final folder (directory) named `random_data` contains the data we randomly selected for our training and testing during this process. Please refer to our manuscript for further clarification.

The `2-projects_experiment_rq1.zip` file contains folders (directories) with data related to the projects (available public GitHub repositories) that were used from the VCCFinder database dump [1] and a C/C++ Vulnerability Dataset ("Big-Vul") [2]. The folders contain four (4) .TXT (text) files representing the overall `fixed` and `vulnerable` functions extracted and paired from the applicable source code mapped to vulnerabilities as well as the condensed `NC` versions.

The `3-cwe_experiment_rq2.zip` file contains folders (directories) with data related to the mapped Common Weakness Enumeration (CWE) identifiers (IDs) from the available Common Vulnerabilities and Exposures (CVE) IDs within the datasets. Each folder contains at least one (1) .TXT (text) file with mapped CVE IDs to the overall CWE (as defined by the folder name). Folders with more data contain more files. For example, CWE 119 has five (5) files corresponding to the overall `fixed` and `vulnerable` functions as well as the `NC` versions and the CVE IDs which were mapped. Whereas CWE 1187 only has a single .TXT (text) file with mapped CVE IDs. Therefore, there was not any applicable data in this case.

If you elect to use the data available in this folder, we ask that you provide a citation in your work for our work as well as all applicable related work as described and referenced in our study.

[1] Perl, Henning, Sergej Dechand, Matthew Smith, Daniel Arp, Fabian Yamaguchi, Konrad Rieck, Sascha Fahl, and Yasemin Acar. "Vccfinder: Finding potential vulnerabilities in open-source projects to assist code audits." In Proceedings of the 22nd ACM SIGSAC Conference on Computer and Communications Security, pp. 426-437. 2015.

https://github.com/announce/vcc-base

[2] Jiahao Fan, Yi Li, Shaohua Wang and Tien N. Nguyen. 2020. A C/C++ Code Vulnerability Dataset with Code Changes and CVE Summaries. In MSR ’20: The 17th International Conference on Mining Software Repositories,May 25–26, 2020, MSR, Seoul, South Korea. ACM, New York, NY, USA, 5 pages. https://doi.org/10.1145/3379597.3387501

https://github.com/ZeoVan/MSR_20_Code_vulnerability_CSV_Dataset
