# Inserting Fakes into DM pipeline 

The basic idea is two-fold
- Pre-data Studies: Create simulated-only or data-simulated hybrid images and process them through the DM pipeline to test the output. Simulated-only images refer to images that have simulated astrophysical objects, noise backgrounds, and sources. Data-simulated hybrid images refer to images of simulated variable objects injected onto real data images of other astrophysical objects and sky backgrounds.
- Runtime Studies: Insert simulated variable objects into the images obtained by data and run the usual DM pipeline on these images as well. 
## Use Cases
- Monitor the efficiency of the DM pipeline in detecting transients of the kind simulated
    - *Is independent single band monitoring sufficient or do we need multi-band monitoring?*
- The efficiency is important in understanding the numbers of transients (eg. rates of SN types) 

### Monitoring the efficiency of the DM pipeline:

We can define the efficiency of the pipeline in detecting transients of a certain kind under specific circumstances as the ratio: 
(number of detected transients / number of such transients ) under specific circumstances. 
 
The efficiency must include thresholds/application of ML algorithms to determine the number of detected objects. Aside from the efficiency, it is important to determine the number of False Positives from the detection algorithm.
 
*Is there any rough plan of doing probabilistic detection, where we treat objects as detected with a probability and use that in analyses? Is efficiency as defined above still useful?*

We expect the efficiency to depend on 
- Signal to noise of the transient. The noise  can be further decomposed into sky noise, and noise due to the surface brightness of the host galaxy
- Seeing conditions at the time of observation
- Airmass of the observation

### Methodology for runtime monitoring
- Do we insert fakes in data that is only processed with fakes? Or do we have a first processing of the real data (without fakes) and do the fake computation in parallel a second time after inserting the fake (no loss of data). 
## Requirements for Fakes
-  Apparent magnitude of the signal
- *In band spectrum (for chromatic effects)?* 
