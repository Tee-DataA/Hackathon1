# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
* Describe your dataset. Choose a dataset of reasonable size to avoid exceeding the repository's maximum size of 100Gb.

The dataset I've chosen is the car Analysis dataset. This shows the sales of cars in the US market. A new 

A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts.

They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. The company wants to know:

Which variables are significant in predicting the price of a car
How well those variables describe the price of a car
Based on various market surveys, the consulting firm has gathered a large data set of different types of cars across the America market. 

## Business Requirements

A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts.

They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. The company wants to know:

Which variables are significant in predicting the price of a car
How well those variables describe the price of a car
Based on various market surveys, the consulting firm has gathered a large data set of different types of cars across the America market. 

We are required to model the price of cars with the available independent variables. It will be used by the management to understand how exactly the prices vary with the independent variables. They can accordingly manipulate the design of the cars, the business strategy etc. to meet certain price levels. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

## Hypothesis and how to validate?
I believe there are many factors that affect the price of a car. Some are factors can be directly affected, like the size of an engine, or the number of doors, and other factors are fully/partially dependant like the length, width, power. From my vested interest in cars, not all of these factors are contributary to the price. Factors such as weight are not a selling point, and the price is listed for takes into consideration manufacturing and logistical costs among others.

The main factors I believe will affect the price are the brand, the horsepower, enginesize and economy. I will validate this by checking the correlation between the variables and price


## Project Plan
* Outline the high-level steps taken for the analysis.
Relevant test were carried to see which of the variables are significant in affecting the price

* How was the data managed throughout the collection, processing, analysis and interpretation steps?
Data was collected from kaggle. One of the first checks was to see if there was any missing data of which there was none. It was processed to make the distribution more closer to a normal distribution. Interpretation was done using my background knowledge in statistics
* Why did you choose the research methodologies you used?
Having studied statistics I knew the relevant methodologies to use. Since price was the main Variable I was interested, I had to check how and if the other variables contributed to it. 

## The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations
Business requirements were to see what factors affected the price the most, the least or even at all. This information is extremely important as the right decisions need to be made before it reaches the manufacturing stage. Making changes after that is very costly

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
Correlation analysis - doesn't always give the whole picture. Dependant on the size of the dataset
ANOVA test for categorical variables - assumes the variance of price is equal accross all the variables. It is sensitive to outliers

* How did you structure the data analysis techniques. Justify your response.
The aim was to remove as many features as I could that did not contribute enough as a factor to the price. I started with the correlation check to remove the features that had a weak correlation. This doesn't work on categorical variables so I used an ANOVA test on those and kept the variables with a p-value<0.05 
* Did the data limit you, and did you use an alternative approach to meet these challenges?
The data did limit me as the sample was too small. I couldn't perform an analysis to check if brand name affects the price which I believe it does. The sample size was also too small small to draw any meaningful information for features like aspiration which only had 19 cars with a turbo.

* How did you use generative AI tools to help with ideation, design thinking and code optimisation?
Gemini was used along the way to help me write the code, solve syntax problems, and brainstorm analysis technique.

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
Data was on a public server available to all so there was no issue with privacy. As mentioned before, sample size was very small and range of cars and classes was not big enough to make any conclusions based on those features
* How did you overcome any legal or societal issues?
I didn't not face any


## Unfixed Bugs
There are no unfixed bugs in my code
* Did you recognise gaps in your knowledge, and how did you address them?
Gaps in my knowledge were filled by using resources such as the LMS for revision, and the internet
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.
I had asked Vasi to have a quick glance to see if I was on the right track, which gave me confidence that I was doing the task correctly

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 
It was my first project so it was very stressful. I wasn't not sure how to start and what analysis I needed to perform.




## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
sns.set_style('whitegrid')
from sklearn.pipeline import Pipeline
from feature_engine import transformation as vt
from feature_engine.outliers import Winsorizer
import plotly.express as px
from scipy.stats import f_oneway
from feature_engine.selection import SmartCorrelatedSelection
from feature_engine.encoding import OrdinalEncoder
from feature_engine.encoding import OneHotEncoder

## Credits 

https://www.kaggle.com/datasets/hellbuoy/car-price-prediction 


### Content 

- The text for the Home page was taken from Wikipedia Article A
- Instructions on how to implement form validation on the Sign-Up page was taken from [Specific YouTube Tutorial](https://www.youtube.com/)
- The icons in the footer were taken from [Font Awesome](https://fontawesome.com/)




## Acknowledgements (optional)

Vasi and Neil for the support
