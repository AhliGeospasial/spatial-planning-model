Calibration of SPF and BLM with Marxan in Quantum GIS

1. Prepare the QMarxan plugin in Quantum GIS.
2. Prepare the input data files to be processed. The input must have a UTM coordinate system.
   The input data files consist of several types:
   - pu – Planning unit data with costs and attributes
   - spec – Species data, including targets and distributions
   - bound – Boundary length file for spatial connectivity
   - puvspr – Relationship between planning units and species presence
3. Conduct planning unit (pu) setup by creating an Area of Interest (AOI) covering the study area.
4. Once the AOI is set, create a planning grid using the QMarxan plugin.
5. Prepare conservation features and cost features according to regulations or your conservation area design.
6. Insert the conservation features into the planning unit and calculate conservation value using QMarxan.
7. Also, insert the cost features using vector and spatial query according to the predetermined score.
8. Perform the "Export to Marxan" step using QMarxan to generate pu.dat, spec.dat, bound.dat, and puvspr.dat.
9. Set the target proportion in spec.dat depending on the protection proportion (30-50%) and the Species Penalty Factor (SPF) to be weighted.
   The SPF used for this study is 1 because the importance of each biodiversity target objectives is same. 
10. An input.dat file will be generated to proceed to the next step.
11. Configure the scenario using the QMarxan plugin.
12. Set the Boundary Layer Modifier (BLM) according to scientific literature based on the study area.
    The higher the BLM value, the more clustered the conservation area design results.
    In this study, a BLM of 1000 is used to reduce conservation area costs.
13. Set the Number of Simulated Annealing Iterations in each use (NUMITNS).
    In this study, NUMITNS is set to 1000 iterations to reduce redundancy and increase solution variations.
14. Set the input and output file paths to be used.
15. Run Marxan using the input files, output files, and input.dat on your device.
16. Once completed, in Quantum GIS, use the QMarxan plugin to import the Marxan results.
    This step is done to view the ssoln or best solution per planning unit based on the provided input.
