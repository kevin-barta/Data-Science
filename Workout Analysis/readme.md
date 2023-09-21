# Workout Analysis Data Science Project

Welcome to the Workout Analysis data science project! This project is all about gaining insights from my workout data, particularly related to 1RM (One-Repetition Maximum) values, and explore how different exercises and workout sessions affect strength and performance.

## Table of Contents

- [Introduction](#introduction)
- [Dependencies](#dependencies)
- [Dataset](#dataset)
- [Analysis](#analysis)
- [Visualization](#visualization)
- [Results](#results)
  
## Introduction

In strength training, the One Rep Max (1RM) is used to determine the maximum amount of weight that a person can possibly lift for one repetition of a given exercise. The project processes a dataset containing a history of workouts, calculates 1RMs using various methods, and provides visualizations of the progress over time.

## Dependencies

The following Python libraries are used in the project:

- numpy
- pandas
- matplotlib
- seaborn
- scipy
- tqdm

Make sure to install them using pip:
```bash
pip install numpy pandas matplotlib seaborn scipy tqdm
```

## Dataset
The dataset (`strong.csv`) used in this project is sourced from a workout mobile application called Strong, and includes data such as:
- Date
- Workout Name
- Exercise Name
- Set Order
- Weight used
- Reps performed
- and more...

## Analysis

1. **Data Cleansing**:
   - The first two sets, which are considered warm-up sets, are removed.
   - Any "working-sets" after 5 are also removed to maintain dataset consistency.
   - The 'Set Order' column is adjusted accordingly.

2. **1RM Calculations**:
   - For each exercise and each set, 1RMs are calculated using various approximation methods like Brzycki, Epley, Lombardi, and O’Conner. An average 1RM across these methods is also derived to obtain a more robust estimate of an 1RM for each exercise and workout session.

3. **1RM Aggregation**:
   - 1RMs are aggregated for each workout session.

## Visualization

Several plots are generated during the analysis:

1. **Per Exercise Visualization**: Shows the 1RM averages for each set of each exercise over time.
2. **Aggregate Visualization**: Displays the 1RM averages across all sets of an exercise.
3. **Total Visualization**: Highlights the average 1RM across all exercises.
4. **Log and Diff Visualization**: Provides insight into the logarithmic difference and direct difference in 1RM averages across exercises.

## Results

The results give insight into the progression of my strength training routine. Through the visualizations, I can gauge the effectiveness of my training over time and identify exercises that have seen the most progression or stagnation. Which I am using to enhance my training strategies and achieve my fitness goals.
