# Unraveling the Mystery of Childbed Fever: A Modern Take on Dr. Semmelweis' 19th Century Data
<img src="https://i.imgur.com/gugIA5r.png" width=700>

## Project Description
Dr. Ignaz Semmelweis was a Hungarian physician born in 1818 who worked in the Vienna General Hospital.
In the past people thought of illness as caused by "bad air" or evil spirits.
But in the 1800s doctors started looking more at anatomy, doing autopsies and started making arguments based on data.
Dr. Semmelweis suspected that something was going wrong with the procedures at Vienna General Hospital.
Semmelweis wanted to figure out why so many women in maternity wards were dying from childbed fever (i.e., [puerperal fever](https://en.wikipedia.org/wiki/Postpartum_infections)).

The primary objective of the project is to analyze the data gathered by Dr. Semmelweis and determine the cause of the elevated mortality rate among women.

**Main questions to answer:**
1. What caused the elevated mortality rate among women up until 1846? 
2. Did the procedure introduced by Dr. Semmelweis lead to a reduction in the death rate among women?

## Dataset Overview
### Source
Dr Semmelweis published his research in 1861. There are the scanned pages of the [full text with the original tables in German](http://www.deutschestextarchiv.de/book/show/semmelweis_kindbettfieber_1861),
 an excellent [English translation can be found here](http://graphics8.nytimes.com/images/blogs/freakonomics/pdf/the%20etiology,%20concept%20and%20prophylaxis%20of%20childbed%20fever.pdf).

### Dataset structure
The dataset comprises 2 .csv files:
* `annual_deaths_by_clinic.csv` covering the years from 1841 through 1846 (12 entries)
* `monthly_deaths.csv` covering the years from 1841 through 1849 (98 entries)

## Setup & Requirements
Follow these steps to get the data analysis project up and running on your local machine.

### Prerequisites
1. **Python**: This project requires Python 3.9 or higher.
If you don't have Python installed, [download and install](https://www.python.org/downloads/) the latest version.
2. **Jupyter Notebook**: Jupyter Notebook is used for the interactive analysis. If you don't have it, install it using pip:
``pip install jupyter``

### Setting Up a Virtual Environment (Recommended)
It's recommended to set up a virtual environment to avoid any package conflicts.
1. Install `virtualenv` if not installed: ``pip install virtualenv``
2. Navigate to the project directory and create a virtual environment: ``virtualenv venv``
3. Activate the virtual environment:
    - **Windows**: ``.\\venv\\Scripts\\activate``
    - **macOS/Linux**: ``source venv/bin/activate``

### Installing Required Libraries
With the virtual environment activated, install the necessary libraries using:
``pip install -r requirements.txt``

Python libraries used:
* pandas
* numpy
* seaborn
* plotly
* matplotlib

### Getting the Data
This project uses the `UCI ML housing` dataset.
1. Download the dataset from the project repository.
2. Place the downloaded dataset in the same directory.

### Running the Notebook
With everything set up, start the Jupyter Notebook server: ``jupyter notebook``
Navigate to the desired notebook and you're ready to start your analysis!

## Methodology
* Exploratory data analysis
* Diagnostic analysis
* Descriptive statistics
* Statistical analysis (t-test, Kernel Density Estimate)
* Time series analysis

## Findings & Conclusions
* Discovered that clinic 2, which was staffed by female midwives, had a consistently lower death rate than clinic 1 (staffed by all-male doctors and medical students).
Based on this insight from data and the pathologist's death, who worked at clinic 2, Dr. Semmelweis implemented an obligatory handwashing procedure. 
* The death rate per birth dropped dramatically after handwashing started (5.0x improvement).
* The difference in means is highly statistically significant:
  * p-value: 0.00002985%
  * t-statistic: 5.512