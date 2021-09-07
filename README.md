# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Catherine Ang, DSIF-1

### Problem Statement
**We Believe In Education Pte Ltd** (“company”) is a private tuition centre based in Singapore, and is looking to expand its range of private education services into the United States. Which **tuition programme (either SAT or ACT)** should the company offer as part of its pilot programme? And, which **states are the most promising for the company to advertise its services to** (inclusive of awarding scholarships to deserving students)?


### Executive Summary


INTRODUCTION

To conduct an analysis on ACT and SAT, datasets from both ACT and SAT were used. Each dataset contains state-by-state mean test scores and participation rates, from 2017, 2018 and 2019. By analysing the test scores and participation rates between ACT and SAT, this allows for a comparison to measure the performance of ACT and SAT over the years. Each year, ACT and SAT would put up their test scores and participation information available for members of the public to refer to.


METHODOLOGY

A data science workflow was introduced to conduct this analysis. Firstly, the problem statement was defined — We Believe In Education Pte Ltd is looking to expand its range of private education services into the United States, and thus seeks recommendations on whether it should offer ACT or SAT tuition programme, and which states should it channel its advertising efforts to. Next, the appropriate datasets were imported to a Pandas DataFrame, which included ACT and SAT test scores and participation rates from 2017-2019. Thereafter, data cleaning was conducted to ensure that any inconsistencies and missing values were fixed, and all datatypes were accurate. All cleaned datasets were then merged into a singular DataFrame. An exploratory data analysis was conducted to determine the parameters about the population being measured. All statistical findings were utilised to then perform data visualisation, which included the use of heat map, histogram, subplots, scatterplots and boxplots. Concurrently, descriptive and inferential statistical analysis was conducted to identify trends that appeared in the data. External research about ACT and SAT were also conducted, to support observations made. Eventually, recommendations for **We Believe in Education Pte Ltd** were compliled.


FINDINGS

When analysing the datasets, various insights about the ACT and SAT test scores and participation rates were obtained. The following consists of the most significant findings:
* ACT Participation Rates vs SAT Participation Rates: There was a strong negative correlation between both test, i.e. when participation in ACT is high (i.e. >70%), participation in SAT is low (i.e. <30%); the reverse holds true.
* ACT Compositve Scores vs Participation Rates & SAT Total Scores vs Participation Rates: Across all 3 years, there was a strong negative correlation between test scores and participation rates, i.e. when participation in SAT is low (i.e. <20%), the total scores remain on the higher end at around 1200 to 1300, as seen in 2019. This indicates a selection bias that may exist. 


---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**state**|*object*|ACT 2017-2019, SAT 2017-2019|State in United States|
|**act_participation_2017**|*float*|ACT 2017|Statewide ACT Participation Rate, 2017| 
|**act_english_2017**|*float*|ACT 2017|State mean score, ACT English (1-36), 2017| 
|**act_math_2017**|*float*|ACT 2017|State mean score, ACT Mean (1-36), 2017| 
|**act_reading_2017**|*float*|ACT 2017|State mean score, ACT Reading (1-36), 2017| 
|**act_science_2017**|*float*|ACT 2017|State mean score, ACT Science (1-36), 2017| 
|**act_composite_2017**|*float*|ACT 2017|State mean ACT Composite Score (1-36), 2017| 
|**sat_participation_2017**|*float*|SAT 2017|Statewide SAT Participation Rate, 2017| 
|**sat_reading_writing_2017**|*integer*|SAT 2017|State mean score, SAT Evidence-Based Reading and Writing (200-800), 2017| 
|**sat_math_2017**|*integer*|SAT 2017|State mean score, SAT Math (200-800), 2017| 
|**sat_total_2017**|*integer*|SAT 2017|State mean total SAT score (400-1600), 2017| 
|**act_participation_2018**|*float*|ACT 2018|Statewide ACT Participation Rate, 2018| 
|**act_composite_2018**|*float*|ACT 2018|State mean ACT Composite Score (1-36), 2018| 
|**sat_participation_2018**|*float*|SAT 2018|Statewide SAT Participation Rate, 2018| 
|**sat_reading_writing_2018**|*integer*|SAT 2018|State mean score, SAT Evidence-Based Reading and Writing (200-800), 2018| 
|**sat_math_2018**|*integer*|SAT 2018|State mean score, SAT Math (200-800), 2018| 
|**sat_total_2018**|*integer*|SAT 2018|State mean total SAT score (400-1600), 2018| 
|**act_participation_2019**|*float*|ACT 2019|Statewide ACT Participation Rate, 2019| 
|**act_composite_2019**|*float*|ACT 2019|State mean ACT Composite Score (1-36), 2019| 
|**sat_participation_2019**|*float*|SAT 2019|Statewide SAT Participation Rate, 2019| 
|**sat_reading_writing_2019**|*integer*|SAT 2019|State mean score, SAT Evidence-Based Reading and Writing (200-800), 2019| 
|**sat_math_2019**|*integer*|SAT 2019|State mean score, SAT Math (200-800), 2019| 
|**sat_total_2019**|*integer*|SAT 2019|State mean total SAT score (400-1600), 2019| 
|**act_participation_change_2017_2018**|*float*|ACT 2017 & 2018|Change in ACT Participation Rate, 2017-2018| 
|**act_participation_change_2018_2019**|*float*|ACT 2018 & 2019|Change in ACT Participation Rate, 2018-2019| 
|**sat_participation_change_2017_2018**|*float*|SAT 2017 & 2018|Change in SAT Participation Rate, 2017-2018| 
|**sat_participation_change_2018_2019**|*float*|SAT 2018 & 2019|Change in SAT Participation Rate, 2018-2019|


---

### External Research

While more and more colleges are adopting test-optional admissions, which mean that ACT or SAT is not mandatory as an admission criteria, the demand to sign up for either ACT or SAT remains high. Even with the COVID-19 pandemic resulting in mass cancellations of SAT/ACT exams in 2020 due to the lack of appropriate examination venues, 1.1 million students from the class of 2020 took the SAT on a school day, up from almost 1 million in the class of 2019.(1) 

Additionally, with academic research highlighting the value of using SAT/ACT test scores as part of the admissions process, where they are used to compare studens from various schools, districts and states, all on the same playing field, they remain highly predictive of the students' success in college.(2)

As the university admissions process stabilises post-pandemic in the long run, the College Board in SAT has stated that it will support the transition for all students to have the opportunity to participate in the tests and submit their scores.(3) Therefore, it is highly likely that there will be a continuous demand for SAT/ACT, and therefore the need for private tuition in a bid to boost up scores.

Citations:
(1) [Source](https://www.theatlantic.com/ideas/archive/2020/09/even-coronavirus-cant-kill-sat-and-act/616360/)
(2) [Source](https://edition.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)
(3) [Source](https://reports.collegeboard.org/sat-suite-program-results)


---

### Conclusion and Recommendations

By examining the trend in the median participation rates for ACT and SAT from 2017 to 2019, it is evident that participation rates for ACT is declining (from 69% in 2017 to 54% in 2019), while participation rates for SAT is increasing (from 38% in 2017 to 54% in 2019) as more states make it mandatory for students to take SAT. These states include Colorado, Illinois, Rhode Island and West Virginia.
* With that, **We Believe In Education Pte Ltd** should focus on providing tuition programme in SAT, as it is likely that more students will take up SAT, thus increasing the demand for SAT tuition to improve scores. 

As for the states which are promising for the company to advertise its services to, as well as to award scholarships to deserving students, they can be segmented as follows: 
* **Target Market #1**: States with highest SAT participation rates, but lowest SAT scores 
* States: **District of Columbia**, **Michigan**, **Connecticut**, **Delaware**, New Hampshire, **Maine**, **Idaho**, Rhode island *(note that states bolded have lowest SAT scores)*
* Reason: WIth SAT being mandated in these states, whilst the states have lower mean scores, there is a potential for stable and high demand for private tuition, as students aim to increase SAT scores and their chances to enrol in prestigious universities.
    
* **Target Market #2**: States with lowest SAT participation rates, but highest SAT scores 
* States: **North Dakota**, Mississippi, **Iowa**, Utah, South Dakota, **Nebraska**, **Wisconsin**, **Minnesota**, Wyoming *(note that states bolded have highest SAT scores)*
* Reason: While SAT is not mandatory in these states, there is a likelihood that many eligible students have yet to participate, due to the lack of awareness about SAT. Hence, there may be a potentially large market that's still untapped, eventually as students become aware of the benefits of SAT. In addition, these states tend to have higher mean total scores for SAT, likely formed by a small of high achieving students. Thus, scholarships can be channeled to these states as a mode for publicity, encouraging even more high achieving and deserving students (who may not have taken the test due to various reasons) to participate in SAT.

---

### Datasets

The sources of datasets used in this analysis: 
* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))

