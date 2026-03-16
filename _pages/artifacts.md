---
layout: page
title: Artifacts
permalink: /artifacts/
order: 6
published: false
---
<!--# Call for Artifacts-->
Claims and (experimental) results described in a paper often originate from artifacts not present in the paper. Reproducibility of (experimental) results is crucial to foster an atmosphere of open, reusable, and trustworthy research. Furthermore, good artifacts enable future researchers to effectively build on and compare with previous work.

Similar to last year, SEFM includes artifact evaluation, which is performed by a separate artifact evaluation committee (AEC). Artifact evaluation is **mandatory for tool papers** and **optional for regular papers**. The goals of artifact evaluation are to encourage authors to provide artifacts for reproduction and future use as well as to reward authors who create good artifacts. 

Artifacts of interest include (but are not limited to):
-	Software, Tools, or Frameworks
-	Data sets
-	Test suites
-	Machine-checkable proofs
-	Any combination of them
-	Any other artifact described in the paper

We aim to assess the artifacts themselves and not the quality of the research linked to the artifact, which is assessed by the SEFM 2024 program committee. However, **artifacts for tool papers** should at least meet the requirements for the **functional badge** for the paper to be eligible for acceptance.

## Important Dates
-	Artifact submission deadline: TO BE ANNOUNCED
-	Test phase notification: TO BE ANNOUNCED
-	Author respond period: TO BE ANNOUNCED
-	Artifact notification: TO BE ANNOUNCED

## Awarded Badges
SEFM awards the [Artifacts Available and Artifacts Evaluated badges of EAPLS](https://eapls.org/pages/artifact_badges/).
1.	The Artifacts Evaluated badge has two levels, functional and reusable. We will award at most one of the two levels.
    1.	For the artifacts **functional** badge, the artifact must be documented, consistent, complete, and exercisable.
    2.	For the artifacts **reusable** badge, the artifact must meet the requirements of the artifacts functional badge and in addition must be of very high quality, i.e., it is also carefully documented and well-structured for reuse and repurposing.
2.	The artifacts **available** badge will be awarded if the artifact is **publicly and permanently available** via a Digital Object Identifier (**DOI**) that is referenced in the respective paper and the artifact is **relevant** for the paper and adds **value** beyond the paper.

The Artifacts Available badge and Artifacts Evaluated badge are awarded independently of each other. Artifacts that are not exercisable, as, for example, protocols used for empirical studies, will be evaluated only according to the Available badge, as the Evaluated badges are not applicable to them. All awarded badges will be shown on the first page of the paper.

## Artifact Submission
An artifact submission should consist of
-	an **abstract** that
    *	summarizes the artifact and explains its relation to the paper,
    *	mentions where in the artifact it is documented how to perform the test phase and how to reproduce the results of the paper, 
    * if applicable, provides a description of any **additional special requirements** beyond a VM or Docker image needed to properly run the artifact, e.g. cloud-computing resources, certain hardware, proprietary software or data,
    * includes an **URL** - we encourage you to provide a DOI - to a **.zip** file of your artifact containing 
        +	a **license** file that allows the artifact evaluation committee to evaluate the artifact,
        + a clear **documentation** how to perform the **test phase**, and
        + a **documentation how to reproduce the results** of the paper,
    * the **SHA256 checksum** of the .zip file, and
    *	the **paper submission ID** of your submitted paper.
-	a **.pdf** file of the submitted paper. For the availability badge, the paper must reference the DOI of your artifact. Note that you do not need to provide the .pdf file with your artifact submission, but we will get the .pdf file from your paper submission.

Please consider the [Artifact Packaging Guidelines](#artifact-packaging-guidelines) for detailed information about the contents of the artifact.

The abstract ~~and the .pdf file of your paper~~ must be submitted via [EasyChair](https://easychair.org/my/conference?conf=sefm25) to the **SEFM'25 Artifact Evaluation** track. The .pdf file of your submitted paper will be taken from your EasyChair submission in paper track.

If you cannot submit the artifact as requested or encounter any other difficulties in the submission process, please contact the artifact evaluation chair prior to submission. 

## Artifact Packaging Guidelines 
We recommend to prepare your artifact in such a way that any computer science expert without dedicated expertise in your field can use your artifact, especially reproduce your results. For example, keep the evaluation process simple, provide easy-to-use scripts and a detailed README document. Furthermore, the artifact and its documentation should be self-contained. In particular, the artifact should contain all the required files to reproduce your results.

The **.zip** file containing your artifact must consist of the following elements:
* The **artifact**, i.e., data, software, libraries, scripts, etc. required to reproduce the results of your paper. Please prepare a **Docker image** or a **Virtual Machine**. We recommend to use VirtualBox to save a VM image as an OVA file.
* A **LICENSE** file that describes the license for your artifact. Your license must allow the artifact evaluation committee members to download and evaluate the artifact, e.g., download, use, execute, and modify the artifact for the purpose of artifact evaluation. Please refer to typical open-source licenses. Artifacts without an open-source license are also accepted, but a license type needs to be specified, allowing the committee to assess the artifact. For quick help about possible licenses, visit [https://choosealicense.com/](https://choosealicense.com/).
* A **README** file that introduces the artifact to the user and guides the user through the reproduction of your results. Consider the section for [README recommendations](#readme-recommendations) for more details.
If you cannot submit the artifact as requested or encounter any other difficulties in the submission process, please contact the artifact evaluation chair prior to submission. 

### Checksum instructions
We need the checksum to ensure the integrity of your artifact. You can generate the checksum using the following command-line tools. 

- Linux: `sha256sum <file>`
- Windows: `CertUtil -hashfile <file> SHA256`
- MacOS: `shasum -a 256 <file>`

### README Recommendations
The README file should introduce the artifact to the user, i.e., describe what the artifact does, and guide the user through the reproduction of your results. In addition, it should guide the user through the test phase evaluation and if needed any required installation or setup processes. Ideally, it should consist of the following sections.
* **Summary**: brief description of the artifact goal, authors, reference to the paper, and indication on how to cite the artifact. We recommend to also describe the structure and content of your artifact.
* **Hardware Requirements**: hardware requirements (RAM, number of cores, CPU frequency), which you considered to test your artifact. Your resource requirements should be modest and allow reproduction of results even on laptops.
* **Proprietary Software or Data Requirements**: additional proprietary software or data that is not provided in the artifact but required to reproduce your results
* **Setup** describes the steps to set up your artifact for use. To simplify the reviewing process, we recommend to provide an installation script (if necessary).
* **Test Instructions** document how to perform the test phase evaluation, e.g., provide instructions that allow rudimentary testing (i.e., in such a way that technical difficulties would pop up) in as little time as possible.
* **Reproduction time** estimates the expected total runtime to reproduce the results, e.g., to run the experiments.
    * Please provide for each task/step of the reproduction (an estimate) how long it will take to perform it or how long it took for you and what exact machine(s) you used.
* **Reproduction Instructions**: clear description how to repeat/reproduce/replicate the results presented in the paper. 
    * Please document which claims or results of the paper can be reproduced with the artifact and how (e.g., which experiment must be performed). Please also explain which claims and results cannot be reproduced and why.
    * Describe in detail how to reproduce the results in the paper, especially describe the steps that need to be performed to reproduce the results in the paper. To simplify the reviewing process, we recommend providing evaluation scripts (where applicable).
* **Reproduction with Limited Resources**: For tasks or experiments that require a large amount of resources (i.e. more than 2 hours or 4 GB), the artifact should offer a possibility to reproduce a subset of the results of the paper that can be reproduced in a reasonable amount of time e.g., within 2 hours and 4 GB on various hardware platforms including laptops and reasonable personal computers. In this case, please also include a script to reproduce only a subset of the results. If this is not possible, please contact the artifact evaluation chair early, but no later than before submission.
* **Examples of Usage** describe how to use your artifact in general accompanied by small examples.
If you cannot submit the artifact as requested or encounter any other difficulties in the submission process, please contact the artifact evaluation chair prior to submission. 

### Publication of Artifacts
To qualify for the artifacts available badge, the artifact must be made publicly and permanently available. We recommend to use services like e.g., [Zenodo](https://zenodo.org/) or [figshare](https://figshare.com/). In addition, the paper needs to reference to the artifact using its DOI. Therefore, we recommend to extend your paper with a data availability statement. We encourage all authors of artifacts to make their artifacts permanently available.

## Artifact Evaluation Process and Criteria
We aim to assess the artifacts themselves and not the quality of the research linked to the artifact, which is assessed by the SEFM 2024 program committee. The goal of our review process is to be constructive and to improve the submitted artifacts. Only, if an artifact cannot be improved to achieve sufficient quality in the given time frame or it is inconsistent with the paper, it should be rejected.

All artifacts are evaluated by the artifact evaluation committee. Each artifact will be reviewed by at least two committee members. Reviewers will read the accepted paper and explore the artifact to evaluate how well the artifact supports the claims and results of the paper. The evaluation is based on the following questions:
*	Is the artifact consistent with the paper and the claims made by the paper, e.g., does it significantly contribute to the generation of its main results?
*	Is the artifact complete, i.e., how many of the results of the paper are reproducible?
* Are the results of the paper reproducible through the artifact, e.g., can the included software be used to generate the results of the paper and included data be accessed and manipulated?
* Is the artifact well-documented?
* Is the artifact easy to use?
* Does the artifact provide a proper and explicitly documented license?
* Is the artifact publicly and permanently available?
* Is a DOI to the artifact provided and referenced in the paper?
* Is the artifact relevant for the associated paper and does it provide additional value?

The artifact evaluation is performed in the following two phases.
1.	**Test Phase**: Reviewers **check if the artifact is functional**, i.e., they look for setup problems (e.g., corrupted, missing files, crashes on simple examples, etc.). The authors are informed of the outcome of the test phase by the **test phase notification** deadline. If any problems are detected during the test phase, the authors are asked to **solve the problems** and answer the respective issue until the end of the **author respond period**. If no problems were detected, the reviewers will continue with the assessment phase directly after the test phase notification.
2.	**Assessment Phase**: In the assessment phase, reviewers will try to **reproduce** any experiments or activities and **evaluate** the artifact w.r.t the questions detailed above. The final review is communicated together with the awarded badges in the artifact notification.

## Artifact Evaluation Chair
[Marie-Christine Jakobs](https://www.sosy-lab.org/people/jakobs/), LMU Munich
