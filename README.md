# hCoCena - Horizontal integration and analysis of transcriptomics datasets

hCoCena is an R-package that allows you to integrate and jointly analyse multiple transcriptomic datasets or simply analyse a single dataset if you don't want to do any data integration! hCoCena uses network representations of the data as the basis for integration. You can find more details of how that works in our [paper](https://academic.oup.com/bioinformatics/advance-article/doi/10.1093/bioinformatics/btac589/6677225) . Below, you will find some info on how to install the package and tips for using it. 

## Installation
To install hcocena from this repo, run the codeline provided in the `install_hcocena.R` script.
To install versioned dependencies, use the script `install_versioned_dependecies.R`.

## Usage
**hCoCena is divided into 2 parts:** 

**1.** the main analysis that comprises the mandatory steps to process and integrate the data and

**2.** the satellite functions that offer you a plethora of analysis options in a pick & mix kind of fashion. 

The figure below illustrates this: the main analysis is at the center, while the satellite functions can be found in the orbits around it. 
A step-by-step walkthrough of the main analysis steps can be found in the `hcocena_main.Rmd`, the satellite functions are in the `hcocena_saltellite.Rmd`. 

hCoCena was written with user-friendliness and customizability in mind. We are doing our best to provide you with plenty of supplementary information that make the usage of the tool easy for you. You can also always extend the tool's functionalities with your on custom scripts and functions to adapt the analysis to your needs! For more details on hCoCena's object structure and where to find the outputs of different analysis steps for customization, please refer to the overview in the [Wiki](https://github.com/MarieOestreich/hCoCena/wiki/Structure-of-the-hcobject) and the extensive function documentations you can access from within R Studio.


![hCoCenaFig1](https://user-images.githubusercontent.com/50077786/158609782-2048c06e-0420-4c3f-8680-5d99f91d6905.jpg)

## Showcase
To rerun the showcase example from our paper you have three options:
1) Use our interactive analysis hosted by the Fastgenomics platform: https://beta.fastgenomics.org/analyses/detail-analysis-461f44b88207411f87669caccfb5ff8f
2) Use our docker image that comes with hcocena installed and includes all required data. When a container is launched, it starts a local RStudio Server session in your browser that let's you try out the tool on a small exmaple. Pull the image using `docker pull mo126/hcocena:showcase`.
3) To run it in an RStudio session on your local machine, install hcocena as described further up. Then, you can find the main- and satellite-markdowns in the `showcase` folder, including an `R` environment named `start_envo.RData`. This should be loaded at the very beginning, since it includes the pre-processed transcriptomics datasets and their annotation files. Note that the markdowns only contain the function showcased in the paper, which is only a small part of the available analysis options that you can find in `hcocena_satellite.Rmd`. It also need to be pointed out, that some of the analysis functions depend on other packages and data bases. Especially databases are frequently updated, thus, while they progress, the results may vary slightly from the originally reported ones. While hCoCena itself, including it's integration strategy, are reproducible, these 3rd party-services are something we simply cannot control.

## Wiki
For loads of additional information regarding the [satellite functions](https://github.com/MarieOestreich/hCoCena/wiki/Satellite-Functions), [community detection](https://github.com/MarieOestreich/hCoCena/wiki/Background-Info-on-the-Community-Detection-Algorithms) algorithms etc. please check out our carefully curated Wiki pages!
