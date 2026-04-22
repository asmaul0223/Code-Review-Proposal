# Code Review

## Selected Manuscript

### Title:
-   Meta-Fish-Lib: A generalised, dynamic DNA reference library pipeline for metabarcoding of fishes

### Authors:
-   Collins et al. (2021)

### Publication:
-   Journal of Fish Biology

### Paper link (DOI):
-   https://doi.org/10.1111/jfb.14852

### Code Repository:
-   https://github.com/genner-lab/meta-fish-lib

## Why did I select this manuscript?

I chose this article because the concept is related to my current research (Fish DNA and species identification). Additionally, it contains a clear bioinformatics pipeline for building a fish DNA reference library.The manuscript uses publicly available data from NCBI and BOLD, making it relevant and reproducible.Furthermore, the authors provided an associated GitHub repository, which allows evaluation of the code structure, documentation, and usability.

## Summary

In this paper the authors Collins et al (2021) introduce Meta-Fish-Lib, which is a pipeline designed to generate curated DNA reference libraries for fish metabarcoding studies. This pipeline automatically gathers fish DNA data through the process of downloading, filtering, annotating, and quality-controlling sequence data from public repositories such as NCBI and BOLD. It also supports multiple genetic markers and provides tools for updating and versioning datasets.
They tested their tool on UK fish and added new DNA data to fill missing gaps. As a result, they improved how many species can be correctly identified, especially using a key DNA marker (12S). The pipeline integrates multiple bioinformatics tools and includes steps for phylogenetic quality control and reporting.
As requested by the editor, my review below focuses on the code associated with this manuscript.

## High-level suggestions

-   Meta-Fish-Lib helps build DNA reference libraries with a clear workflow, making research results more reproducible.
-   Using version control and DOIs makes it easy to track and cite results over time.
-   However, the overall usability of the pipeline is limited by a complex setup process that requires installation of multiple external tools (R, HMMER, MAFFT, RAxML).
-   The pipeline is not fully automatic. Users need to manually check phylogenetic trees and edit exclusion lists.
-   The workflow involves running multiple scripts in a specific order. There isn't a single command that runs everything, which could confuse beginners.
-   The documentation is detailed but may overwhelm beginners. Simpler instructions or tutorials would help
-   Some steps, like phylogenetic quality control, take a lot of time and computer power, which may be hard for some users.

## Lower-level suggestions (Specific):

-   The installation process requires multiple dependencies and environment setup steps, but a simplified installation guide or automated setup script would improve usability.
-   Setting up an NCBI API key is needed, but this step is not always clear and may be confusing for those new to the process.
-   The pipeline relies on executing multiple scripts manually, and clearer guidance on execution order would improve user experience.
-   Some scripts do not have many comments, which can make it harder for users to follow what certain parts of the code are for.
-   Error handling is limited, so if one API request does not work, the pipeline may stop, as mentioned in the README.md file.
-   It expects users to know Unix systems (mentioned in the README.md file) and does not offer help for Windows, which can make it less accessible.
-   Some steps, specially making phylogenetic trees, can take a long time, which may be difficult for users with fewer computing resources.
-   Although tutorials are available, having a small example or sample dataset could make it easier for users to try out and understand the pipeline.
-   Using both R and bash scripts makes the pipeline flexible, but it can be harder for users who are not familiar with both.

## Conclusion

The Meta-Fish-Lib pipeline is a well-designed tool for DNA metabarcoding. It utilizes version control, modular structure, and public databases, which are strong points. The setup is complex, and some steps are manually done. Easier instructions and more automation would make it more accessible to a broader range of users.  



 
