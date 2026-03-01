# Resting-State fMRI Functional Connectivity Pipeline
This project demonstrates a basic functional connectivity pipeline using resting-state fMRI data from a single participant. The goal is to examine correlations between the BOLD (Blood-Oxygen-Level-Dependent) signals of different brain regions in order to explore which areas show similar patterns of activity over time.
Functional connectivity analysis is commonly used in neuroscience to study how different regions of the brain may be functionally related. 

Data used include:
- The Harvard-Oxford cortical atlas to define brain regions
- The fMRI data used was of one adult participant from the movie-watching based functional MRI dataset from Nilearn, retrieved using nilearn.datasets.fetch_development_fmri

Methods used (pipeline steps):
- Load atlas and fMRI data from Nilearn
- Create time series by using NiftiLabelsMasker to to extract the mean BOLD signal from each atlas-defined brain region across time.
- Compute a correlation matrix. Pearson correlations were calculated between all regional time series to measure similarity in activity patterns.
- Visualize correlation matrix using a heatmap. Warmer colours indicate positive correlations and cooler colours indicate negative correlations.

Interpretation of Results:
The heatmap shows pairwise correlations between brain regions. Regions with strong positive correlations tend to have BOLD signals that rise and fall together over time. Negative correlations suggest opposite patterns of activity.
This analysis provides a simple example of how resting-state fMRI data can be used to explore functional relationships between brain regions. 

Future Directions:
- Completing pre-processing steps
- Working with multiple participants' fMRI data to complete group-level analysis
- Comparing resting-state and task-based fMRI data

Skills Demonstrated:
- Python (Numpy, Matplotlib)
- Data visualization and interpretation
- Neuroimaging analysis with Nilearn
