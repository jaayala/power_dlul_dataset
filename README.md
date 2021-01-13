Dataset providing a set of measurement of performance and power consumpetion of a virtualized Base Station (srseNB). The details of the experiments and the softwared and hardware used can be found in the paper:

Jose A. Ayala-Romero, A. Garcia-Saavedra, X. Costa-Perez, G. Iosifidis (2021). Bayesian Online Learning for Energy-Aware Resource Orchestration in Virtualized RANs. IEEE INFOCOM 2021.


**Configurations:**

"date": Timestamp of the measurement
"cpu_platform": CPU model of the computing platform running the BBU
"BW": Bandwidth of the LTE interface in number of resource block. For instance, BW = 50 -> 10 MHz
"TM": Transmission mode
"UL/DL": Indicates if we consider the Uplink (UL), the downlink (DL), or both (DLUL)
"traffic_load_dl": Downlink traffic load
"traffic_load_ul": Uplink traffic load
"txgain_dl": Transmission gain of the USRP implementing the BS 
"txgain_ul": Transmission gain of the USRP implementing the UE
"cpu_time": Ratio of the time assigned to the CPU that runs the BS process, [0, 1].
"number_active_cores": Number of active cores at the CPU
"pinning": when -1 no pinning is used
"cpu_config": configuration of the governor of the CPU
"selected_mcs_dl": Selected MCS on the downlink
"selected_mcs_ul": Selected MCS on the uplink
"selected_airtime_dl": Selected airtime on the downlink
"selected_airtime_ul": Selected airtime on the uplink

**Measurements:**

"mean_used_mcs_dl": Average MCS used during the experiment on the downlink
"mean_used_mcs_ul": Average MCS used during the experiment on the uplink
"bsr_dl": Average Buffer Status Report downlink
"bsr_ul": Average Buffer Status Report uplink
"gput_ul": Average Goodput uplink
"mean_snr_ul": Average SNR measured during the experiment on the uplink
"turbodec_it": Average number of turbo decoder iterations during the experiment
"dec_time": Average decoding time
"nRBs_ul": Average number of Resource Blocks used in the uplink
"num_ues": Number of UE associated with the BS
"thr_dl": Average throughput downlink
"thr_ul": Average throughput uplink
"bler_dl": Average Block Error Rate downlink
"bler_ul": Average Block Error Rate uplink
"tbs_dl": Average Transport Block Size downlink
"pm_power": Average power consumed by the BBU measured externally using the digital power meter
"pm_var": Variance of the power consumed by the BBU measured externally using the digital power meter
"pm_median": Median of the power consumed by the BBU measured externally using the digital power meter
"n_pm": Number of samples of consumed power taken by the digital power meter during the experiment
"rapl_power": Average power consumed by the CPU of the BBU measured using the RAPL functionality
"rapl_var": Variance of the power consumed by the CPU of the BBU measured using the RAPL functionality
"n_rapl": Number of samples of consumed power taken by the RAPL functionality during the experiment
"clockspeed": Average clockspeed of the CPU running the BBU
"airtime_dl": Average measured airtime on the downlink
"airtime_ul": Average measured airtime on the uplink
"cqi_dl": Average CQI value on the downlink
"cqi_ul": Average CQI value on the uplink
"fixed_mcs_flag": if 0, the value of the fields 'selected_mcs_dl' and 'selected_mcs_dl' is taken as an upper bound, i.e., the radio scheduler can select lower values for the MCS when it is required by the radio channel. If 1, the radio scheduler is forced to use these MCS values. When the channel quality is poor, decoding errors may occur.
"failed_experiment": If 1, it indicates that the experiment has failed due to decoding error.




## Citing Work
If you use any code please cite the following:
```
@inproceedings{ayala2021,
  title={Bayesian Online Learning for Energy-Aware Resource Orchestration in Virtualized RANs},
  author={Ayala-Romero, Jose A and Garcia-Saavedra, Andres and Costa-Perez, Xavier and Iosifidis, George},
  booktitle={{IEEE} Conference on Computer Communications, {INFOCOM} 2021},
  year={2021}
}
```



