Major Leagues
==============================

Soccer scores

Author: Ruturaj Kiran Vaidya

Project Organization
------------

    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting

--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

### Before Getting Stated

If you are only interested in looking at the notebook then go to (There are notebook rendering problems in github ecosystem):

https://nbviewer.jupyter.org/github/Ruturaj4/major_leagues/blob/master/notebooks/1.0-rkv-major-leagues.ipynb

All the graphs are plotted using `matplotlib`.

### Aim
<ul>
<li>Pick datasets from various leagues like NFL, MLB, NBA and Soccer</li>
<li>Obtain additional value using exploratory data analysis, by formulating ideas using feature engineering</li>
<li>Using regression algorithms to determine scores of each team</li>
</ul>

### Dataset used

I used soccer dataset.

Dataset: https://github.com/fivethirtyeight/data/tree/master/soccer-spi

Specific Dataset Link: https://projects.fivethirtyeight.com/soccer-api/club/spi_matches.csv

### Discussion

First, I imported the soccer dataset, as soccer interests me the most. I was unaware of what some of the features mean, particularly Xg and NsXg. With some research, I discovered that Xg belongs to "Expected goals" and NsXg belongs to "Non shot Xg". It was interesting to find this information. Second, for feature engineering, I split "date" into years, months and days. Next, for training, I used linear regression model from sklearn module. The actual and predicted results for score1 and score2 (scores for each team) are as follows:

![alt text](/reports/figures/score1.png)
![alt text](/reports/figures/score2.png)

I think that the prediction algorithm is quite nice. Lastly, I also calculated "Mean Absolute Error", "Mean Squared Error" and "Root Mean Squared Error" for the scores for each team. These results can be seen in the Jupyter Notebook.

My reason for splitting date:

I think that each team may change their form based on year, month or even season. I belive that, in future a column or feature which defines season, may be added, as that would make a lot more sense.

Plot and error calculation reference: https://towardsdatascience.com/a-beginners-guide-to-linear-regression-in-python-with-scikit-learn-83a8f7ae2b4f.

### License

<b>MIT</b>

