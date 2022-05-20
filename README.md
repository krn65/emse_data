# emse_data
NOTE: Due to GitHub size limitations, we are unable to upload the entirety of our data to GitHub. Please access the data described below via our Microsoft OneDrive link: https://mstate-my.sharepoint.com/:f:/g/personal/krn65_msstate_edu/ErpIY6uOnthBuEOmQYuXG6oBFvnjM7-ENk_qWn6x9ICDBg?e=PuNnjH

If this link becomes unavailable at any point, please contact and let us know so we can update.

We present the data used for experiments in the Empirical Software Engineering (EMSE) manuscript: "An Empirical Study of Text-based Machine Learning Models for Vulnerability Detection" by Napier et al.

The data includes `fixed` and `vulnerable` instances of source code extracted from various projects. In some cases, the data has been processed with one of three data processing methods we introduced in our study: 1) Full Context (FC) (raw data from extracted function, minus comments), 2) Condensed data from FC method that removes duplicate pieces of split functions based on whitespace, referred to as No Context (NC) in our manuscript. 3) Condensed data from FC method that removes duplicate pieces of split functions based on semicolons (lines of source code). Additionally, if available, add context of two (2) lines which occurred before and after a current line. We refer to this data processing method as Lines Context (LC).

The data is split into folders corresponding to the experiments performed in the study.

The `1-preliminary_experiment.zip` file contains two .TXT files and three folders. The two .TXT files contain all extracted fixed and vulnerable functions which we used as pairings. The data corresponds line for line between the two files. The three folders contain random samplings for each of the three data processing methods: Full Context (FC), No Context (NC), and Lines Context (LC).

The `2-projects_experiment_rq1.zip` file contains 343 folders with data related to the projects (available public GitHub repositories) that were used from the VCCFinder database dump [1] and a C/C++ Vulnerability Dataset [2].

The `3-cwe_experiment_rq2.zip` file contains 40 folders with data related to the mapped CWE IDs from the available CVE IDs within the datasets.

If you elect to use the data available in this folder, we ask that you provide a citation in your work for our work as well as all applicable related work as described and referenced in our study.

[1] Perl, Henning, Sergej Dechand, Matthew Smith, Daniel Arp, Fabian Yamaguchi, Konrad Rieck, Sascha Fahl, and Yasemin Acar. "Vccfinder: Finding potential vulnerabilities in open-source projects to assist code audits." In Proceedings of the 22nd ACM SIGSAC Conference on Computer and Communications Security, pp. 426-437. 2015.

https://github.com/announce/vcc-base

[2] Jiahao Fan, Yi Li, Shaohua Wang and Tien N. Nguyen. 2020. A C/C++ Code Vulnerability Dataset with Code Changes and CVE Summaries. In MSR ’20: The 17th International Conference on Mining Software Repositories,May 25–26, 2020, MSR, Seoul, South Korea. ACM, New York, NY, USA, 5 pages. https://doi.org/10.1145/3379597.3387501

https://github.com/ZeoVan/MSR_20_Code_vulnerability_CSV_Dataset
