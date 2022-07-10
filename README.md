
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

Required libraries:

pandas
numpy
seaborn
matplotlib
sklearn
imblearn

The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

The work done within this project was for the capstone project of Udacity’s Data Scientist Nanodegree. The goal was to demonstrate my understanding in the data science processes through a project that interests me. This project is about to classify songs into categories like Rock or Hip-Hop using predefined features created by The Echo Nest research group. I have chosen this project not only because I like music but because of the growing application of machine learning driven signal processing in other industries (like manufacturing, automotive etc) which I find very similar to the current project. In all cases one would have descriptive features derived from signals and could use for clustering or classifying the records to automatize engineering processes.

1. Problem statement
2. Metrics
3. Data exploration and visualization
4. Creating train and test sets
5. Scaling data
6. Building classification models
7. Compare models
8. Solving imbalanced dataset
9. Principal Component Analysis
10. Creating new models using PCA features
11. Summary
12. Outlook
13. Acknowledgement


## File Descriptions <a name="files"></a>

The two files that are used during this project contain the track's metadata and derived values created by The Echo Nest group. The first is in csv file format while the later is in json format. After reading the files we can explore their columns and values only printing the first few rows.
In the track metadata file the genre_top column indicates the type of the song; whether it is rock or hip-hop. Besides this one can find information e.g. about the composer, the date of the record and duration of the track.

## Results<a name="results"></a>

The goal of the project was to create a software solution which can distinguish song genres — like in this particular case rock and hip-hop songs — from each other using derived features.
The derived features (8 features were created for each song) were built by The Echo Nest research group.
Feature data was analyzed by plotting histograms, creating correlation matrix and summary statistics. Label vector countplot showed that there are much more rock songs in the dataset than hip-hop songs.
No strong correlation were found between features which is beneficial for a machine learning model.
Feature scaling was applied in order to avoid some features being too dominant. We have seen that tempo feature had values two order higher than the others.
Random Forest model was outperforming the two other (Logistic regression and Gradient Boosting Tree) models but hip-hop song label prediction performance was much behind rock label prediction capability.
Data balancing was then applied in order to overcome this issue, which proved to be successful. All model improved a lot, and Random Forest (which was already very good) is now able perfectly distinguish rock and hip-hop songs.
In order to still push the models to the limit PCA was applied to reduce feature numbers by creating new components, but this approach did not help at this particular dataset.

Blog post of the project: https://medium.com/@andrskriston/rock-or-hip-hop-algorithms-can-tell-us-608f9e09390f

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to The Echo Nest research group for the data.  

The Echo Nest github: https://github.com/orgs/echonest/repositories?type=all
