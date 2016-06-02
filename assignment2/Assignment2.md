# Assignment 2: Exploratory Data Analysis

## Ron Cordell

## W209 - Section 3</p>

## Florida 2000 Elections

Using [county data from the 2000 Presidential elections in Florida](https://www.dropbox.com/s/1arzn0nup8jua6t/fl2000clean.csv?dl=0) , examine the raw data and formulate 3 hypotheses. For each of the 67 Florida counties, the data include the type of voting machine used, the number of columns in the presidential ballot, the undervote, the overvote, and the official certified votes for each of the twelve presidential candidates. Of particular interest are the Buchanan vote in Palm Beach county, and the overvote as a function of voting machine type and number of columns. Data is from the CMU Statistical Data Repository.

## Hypotheses:

1. Votomatic voting machines have a higher overvote as a fraction of the total vote than other voting technologies.
2. The 2 column vote has a higher overvote as a fraction of the total vote than the 1 column vote.
3. The Buchanan vote in Palm Beach county is significantly larger than it should be.

### Definitions:

- **Overvote**: occurs when a voter chooses more than the allowed number of candidates for an elected position. For example, if only one choice is allowed but the voter chose two. In the case of overvotes the vote is cancelled. 

- **Undervote**: occurs when a voter chooses less than the required number of candidates for an elected position. It is within the voter's right to do so; for example, when choosing not to vote for any candidate for that position. The vote is still valid.

### Hypothesis 1: Votomatic voting machines have a higher overvote as a fraction of the total vote than other technologies.

![Overvotes By Technology](https://raw.githubusercontent.com/rocket-ron/MIDS-W209/master/assignment2/OvervoteByTechByColumn.png "Overvotes By Technology and Columns")

**What's informative about this view:** This view shows the number of overvotes by columns and by technology type for the Florida 2000 Presidential election. This view shows that the highest counts of overvotes occur with the [Votomatic](http://americanhistory.si.edu/vote/resources_votomatic.html) voting machines.

**What could be improved about this view:** This view uses only the raw counts of overvotes instead of the proportion of overvotes of the total vote count. Doing so would account for populations of counties and provide a better sense for *error rate* as opposed to *error count*.

![Overvote Rate By Technology and Column](https://raw.githubusercontent.com/rocket-ron/MIDS-W209/master/assignment2/OvervoteRate.png)

**What's informative about this view:** This view shows the overvotes as a percentage of the total votes. Clearly the technology with the highest error rate regardless of number of columns is the [Datavote](http://americanhistory.si.edu/vote/resources_datavote.html). While all technologies show an increase in overvote rates from 1 column format to 2 column format, only the Datavote is high in both categories.

**What could be improved about this view:** There is more going on here than just voting technology. The 2 column format is more prone to overvotes than the single column format for most technology types except the Datavote. We can bring more into the picture here on what counties and what candidates were involved in where the Datavote technology was used.

Third View - Image Here

### Hypothesis 2: Two column format has a higher overvote rate than single column format




### Hypothesis 3: The Buchanan vote count in Palm Beach county is larger than it should be.

![Buchanan Relative Votes](https://raw.githubusercontent.com/rocket-ron/MIDS-W209/master/assignment2/BuchananRedBlue.png)

**What's informative about this view:** This graphic shows the relationships between the Republican, Democrat, and Buchanan votes by county. In this view the traditional red/blue colors indicated which party carried the county and the size of the circle is the proportion of Buchanan votes to total votes. Pat Buchanan was an [extremely conservative candidate](https://en.wikipedia.org/wiki/Pat_Buchanan_presidential_campaign,_2000) so if we also equate the Republican party with conservatism we would expect to see a corresponding increase in the Buchanan vote for those counties that voted Republican. We do see this trend in general in the graphic - the red circles tend to be larger than the blue ones - but this is not always the case. Palm Beach county is the highest Buchanan vote proportion and stands out from the other blue circles with the highest proportion of Buchanan votes.

Palm Beach County is also the county at the center of the controversy of the "hanging chad" of the 2000 election. Palm Beach county used a 2 column format and Votomatic card punch machine. In the 2 column format Bush's name would be opposite Buchanan's name and have adjacent chads. One possible explanation is that the Buchanan votes were actually meant to be Bush votes.
