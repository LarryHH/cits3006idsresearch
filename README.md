# Benchmarking IDS Systems
## Overview
This repository contains the necessary code and datasets for the research paper on benchmarking Intrusion Detection Systems (IDS). It includes various datasets and scripts to process and analyze the performance of different IDS systems.

## Datasets
The datasets included in this study are:
- BoT_IoT
- CICIDS2017
- CTU
- Mirai
- UNSW
These datasets are used to evaluate the effectiveness of the IDS systems.

## IDS Systems
The IDS systems evaluated in this research are:
- AOC-IDS
    - https://github.com/xinchen930/AOC-IDS
    - @inproceedings{zhang2024aoc,
        title={Aoc-ids: Autonomous online framework with contrastive learning for intrusion detection},
        author={Zhang, Xinchen and Zhao, Running and Jiang, Zhihan and Sun, Zhicong and Ding, Yulong and Ngai, Edith CH and Yang, Shuang-Hua},
        booktitle={IEEE INFOCOM 2024-IEEE Conference on Computer Communications},
        pages={581--590},
        year={2024},
        organization={IEEE}
        }
- HELAD
    - https://github.com/cdogemaru/CPIP
    - @article{zhong2020helad,
        title={HELAD: A novel network anomaly detection model based on heterogeneous ensemble learning},
        author={Zhong, Ying and Chen, Wenqi and Wang, Zhiliang and Chen, Yifan and Wang, Kai and Li, Yahui and Yin, Xia and Shi, Xingang and Yang, Jiahai and Li, Keqin},
        journal={Computer Networks},
        volume={169},
        pages={107049},
        year={2020},
        publisher={Elsevier}
        }
- NEGSC
    - https://github.com/renj-xu/NEGSC
    - @article{xu2024applying,
        title={Applying self-supervised learning to network intrusion detection for network flows with graph neural network},
        author={Xu, Renjie and Wu, Guangwei and Wang, Weiping and Gao, Xing and He, An and Zhang, Zhengpeng},
        journal={Computer Networks},
        volume={248},
        pages={110495},
        year={2024},
        publisher={Elsevier}
        }
- StratosphereLinuxIPS (SLIPS)
    - https://github.com/stratosphereips/StratosphereLinuxIPS

Modifications were made to Kitsune and HELAD to ensure that they output CSV files with the Root Mean Square Error (RMSE) scores.

File Structure
- /Archive: Contains working and older versions of code
- /AOC-IDS: Contains the AOC-IDS model with adapted code for accepting other datasets.
- /AOC-IDS Processing: Contains our dataset preprocessing code for the AOC-IDS model
- /BoT_IoT: Contains the BoT_IoT related processing scripts.
- /CICIDS2017: Contains the CICIDS2017 related processing scripts.
- /CTU: Contains the CTU related processing scripts.
- /EditedHELAD: Contains the HELAD IDS edited to output the RMSE output.
- /EditedKitsune: Contains the Kitsune IDS edited to output the RMSE output.
- /NEGSC: Contains the NEGSC model with adapted code for accepting other datasets.
- /NEGSC Processing: Directs to the /NEGSC/NEGSC.ipynb code for the preprocessing modifications
- /ResultsScripts: Contains the scripts used to process the results.
- /SDNN_submit: Contains the scripts required for the SDNN IDS
- /Stratosphere: Contains the BOTIOT assets for Stratosphere.
- /UNSW: Contains the UNSW related processing scripts.

## Usage Guide
For each of the folders in the repository, there are specific usage instructions.

Each dataset has to be processed to be used in the IDS systems, the processing of each dataset within its specific folder will result in a dataset that can be used within Kitsune and HELAD.

These output files can be processed through SDNN_submit/convert_kitsune_file.py to be used with SDNN.

After converting the datasets to the required format, the IDS folders have specific instructions for running converted output file through each IDS

After gathering the results for each combination of dataset and IDS, the ResultsScripts folder can be used to derive the results for the given dataset.