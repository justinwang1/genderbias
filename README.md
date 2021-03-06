# Analysis of Gender Bias in Statistical Journals

The goal of the project is to assess whether gender bias exists in statistical journals and in the academic statistics world in general. To do so, we analyzed whether there exists a significant disparity in citation counts between papers with male and female (first) authors, that could not be explained by common confounding factors such as seniority (job title) or country of employment. The data was collected by scraping data from the four largest statistical journals, Google scholar, and the Mathematics Geneology Project. Scraping, cleaning, and combining of data were performed in Python. Some further cleaning and the analysis were performed in R. A resubmission of this work is currently in progress to the journal Annals of Applied Statistics. 


## Brief description of data

Consists of 3,246 journal papers with 1,889 unique authors. There are 6 variables total: citation count (response), gender, publication year, year obtained PhD, job title (including seniority if in academia), employment country. 

## Results 
There is a significant disparity in citation counts between papers with male and female (first) authors, but they can be largely explained by two primary factors: A relatively small number of highly prolific authors with high citation counts (mostly male), and the fact that there appear to be less women at higher seniority positions in academia (Professor or Distinguished Professor). From a sociological perspective, I do not feel qualified to comment on whether this constitutes gender bias, but the data does seem to suggest that the statistics world is trending in a direction of greater equality. 

## Description of files

1. *scrape.py*. Scrape information from statistical journals. Some of the scripts used to scrape have been lost, and this file preserves everything I could find from my scraping scripts. 
2. *cleanauthors.py*. Store authors information into a dictionary to make it much easier to match authors with their papers and figure out how many authors are unique. 
3. *genderdetection.py*. Use an API to determine the gender (or likely gender) of an author given their name. Some authors returned Unknown and needed to be identified through other means. 
4. *cleandata.R*. After data has been compiled, perform cleaning tasks such as removal or imputation of missing fields and combining similar categories of certain categorical variables. 
5. *analysis.R*. Exploratory analysis and modelling of the data. 
6. *genderbiasdata.txt*. Text file containing the dataset. 
