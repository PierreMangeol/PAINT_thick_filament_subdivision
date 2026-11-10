# PAINT_thick_filament_subdivision

Code used to analyze DNA-PAINT data and extract Drosophila titin epitopes positions

## What is this about?

The codes you will find here were used to analyze the data of Sane _et al._ 2026

Intact Drosophila flight muscles were imaged with DNA-PAINT and super-resolved images were recontructed with [Picasso](https://github.com/jungmannlab/picasso).

In a first step, from Picasso, individual myofibrils were selected. Localizations were either saved in separate files.

# Single and two band analysis
In the first step, from the selected myofibrils (multiple files), the bands were detected and the bands that were good for further analysis were saved in s csv file (Step 1 Single file...)
In the next step, all the compiled bands were analysed to report width and position (Step 5 All_dataset_...)
And finally the sarcomere lengths were extracted from the detected band positions (Step 6 Extract sarcomere length..)
The plots were made using (Figure....)

Band distance fit.ipnb uses the band widths from the output csv files from Step 6 - single band - Extract sarcomere length V1.0 to fit two Gaussians within the single band width and reports the distance between these gaussians

# Semi manual analysis
For semi manual analysis (for Actin), the code fits a Gaussian to the manually selected regions within the myofibril

# Block analysis
For block analysis, the edge of the block is detected within manually selected regions of the myofibril using Changepoint_Detection. 
Block averages.ipynb is used to align multiple sarcomere that have the edges detected using Changepoint detection. 


The selected myofibrils are saved as seperate files using Picks_to_presentation_Picasso.ipynb This filters the picked localisations for noise and long staying cluster and rotates the myofibrils to make them horizontal

The Merge_myofibrils compiles different files from  Picks_to_presentation_Picasso.ipynb into a single file.  
 
