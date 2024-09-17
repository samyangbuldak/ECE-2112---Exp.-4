# ECE 2112 - Programming Assignment 4
# Experiment 4 - Data Wrangling and Data Visualization
## Getting Started
I. Intended Learning Outcomes
1. To identify the codes and functions needed in cleaning and visualizing data
2. To be able to apply and use the different codes and functions in creating a Python program that will be used in data wrangling and data visualization

The following tools were used in the completion of this experiment:
- Anaconda Navigator 2.6.0
- Jupyter Notebook 7.0.8

### Problem 1
Using data wrangling and data visualization technique with storytelling, analyze the data and present different (i) data frames; and (ii) visuals using the dataset given.

a. To identify students in the **Instrumentation track** from **Luzon** with an **Electronics score greater than 70**, I used the Pandas library to filter the dataset. Specifically, I applied the conditions using the _`df[(df['Electronics'] > 70) & (df['Track'] == 'Instrumentation') & (df['Hometown'] == 'Luzon')]`_ statement. This filters the DataFrame to include only students who meet the specified criteria. I then selected the relevant columns **Name**, **GEAS**, and **Electronics** using _`[['Name', 'GEAS', 'Electronics']]`_ to get a concise view of the filtered students. This method provides an effective way to focus on students excelling in Electronics within the Instrumentation track, while narrowing the data to those from Luzon.

b. To create the **Mindy** DataFrame, which filters female students from **Mindanao** with an **average score of 55 or higher**, I first calculated the average score across four subjects: **Math**, **Electronics**, **GEAS**, and **Communication**. I used the Pandas _`mean`_ function with the statement _`df['Average'] = df[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)`_ to compute the average for each student. Next, I applied filtering conditions to select rows where the **Hometown** is "Mindanao", **Gender** is "Female", and the **Average score** is greater than or equal to 55. I then limited the output to the **Name**, **Track**, **Electronics**, and **Average** columns. This approach allowed me to isolate the relevant students who meet all the criteria, providing a clear view of their performance.

### Problem 2
Create a visualization that shows how the different features contributes to average grade. Does chosen track in college, gender, or hometown contributes to a higher average score?

To visualize how different features contribute to the **average score**, I first calculated the **average grade** for each student by taking the mean of the **Math**, **Electronics**, **GEAS**, and **Communication** columns using the Pandas _`mean`_ function: _`df['Average'] = df[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)`_. 

Next, I created three separate bar plots using Seaborn's `barplot` function to compare the **average score** across different categories:
- For the **Track** visualization, I plotted the average score grouped by the **Track** feature, which allows me to see how students in different tracks perform on average.
- For the **Gender** visualization, I plotted the average score by **Gender**, helping to identify if there is a difference in performance between male and female students.
- Lastly, for the **Hometown** visualization, I compared the average score by **Hometown** to examine whether students from different regions perform differently.

These visualizations provide insights into how a student's track, gender, and hometown may influence their overall academic performance.

# Author
Samantha Louise J. Samoy

2ECE-C

