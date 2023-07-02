

# FPSecretBench: A Dataset of False Positive Software Secrets Reported by Nine Secret Detection Tools

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7571266.svg)](https://doi.org/10.5281/zenodo.7555981)

*The research work is accepted at the Technical Track of the International Symposium on Empirical Software Engineering and Measurement (ESEM 2023)*

## Table of Contents
   * [Introduction](#introduction)
   * [How To Use](#how-to-use)
   * [Data Overview](#data-overview)
   * [License](#license)
   * [Ethics](#ethics)
   * [How to Contribute](#how-to-contribute)
   * [Authors](#authors)

## Introduction

According to GitGuardian’s monitoring of public GitHub repositories, secrets sprawl continued accelerating in 2022 by 67% compared to 2021, exposing over 10 million secrets (API keys and other credentials). Though many open-source and proprietary secret detection tools are available, these tools output many false positives, making it difficult for developers to take action and teams to choose one tool out of many. To our knowledge, the secret detection tools are not yet compared and evaluated. The goal of our study is to aid developers in choosing a secret detection tool to reduce the exposure of secrets through an empirical investigation of existing secret detection tools. We present an evaluation of five open-source and four proprietary tools against a benchmark dataset.

**In addition to comparing nine secret detection tools, we have curated a dataset *FPSecretBench*, which contains the false positives reported by the secret detection tools scanned on the benchmark dataset ([SecretBench](https://github.com/setu1421/SecretBench)). The dataset will aid in expediting the research on improving the accuracy of the tools.** 

## How to Use

The dataset is stored in Google BigQuery. First, you need to create a Google Cloud Account. Google Cloud gives a $300 free credit after opening the account. You can run SQL queries in Google BigQuery to access the false positive secrets.

 - **Google BigQuery Dataset id (*dev-range-332204.fpsecretbench*):**  Google BigQuery contains false positive secrets with additional metadata information regarding the secrets such as repository name, commit id, file path, and start line of where the false positive secret is reported. More details of the metadata is described in [Data Overview](#data-overview) section.

**Important:** *The researchers and developers who want to use our dataset must contact us. Since the dataset may contain mislabeled true positives, a data protection agreement has to be signed with us to avoid any unethical use of the data. Later, we will give access to the dataset using their email addresses.*

## Data Overview

The dataset consists of the false-positive secrets reported by nine secret detection tools below when scanned on the **[SecretBench](https://github.com/setu1421/SecretBench)** dataset. The SecretBench is a benchmark dataset consisting of 818 public GitHub repositories.

|Tool Name|# False Positive Secrets|
|--------|--------|
|[git-secrets](https://github.com/awslabs/git-secrets)|89,584||
|[Gitleaks](https://github.com/gitleaks/gitleaks)|24,885|
|[Repo-Supervisor](https://github.com/auth0/repo-supervisor)|177,658|
|[TruffleHog](https://github.com/trufflesecurity/trufflehog)|85,556|
|[Whispers](https://github.com/Skyscanner/whispers)|414,068|
|[ggshield](https://github.com/GitGuardian/ggshield)|134,769|
|[SpectralOps](https://spectralops.io/)|1,543,217|
|[GitHub-scanner](https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories)|429|
|Commercial X|64,933|

## License:

This project is licensed under the terms of the MIT license. Please check [LICENSE](https://github.com/setu1421/FPSecretBench/blob/main/LICENSE) for more details.


## Ethics:
Since our dataset may contain sensitive information, we will make available to dataset only to researchers and tool developers. The researchers and tool developers will sign an agreement to protect the data from any unethical use.

### How to Contribute

Please email us if you want to contribute. See [Authors](#authors) section for contact information.

## Authors:
 - Setu Kumar Basak (sbasak4@ncsu.edu)
 - Jamison Cox (jcox3@ncsu.edu)
 - Bradley Reaves (bgreaves@ncsu.edu)
 - Laurie Willams (lawilli3@ncsu.edu) 
 
## Cite our work:

```
@article{basak2023secretbench,
  title={SecretBench: A Dataset of Software Secrets},
  author={Basak, Setu Kumar and Neil, Lorenzo and Reaves, Bradley and Williams, Laurie},
  journal={arXiv preprint arXiv:2303.06729},
  year={2023}
} 

