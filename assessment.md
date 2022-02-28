<!-- #region -->
#### Data Science Project Self Assessment

## Criterion A: Knowing, understanding, and computational thinking

My project achieves a [ ] for this criterion because...

1. explanations of why a statistic or plot answers a question:

The scatter graph was able to answer the first sub question as it showed how the grade level impacted the average time spent on social media.
The 3 different pie chart shows the percentage of grade level who uses Instagram, Youtube and discord

2. a plot generated to answer a question:
plt.pie(Discord_grade,            
        labels = Grades,   
        autopct='%1.1f%%') 

3. use of a feature from Pandas or Matplotlib that we didn’t cover in class:(trend line)

y = pd.to_numeric(Time_SM_df["time_on_apps_per_week_self_report_social"])
z = np.polyfit(Time_SM_df["grade"], y, 1)
p = np.poly1d(z)
plt.plot(Time_SM_df["grade"],p(Time_SM_df["grade"]),"r--")

4. use of a data structure (i.e. list, dict, dataframe) which is appropriate for what you want to store:
Time_SM_df

5. code looping through a data structure in order to access/change elements inside the data structure:
Instagram_g6 = df.loc[(df["most_used_sm_platforms"]== "Instagram")].loc[(df["grade"]== 6)]["grade"].count()

6. a function that transforms data into a more useful format (i.e. filtering):
df[["time_on_apps_per_week_self_report_social","grade"]]

7. a pair of functions where one function generates an output which is then used as the input of the second function:
Time_SM_df = df[["time_on_apps_per_week_self_report_social","grade"]] Then I used the data in Time_SM_df.loc[Time_SM_df["time_on_apps_per_week_self_report_social"]=="< 10m","time_on_apps_per_week_self_report_social"] =10


> **💬 Teacher Comments**
> * *Analyzing and Visualizing data* - You've done a wonderful job choosing visualizations for your data. The trend
>   line is very helpful for understanding what's happening with your scatter plot.
> * *Data Structures* - Great job using appropriate data structures and manipulating your data with a loop.
> * *Functions* - Amazing job using functions outside of what we covered in class to add a trendline to your data.
>   You have an opportunity to use a function when making your pie charts. Anytime you repeat similar
>   code over and over again, you probably want to use a loop, a function, or both. For example, you could make a
>   function to produce a list of grade level counts of most used social media given a grade level and a media
>   platform.
>
> 8/8

## Criterion B: Planning and development

My project achieves a [ ] for this criterion because...

1. A thorough design document.:
Link to Google doc. (https://docs.google.com/document/d/1Ug5wNqE91CnmQojA3DOVySgfkooWfRbfE74QIxDalZU/edit)

2. Updates to your project plan to account for challenges during development
Not sure how to use the data to create a scatter graph → changes the value of average time spent on social media to the range’s max (check back part of doc to see more)

3. At least 5 regular and descriptive git commits on your project
I have 7 git commits as I am writing this

4. A description of a GitHub issue / bug you encountered, as well as an explanation of how you fixed it (you may include links that you used, such as StackOverflow).
I wasn't sure how to create a trendline as we haven't learnt about it, therfore I used the StackOverflow to try and see how I could create a trendline.

5. Comments for each of the modules and functions in your project:

eg: # Code to create the scatter graph along with the trend line

> **💬 Teacher Comments**
> * *Planning* - Great job planning your project! You've got a clear outline of how you will answer each of your
>   subquestions.
> * *Development* - Good work iteratively developing your project. It's clear from your git commits that you started
>   with a more basic analysis and then built it up. Additionally, good work documenting what your code does with
>   inline comments and also documenting the issues you faced over the course of your project's development.
>
> 8/8

## Criterion C: Evaluation

My project achieves a [ ] for this criterion because...
1. handling of bad data by cleaning the data beyond what’s provided (removing the data that is blank or determining that an outlier is actually bad data):
.dropna() (used to make clear data which was blank)

2. Combinations or reorganizations of data that explore new relationships
I used the data which I reorganized in my graphs to show the different relationships

3. Justifications of why particular data was/wasn’t selected and how that choice impacted the results
Some of the data which wasn't used as it was effecting the function of the trendline therfore It was removed, this choice may have effected the results as maybe the person had an answer but forgot to input the answer impacting the average as the response was removed.
4. a test to make sure that your code is doing what it’s supposed to (filtering a dataframe to check for values, producing counts to make sure data was filtered, etc.):

i = df.loc[(df["most_used_sm_platforms"]== "Instagram")].loc[(df["grade"]== 6)]["grade"].count()
print(i)
Then I used the code bellow to check
df.loc[(df["most_used_sm_platforms"]== "Instagram")].loc[(df["grade"]== 6)]

> **💬 Teacher Comments**
> * *Choosing Data* - You've done a great job of selecting data to help answer your questions. To do so, you've had
>   to think about the relationships across different columns and also further refine your data so you can perform
>   the kind of analysis you want to perform
> * *Analytical Choices* - Good work testing your code to make sure that it works as expected. Additionally, good
>   work describing your reasoning for removing the blank data from your dataframe.
>
> 7/8

## Criterion D: Reflecting on the impacts of technology on society

My project achieves a [ ] for this criterion because...
1. identification of an audience for the project
Planning Document (part 4)
2. developments of your analysis made with the audience in mind
3. responses to your research communication that show that your audience cares about the question
I think that parents would be most interested in my finding as many parents are often worried about their child using too much of their digital devices (planning document)
4. discussion of the underlying benefits of your quantitative analysis
project (5.3)


5. discussion of the limitations of your quantitative analysis
Project (5.3)
6. possible approaches to addressing the limitations
Project (5.3)
7. identification of biases present in your analysis
project (5.2)
8. an outline of future steps for research in your area
Project (5.3)

> **💬 Teacher Comments**
> * *Communication* - Great work communicating your research in a way that was compatible with your chosen audience!
> * *Impact* - You include a background source about age and social media usage in your planning document, but you 
>   don't include it in your project. Great job considering how your results differ from your own experience. I 
>   think you could still consider how your research should impact the audience you identified beyond just finding
>   it interesting.
> * *Limitations and Potential* - Great work thinking about the limitations of your data and how it may not be
>    representative given the limited number of responses from older students.
>
> 6/8

<!-- #endregion -->

```python

```

```python

```
