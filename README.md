# Spatial_Analytics

### Christian K. Kjeldsen 

This repositoy contains the code, data, and output files for my exam project, "A geostatistical analysis of the equitability of the distribution of municipal trees in Copenhagen" for the Spatial Analytics 2026 spring course.

## Data

Three datasets are loaded in this project. The districts dataset is available in the data/ folder and is loaded from there.
The tree dataset in its entirety is downloaded from an URL in the Rmarkdown, but a 500 tree test dataset is provided in the data/ folder, which can be loaded for code verification purposes. If the test set is created as object "trees", the code can be run without changing variable names. If so, do not run line 53-54. The BBR data is downloaded from an URL in the Rmarkdown. 

## Requirements 

This code was run on locally downloaded R version 4.5.3 and RStudio version 2026.1.0.392. 

In order to run this code, first install the required packages in a new codecell in the Exam_analysis.Rmd by executing: 

```r
install.packages("rmdformats")
install.packages("tmap")
install.packages("sf")
install.packages("tidyverse")
install.packages("spatstat")
install.packages("sfarrow")
install.packages("mapview")
install.packages("jsonlite")
```

The Rmd document expects a data/ folder and output/ folder at the same level of Exam_analysis.Rmd, so to run this project locally make sure to preserve the repository structure: 

```
Spatial_Analytics/
├── data/
│   └── districts.json
│   └── trees_500_test_data.json
├── output/
│   └── combined_tree_density_map.png
│   └── [4 other .png files]
└── Exam_analysis.Rmd
```

The output files are saved locally to the output/ folder. Make sure to change the path between C:// and output/ to match the path on your machine in the codecells that save maps as images. The analysis can be completed without saving any images. 


## Output

The Rmarkdown creates a total of 5 maps and saves them to the output/ folder. Two of them, combined_tree_density_map.png and trees_per_res_building_map.png are reproduced in the report, while the three individual maps are not used in the report. 