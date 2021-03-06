R introduction
================
Kasper Welbers & Wouter van Atteveldt

-   [Introduction](#introduction)
    -   [What is R and why should you learn it?](#what-is-r-and-why-should-you-learn-it)
    -   [Purpose of this tutorial](#purpose-of-this-tutorial)
-   [Getting started with R](#getting-started-with-r)
    -   [Installing R](#installing-r)
    -   [Installing RStudio](#installing-rstudio)
    -   [Using RStudio](#using-rstudio)
    -   [Running code from the R script](#running-code-from-the-r-script)
    -   [Assigning values to names](#assigning-values-to-names)
        -   [Values can be anything](#values-can-be-anything)
    -   [Using functions](#using-functions)
-   [Data analysis in R](#data-analysis-in-r)
    -   [Step 1: Create an RStudio project](#step-1-create-an-rstudio-project)
    -   [Step 2: Installing and using new packages](#step-2-installing-and-using-new-packages)
    -   [Step 3: Reading data into R](#step-3-reading-data-into-r)
    -   [Step 4: Cleaning data](#step-4-cleaning-data)
    -   [Step 5: Visualization](#step-5-visualization)
    -   [Step 6: Statistical analysis](#step-6-statistical-analysis)
-   [Where to go from here](#where-to-go-from-here)

Introduction
============

What is R and why should you learn it?
--------------------------------------

R is an open-source statistical software language, that is currently among the most popular languages for data science. In comparison to other popular software packages in social scientific research, such as SPSS and Stata, R has several notable advantages:

-   R is a programming language, which makes it much more versatile. While R focuses on statistical analysis at heart, it facilitates a wide-range of features, and virtually any tool for data science can be implemented.
-   The range of things you can do with R is constantly being updated. R is open-source, meaning that anyone can contribute to its development. In particular, people can develop new *packages*, that can easily and safely be installed from within R with a single command. Since many scholars and industry professionals use R, it is likely that any cutting-edge and bleeding-edge techniques that you are interested in are already available. You can think of it as an app-store for all your data-science needs!
-   R is free. While for students this is not yet a big deal due to free or cheap student and university licences, this can be a big plus in the commercial sector. Especially for small businesses and free-lancers.

The tradeoff is that R has a relatively steep learning curve. Still, learning R is not as bad as people often fear, and with thanks to the rising popularity of data science there are now many footholds that make learning and using R easier and--dare we say--fun. In this course you will learn the core basics, and see how this immediately grants you access to using cutting-edge techniques.

Purpose of this tutorial
------------------------

The focus of this tutorial is to get you started with R, and to see how easy it is to start doing some cool stuff. We will not yet dive into how R and the R syntax really work, so do not be allarmed if you do not understand the code that you'll be using. For now, just focus on getting R running, getting familiar with how to run code, and playing around with it.

Getting started with R
======================

For the current course material, you will need to install two pieces of software.

-   *R* is the actual R software, that is used to run R code.
-   *RStudio* is a graphical user interface (GUI) that makes working with R much easier. While it is not required to use R, and there are other GUI's available, using RStudio is highly recommended.

Both programs can be downloaded for free, and are available for all main operating systems (Windows, macOS and Linux).

Installing R
------------

To install R, you can download it from the [CRAN (comprehensive R Archive Network) website](https://cran.r-project.org/). Do not be alarmed by the website's 90's asthetics. R itself is cold, dry, no-nonsense software. The decoration comes with RStudio.

Installing RStudio
------------------

The [RStudio website](https://www.rstudio.com/) contains download links and installing instructions. You will need to install the free *RStudio Desktop Open Source License*. Note that the expensive licences do not offer better features or anything, but just offer additional support and a commercial licence. You can also use the free version when doing commercial research, but with an AGPL licence.

Using RStudio
-------------

Once you have installed R and RStudio, you can start by launching RStudio. If everything was installed correctly, RStudio will automatically launch R as well.

The first time you open RStudio, you will likely see three separate windows. The first thing you want to do is open an R Script to work in. To do so, go to the toolbar and select File -&gt; New File -&gt; R Script.

You will now see four windows split evenly over the four corners of your screen:

-   In the **top-left** you have the text editor for the file that you are working in. This will most of the time be an R script or RMarkdown file.
-   In the **top-right** you can see the data and values that you are currently working with (environment) or view your history of input.
-   In the **bottom-left** you have the console, which is where you can enter and run code, and view the output. If you run code from your R script, it will also be executed in this console.
-   In the **bottom-right** you can browse through files on your computer, view help for functions, or view visualizations.

While you can directly enter code into your console (bottom-left), you should always work with R scripts (top-left). This allows you to keep track of what you are doing and save every step.

Running code from the R script
------------------------------

Copy and paste the following example code into your R Script. For now, don't bother understanding the syntax itself. Just focus on running it.

``` r
3 + 3
2 * 5
6 / 2
"some text"
"some more text"
sum(1,2,3,4,5)
```

You can **run** parts of the code in an R script by pressing Ctrl + Enter (on mac this is command + Enter). This can be done in two ways:

-   If you select a piece of text (so that it is highlighted) you can press Ctrl + Enter to run the selection. For example, select the first three lines (the three mathematical operations) and press Ctrl + Enter.
-   If you haven't made a selection, but your text cursor is in the editor, you can press Ctrl + Enter to run the line where the cursor is at. This will also move the cursor to the next line, so you can *walk* through the code from top to bottom, running each line. Try starting on the first line, and pressing Ctrl + Enter six times, to run each line separately.

Assigning values to names
-------------------------

When running the example code, you saw that R automatically **evaluates** expressions. The calculation 3+3 evaluates to 6, and 2\*5 evaluates to 10. You also saw that the **function** *sum(1,2,3,4,5)* evaluates to 15 (the sum of the numbers). We'll address how to use R as a calculator and how to perform functions at a later time. For now, one more thing that you need to know about the R syntax is how values can be **assigned** to names.

In plain terms, **assignment** is how you make R remember things by assigning them to a name. This works the same way for all sorts of values, from single numbers to entire datasets. You can choose whether you prefer the equal sign (=) or the arrow (&lt;-) for assignment.

``` r
x = 2
y <- "some text"
```

Here we have remembered the number 2 as **x** and the text "some text" as **y**. If you are working in RStudio (which you should), you can now also see these names and values in the topright window, under the "Environment" tab.

We can now use the names to retrieve the values, or to use these values in new commands.

``` r
x * 5
```

Note that you shouldn't type the line `## [1] 10`: in this tutorial, lines starting with `##` show the *output* of commands (2 \* 5 = 10).

### Values can be anything

Above we assigned single values to names, but in R, any type of data can be assigned to a name. This includes the rectangular data.frames that you all know and love from programs such as Excell and SPSS. Here we create a small example data.frame and assign it to the name `d`.

``` r
d = data.frame(age = c(19,17,20,24),
               gender = c('F','F','M','M'))
```

Now `d` refers to an entire data.frame.

``` r
d
```

The nice thing is that in R we can work with multiple data.frames simultaneously (in SPSS your data is always a single data.frame). This makes it much easier to work with complex data or to combine data from different sources.

Using functions
---------------

In R, `functions` are the way in which you get stuff done.

There are many correct and formal ways to define what functions are, but for the sake of simplicity we will focus on an informal description of how you can think of functions in R:

-   A function has the form: `output = function_name(argument1, argument2, ...)`
    -   **function\_name** is a name to indicate which function you want to use. It is followed by parentheses.
    -   **arguments** are the input of the function, and are inserted within the parentheses. Arguments can be any R object, such as numbers, strings, vectors and data.frames. Multiple arguments can be given, separated by commas.
    -   **output** is anything that is returned by the function, such as vectors, data.frames or the results of a statistical analysis. Some functions do not have output, but produce a visualization or write data to disk.
-   The purpose of a function is to make it easy to perform a (large) set of (complex) operations. This is crucial, because
    -   It makes code easier to understand. You don't need to see the operations, just the name of the function that performs them
    -   You don't need to understand the operations, just how to use the function

For example, say that you need to calculate the square root of a number. This is a very common thing to do in statistical analysis, but it actually requires a quite complicated set of operations to perform. This is when you want to use a function, in this case the `sqrt` (square root) function.

``` r
sqrt(5)
```

Here `sqrt` is a rather simple function, but the essence of working with functions is the same for more complex operations, such as linear regression. Once you learn how to use functions, you get access to a vast range of techniques. You can look at the function documentation by typing a questionmark before the function name, and running the line of code

``` r
?sqrt
```

This documentation might seem a bit complicated at first glance, but all function documentation follows a standard structure. Once you understand this structure, you can quickly learn how to work with any function that you need.

Data analysis in R
==================

As you see above, there is quite some stuff to learn before you can get started. This really isn't that complicated, but it simple takes a bit of practice. At the end of this document we provide some information on where you can find practice material.

For now, let's first do some actual data crunching! In this example we will provide you with some code to run, but we do not expect you to immediately understand it. The main purpose is to show you a bit of what you can do in R, have you practice a bit with running code, and teach you some of the basics along the way.

Step 1: Create an RStudio project
---------------------------------

For this example, we'll start by making a *project* in Rstudio. This is essentially a folder on your computer in which you can store the R files and data for a project that you are working on. While you do not necesarily need a project to work with R, they are very convenient, and we strongly recommend using them.

To create a new project, go to the top-right corner of your RStudio window. Look for the button labeled **Project: (None)**. Click on this button, and select New Project. Follow the instructions to create a new directory with a new project. Name the project "R introduction".

Now, open a new R script (in toolbar: `File -> New File -> R script`) and immediately save it (in toolbar: `File -> Save`, or press ctrl-s). Name the file **my\_first\_r\_script.r**. In the bottom-right corner, under the **Files** tab, you'll now see the file added to the project. The extension **.r** indicates that the file is an R script.

For the remainder of this example, you can copy-paste all of the code into your **my\_first\_r\_script.r** file.

Step 2: Installing and using new packages
-----------------------------------------

The standard install of R already provides many functionalities, but R is designed to work with `packages`. An R packages is, simply put, a container with functions that you can use to perform certain techniques. For example, the `tidyverse` package provides many functions for reading, manipulating and visualizing data, and the `quanteda` package provides functions for performing text analysis in R. The popularity of R is largue due to the very active open-source community. The most popular archive, CRAN, currently has over 15.000 packages!

Each of these packages can be installed with a simple line of code: `install.packages("package_name")`. Here we use this to install the `tidyverse` package, that we'll use for this tutorial. This is quite a large package (its actually a collection of packages), so it might take a little time. Note that tidyverse has to be between quotes.

``` r
install.packages('tidyverse')
```

You only need to install a package once on your computer. When you then want to use this package, you need to run `library(package_name)`. This tells R: "I want to use this package in my current session".

``` r
library(tidyverse)
```

The `tidyverse` is a bit special, because it's actually a collection of packages. When you run the code above, you see that several packages are opened, such as `readr`, `dplyr` and `ggplot2`. Below you'll see that this collection of packages allows us to do many cool things.

Step 3: Reading data into R
---------------------------

Now, our first step is to load some data into R. For this we will be using the `read_csv` function (from the `readr` package, which is part of the tidyverse), which allows you to read csv (comma separated values) files. The first argument to the `read_csv` function is the location of the file. This can be a location on you own computer, but also a URL for a file on the internet. Here we use an open dataset published by [Houston Data Visualisation github page](https://github.com/houstondatavis/data-jam-august-2016). In our analysis, we'll use this data to analyse the relation between college education and household income. We assign the data to the name `facts`.

``` r
facts = read_csv("https://raw.githubusercontent.com/houstondatavis/data-jam-august-2016/master/csv/county_facts.csv") 
```

Let's take a first look at the data. We can do this by simply running the name facts.

``` r
facts
```

We see that this only shows a part of the data, simply because the data is too big. At the top, we see that the data has 3195 rows and 54 columns. From Excell and SPSS you might be used to the idea that you can see all your data. This is convenient, but for large datasets this can become slow (or impossible), so it's not the default in R. If you reallly do want to look at the entire dataset, you can use the `View` function. This opens a new tab in Rstudio with the data (you can switch tabs in the same way as you can switch tabs in you webbrowser).

``` r
View(facts)
```

Now, we see that we have quite a lot of columns, and there are also some missing data. In the next step, we'll do some data mangling to clean the data and keep only the columns that we're interested in.

Step 4: Cleaning data
---------------------

We live in a messy world, with messy data. One of the most important data science skills is the ability to clean-up a dataset. The `dplyr` package (which is part of the tidyverse, so we're already using it) has some excellent functions for managing data. Here we use two functions:

-   filter: for selecting rows
-   select: for selecting columns

We start by removing some rows from our data. Currently, the data contains many different areas, but for this example we'll just focus on the `states`. Without going into details, we can do this by selecting the rows that do not have a state\_abbreviation. In addition, we remove the broader area "United States".

``` r
facts_state = filter(facts, is.na(state_abbreviation) & !area_name == 'United States')
```

Next, we'll select the columns that we're interested in by entering the columns in the `select` function. The select function also has a nice syntax for renaming columns. If we say `population = Pop_2014_count`, we ask R to select the column named Pop\_2014\_count, but to rename it to `population` in our new data.

``` r
facts_state = select(facts_state, area_name, population=Pop_2014_count, pop_change=Pop_change_pct, 
                                  college=Pop_college_grad_pct, income=Income_per_capita)
```

Now we have a data frame called facts\_state that only has the cleaned up data we're interested in.

``` r
facts_state
```

Our data now has only 5 columns:

-   area\_name: The name of the area
-   population: The population of the area (2014 estimate)
-   pop\_change: Percent change in population (April 1, 2010 to July 1, 2014)
-   college: percentage of people age 25+ with Bachelor's degree or higher
-   income: per capita income (in US dollars)

Note that we still have all of our data assigned to the name `facts`. Since we can work with multiple data frames in R, there is no harm in making different subsets. This keeps data nice, simple and clean.

Step 5: Visualization
---------------------

One of the bit appeals of R is that it has amazing support for visualization. Here we use the celebrated `ggplot2` package, which is also part of the tidyverse.

The syntax for `ggplot2` looks a bit daunting at first, but it's really intuitive once you get the hang of it. If you are interested in making fancy and informative visualizations, learning ggplot2 is a great investment. You can make many types of visualizations, from line graphs and bar charts to coloured worldmaps.

We'll start with a simple scatterplot of the college education (x axis) and income (y axis). The first line of code specified that we use ggplot to make a plot based on the facts\_state date. In the second line of code we specify that we want to plot points, using the `college` column on the x-axis and the `income` column on the y-axis.

``` r
ggplot(data=facts_state) + 
  geom_point(mapping=aes(x=college, y=income))
```

This is ok, but we can do better. Next to the x and y axis, we have several other ways to visualize information. One is to use different points of different sizes. Here we add that we want to set the size of the points based on the `population` column in our data.

``` r
ggplot(data=facts_state) + 
  geom_point(mapping=aes(x=college, y=income, size=population))
```

Cool, but we can still add more (disclaimer: it's not actually good practice to put as much information as possible into one graph, but it is fun). Let's use the pop\_change column (percent change in population over time) to make a distinction between states with `Growing` and `Stable` population. First, we use the mutate function to add a new column to our data. The following code says:

-   we're mutating the facts\_state data
-   we add a column named `growth`
-   If pop\_change is larger than 1, the value for `growth` is "Growing", and otherwise its "Stable"

``` r
facts_state = mutate(facts_state, growth = ifelse(pop_change > 1, "Growing", "Stable"))
```

Now we can again use ggplot. We add that we want to let the colours of points differ for different values in the `growth` column.

``` r
ggplot(data=facts_state) + 
  geom_point(mapping=aes(x=college, y=income, size=population, colour=growth))
```

Step 6: Statistical analysis
----------------------------

R was originally designed by and for statisticians, so it comes as no surprise that it's very strong in the stats department. Most of the basic statistical tools such as the t-test, correlation and linear regression are by default included. But on top of that, there are many packages for all kinds of advanced statistical analyses, such as time-series analysis and multi-level modeling.

For this example we'll keep it simple, and only run a linear regression model using the `lm` (linear model) function. For statistical functions, R works with a `formula`, in which you specify what the dependent and independent variables are. For linear regression, the formula is `y ~ x1 + x2 + ...`, where y is the dependent variable, and x1, x2, etc. are independent variables (note that this bears resemblance to the actual regression formula). In the following line of code, we fit a linear regression model where the dependent variable is `income`, and the independent variables are `college`, `population` and `pop_change`.

``` r
m = lm(income ~ college + population + pop_change, data=facts_state)
```

Remember that before we said that you can assign anything in R to a name? Here we assigned the regression model to the name `m`. This is neat, because it gives us much flexibility in what to do with the results.

First, let's look at a summary of the model.

``` r
summary(m)
```

Here we have all the information that we would need to report a regression table in a study. However, this is just the dry, no-nonsense output. We can also use specialized packages for presenting the output of statistical models in more paper-ready tables. Here we will use the `sjPlot` package, that we first need to install (if you haven't done so before).

``` r
install.packages('sjPlot')
```

Now we open the package with `library()`, and use the `tab_model` function to create a regression table for the model assigned to `m`.

``` r
library(sjPlot)
tab_model(m)
```

Now we have a nice table with the regression coefficients (Estimates), p-values and R2 value. In addition, sjPlot calculated the confidence intervals (CI) for us.

If you see regression tables in papers, you often see multiple tables side-by-side. This is often done to show, from left to right, what happens if additional variables are added. Convenient packages like sjPlot make this really easy. We can just fit different models, and then plug them all into the `tab_model` function.

``` r
m1 = lm(income ~ college, data=facts_state)
m2 = lm(income ~ college + population, data=facts_state)
m3 = lm(income ~ college + population + pop_change, data=facts_state)
tab_model(m1,m2,m3)
```

As a final step, it is often good practise to use visualization to inspect how a model fits the data, and to check if any assumptions are violated. The default `plot` function in R can already show you the standard regression diagnostics. But the sjPlot package also has some nice visualization tools in the `plot_model` function. Here we visualize the fitted values of the model for the three independent variables.

``` r
plot_model(m, type='pred', show.data=T, grid = T)
```

Where to go from here
=====================

You've now only seen the very surface of what you can do with R, but hopefully you've developed a taste for more. While there is certainly an initial hurdle of getting into R, once you get past the basics it becomes much more fun and you'll learn new things much faster. Learning a programming language really is similar to learning a regular language. Once you know the basics, you can start learning by doing, and at that point progress becomes much easier and more rewarding.

So how do you get past that initial hurdle? First, you will need to find learning material that fits your learning style. Our own [github page](https://github.com/ccs-amsterdam/r-course-material) might be a good place to start. Here you can find more information on [Data and functions](https://github.com/ccs-amsterdam/r-course-material/blob/master/tutorials/R_basics_2_data_and_functions.md) in R, and the series of tutorials on Data mangling in the tidyverse is a good concise introduction for all your data mangling needs. Other than that, there are many other tutorials available online, many of which are free. There is also the excellent [R for data science](https://r4ds.had.co.nz/) book, which has a free online version.

Once you have learned the basics, it is mainly a matter of practice. To keep you motivated, we recommend picking up a project that interests you. This can be something that you need for work or studies, but also simply something fun.
