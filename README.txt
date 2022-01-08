Tick Densities and Lyme Disease Prevalence in the Scottish Outer Hebrides:

This python script enables basic data analysis and the generation of heatmaps through the google maps platform for epidemiological data in which coordinate data is available. The example data provided is available within the supplementary information section of: Millins, C., Leo, W., MacInnes, I., Ferguson, J., Charlesworth, G., Nayar, D., Davison, R., Yardley, J., Kilbride, E., Huntley, S. and Gilbert, L., 2021. Emergence of Lyme disease on treeless islands in Scotland, UK. Emerging Infectious Diseases, 27(2), pp.538-546.

This script has two main sections: 

An initial section which performs some basic data analysis and visualisation in the form of a linear regression model and boxplot diagram.

The second section can be used to generate google maps heatmaps and random points at which data collection can be performed, prior to also mapping these points. 

The script can be edited in a number of ways to:

Perform more complex data analyss. 
Plot different epidemiological data. 
Generate sample sites in alternative manners. 

Before running:

Ensure that the following packages available natively within anaconda are installed: 

	Pandas
	sklearn
	matplotlib
	seaborn
	numpy
	
Additionally, the gmplots package must be installed for this script to function. A line to install this package is included within the script that must be run on first use. 

Running: 

	1. Ensure that the python script (SWBioAssessment.ipynb) and data to be studied are in the same folder. Example data has been named ‘LDData.csv’.

	2.  If using another dataset, ensure that missing coordinates or rows containing longitudes/latitudes in different formats are filtered out. 
	
	3. Cells 22 and 23 contain the code necessary to generate the data enabling heatmap creation:
		data = df.loc[df.index.repeat(df.column)]
By altering ‘column’ you can change the variable for which the heat map is generated. Note that to achieve a heat map with reasonable resolution using this method, data manipulation may need to be employed (for instance halving the repeated output). 

	4. If using sample data, please select coordinates from Barra, South Uist, Benbecula, North Uist or Harris and input 	them when requested by cells 30 (longitude) and 31 (latitude). An example being 57.267598 and -7.320495. Note that the range covered by the randomly generated sample points may vary substantially for attitudes closer to the equator/poles. 

	5. Generated html map files can be opened in Jupyter labs by double clicking on the files (by default 'TickDensityMap.html', 'LDPrevalenceMap.html’ and 'randomSampling.html') and selecting ‘Trust HTML’ which should appear in the upper left corner or by opening the html file directly outside of Jupetyr lab. 

Using the example data, this python script has been used to indicate that in high tick density samples, as densities increase, Lyme disease prevalence also increases. The script proceeds to generate heatmaps that demonstrate lower tick densities in coastal machair than in other habitats, as well as visualising lyme disease prevalence in ticks at high tick density sample sites. 

By allowing citizen scientists to perform tick drags and calculate tick denisties at 5 sites for which  they can easily access that are generated within the script we may be able to also estimate Lyme disease prevalence at these sites. Such data could be used to generate large and publicly accessible data libraries through the google maps platform, a platform that is widely available and free. This could have numerous public health applications in regards to informing the public of Lyme disease/other tick born disease prevalence at different locations. 