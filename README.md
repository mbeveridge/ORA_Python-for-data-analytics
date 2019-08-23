# Learning Path: Python for Data Analytics

######  Data Exploration in Python: Best Practices for Developers -- Allen Downey


#### § Introduction to Data Exploration

* Opportunities and Goals
* The State of Data :: ["[Probably Overthinking It](https://www.allendowney.com/blog/)" blog ...([old](http://allendowney.blogspot.com/))]
* Data Optimism


#### § Getting Started

* Software Setup, IPython, and Import and Validation :: ["**nsfg.ipynb**"] ::
[*Prereqs : Core Python; Ideally objects and classes; Maybe NumPy and Pandas; Not much math (counting mostly); Logarithms*] [*I recommend Anaconda*] [*[repo](https://github.com/AllenDowney/DataExplorationInPython) to follow along*] [*@4'50 "When I load a dataframe, usually the first thing I do is print the `shape`"*] [*@5'03 `head()` for first 5 rows*] [*@6'42 `mean()` is a reasonable number*] [*@7'11 `describe()` to summarise a variable*] [*@8'00 `value_counts().sort_index()` for distribution of values*] [*@9'10 `loc[]` to select a particular row*] [*@9'27 replace some values with `np.nan` (unknown or unavailable data, NaN)*] [*@9'34 "The other thing I can use is `replace()`"*] [*@10'17 "The next step is usually to wrap that up in a function"*] [*@10'35 Validate data by comparing (distributions) between dataframe and code book*] [*@11'17 "And then the last step is I'll take those checks and I'll do at least one test for each variable, and turn that (in this case) into an `assert` statement ... So if anything breaks, I'll know about it. This is a form of regression testing"*]

* Data Organization :: [*Maintain the chain of custody. Apply software engineering principles to data (automated build, automated testing, version control)*]


#### § Visualizing Distributions

* PMFs and CDFs (Probability Mass Functions and Cumulative Distribution Functions) :: ["**distribution.ipynb**"] ::
[*@0'06 "My first step is to look at one variable at a time"*] [*@2'07 "It can be misleading to only look at summary statistics. I think it's very important to look at the shape of the whole distribution"*] [*2'39 "So let me show you the code [for PMF] and then we'll take a look at the results"*] [*@3'13 "51% of pregnancies end in the 39th week"*] [*@3'35 "The obvious thing that you want to do next is to make a visualisation" ...`.Hist(pmf)`, `.Pmf(pmf)`, `.Pdf(pmf)` (Probability density function)*] [*@5'35 "But PMFs are not always a good way to visualize distributions"*] [*@6'31 "Bin them ... The advantage there is that [wider bins] smooths things out"*] [*@7'27 "But there are still drawbacks to doing that. One is that binning is kind of a nuisance ... The other problem is that the whole process is kind of fragile"*] [*@8'17 "There is a better way to do all of this, which is to use CDFs"*] [*@9'35 "Here's what it looks like as a visualization"*] [*@10'30 "Cumulative Probability always goes from 0-1. You can read the CDF in 2 possible directions" (ie. start from either x- or y-axis)*] [*@11'59 "So, this distribution has a sigmoid shape ... steep in the middle, meaning that there are many values there"*] [*@12'24 "You can plot multiple CDFs on the same axis and [comparing] you can get a very clear picture of where they differ and what those differences are"*] [*@13'29 "By comparison, if you try to plot multiple PMFs on the same axis, it's not so easy to see [differences]" (You could smooth PMFs, using Kernel Density Estimation (to create PDFs), if audience won't understand CDF)*]


#### § Relationships Between Variables

* Scatterplots :: ["**scatter.ipynb**"] ::
[*@1'58 "`.dropna()` will drop any rows from this table that contain NA values - NaN's"*] [*@2'37 "We can use the `.describe()` function again"*] [*@3'15 "I'm going to start small ... with a sample of just 1000 values" (from full dataset of ~400k)*] [*@4'39 "I'm going to (just) change the limits of the display to focus in on the part we're most interested in" (to exclude outliers)*] [*@4'47 "The other thing I'm going to do, in order to break up these columns of data, is to `.Jitter()` the data"*] [*@6'40 "One simple way to fix [saturation ...else outliers are over-emphasised] is just to adjust the alpha setting and the size of the markers"*] [*@7'38 "I'm going to increase the size of the sample one more time ... to 100k"*]
