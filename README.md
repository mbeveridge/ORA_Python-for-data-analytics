# Learning Path: Python for Data Analytics

######  Data Exploration in Python: Best Practices for Developers -- Allen Downey


#### § Introduction to Data Exploration

* Opportunities and Goals
* The State of Data :: ["[Probably Overthinking It](https://www.allendowney.com/blog/)" blog ...([old](http://allendowney.blogspot.com/))]
* Data Optimism

#### § Getting Started

* Software Setup, IPython, and Import and Validation :: [*Prereqs : Core Python; Ideally objects and classes; Maybe NumPy and Pandas; Not much math (counting mostly); Logarithms*] [*I recommend Anaconda*] [*[repo](https://github.com/AllenDowney/DataExplorationInPython) to follow along*] [*@4'50 "When I load a dataframe, usually the first thing I do is print the `shape`"*] [*@5'03 `head()` for first 5 rows*] [*@6'42 `mean()` is a reasonable number*] [*@7'11 `describe()` to summarise a variable*] [*@8'00 `value_counts().sort_index()` for distribution of values*] [*@9'10 `loc[]` to select a particular row*] [*@9'27 replace some values with `np.nan` (unknown or unavailable data, NaN)*] [*@9'34 "The other thing I can use is `replace()`"*] [*@10'17 "The next step is usually to wrap that up in a function"*] [*@10'35 Validate data by comparing (distributions) between dataframe and code book*] [*@11'17 "And then the last step is I'll take those checks and I'll do at least one test for each variable, and turn that (in this case) into an `assert` statement ... So if anything breaks, I'll know about it. THis is a form of regression testing"*]

* Data Organization :: [*Maintain the chain of custody. Apply software engineering principles to data (automated build, automated testing, version control)*]

#### § Visualizing Distributions

* PMFs and CDFs


