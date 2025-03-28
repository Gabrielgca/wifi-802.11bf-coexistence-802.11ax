# Coexistence of 802.11bf and 802.11ax #
## Introduction

  This repository contains an ns-3 implementation and module extension of IEEE 802.11bf Wi-Fi Sensing version ns-3.40. As the standard IEEE 802.11bf is currently developing, this repository provides an ns-3 implementation to simulate and evaluate the sensing functionality in Wi-Fi technology based on the draft.


## Main Features
The implementation of Wi-Fi sensing in sub-7 GHz currently only supports the TB sensing measurement instance. Complete implementation is still ongoing while waiting for the final draft of IEEE 802.11bf. The main features of the current implementation are as follows:
- Facilitates simulation of Wi-Fi sensing and extracts some performance parameters (e.g., sensing latency)
- Facilitates the coexistence simulation with other Wi-Fi legacy protocols

To demonstrate the implementation please refers to this [file](/examples/wireless/wifi-bf-network.cc). This simulation code includes the setup of the network using IEEE 802.11bf standard and several scenarios to evaluate its performance and capabilities. The output from the simulation code is mainly one of the sensing KPIs, i.e. sensing latency. The following parameters are configurable for the simulation: 

| Name | Description |
| --- | --- |
| Network Structure | Number of AP and stations |
| Network layout | simple and 3GPP indoor office layout | 
| Sensing Parameters | frequency, bandwidth, CFP , instance number, sensing transmission types, sensing priorities |

## Keywords 
- WiFi Sensing, MU-OFDMA, PCF, Channel Sounding, ns3

## Usage example 
There is a [shell script](/output_run_info.sh) defined by the author to automate the output of the simulation code. Please refer to this file for understanding how to efficiently run the simulation. These are few tips for running the program:
- Build the ns3: ./output_run_info.sh build (type: debug, optimized)
  - example: ./output_run_info.sh build optimized
- Fast run: ./output_run_info.sh investigate (logging type: no_log, log_info, log_function) ("parameter") (logging file name)
  - example: ./output_run_info.sh investigate no_log "--nBss=2" twoBss
- Scenario run: ./output_run_info.sh (scenario name)
  - example: ./output_run_info.sh investigate multipleBssBf

! Remeber to change the save location in shell script. You may also need to follow some directory defined in the script

## References
If you use this module in your research, please cite following:
<details>
<summary>Bibtex</summary>


```@misc{keshtiarast2025nextgensensingmeetslegacy,
      title={When Next-Gen Sensing Meets Legacy Wi-Fi: Performance Analyses of IEEE 802.11bf and IEEE 802.11ax Coexistence}, 
      author={Navid Keshtiarast and Pradyumna Kumar Bishoyi and Ido Manuel Lumbantobing and Marina Petrova},
      year={2025},
      eprint={2503.04637},
      archivePrefix={arXiv},
      primaryClass={cs.NI},
      url={https://arxiv.org/abs/2503.04637}, 
}

```


</details>

## License
This software is licensed under the terms of the GNU GPLv2, as like as ns-3. See the [LICENSE](/LICENSE) file for more details.