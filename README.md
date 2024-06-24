# Habit Tracker

This is a habit tracker application that allows you to manage and track your habits through a command-line interface. 
The application uses the questionary library to provide an interactive experience for users and the rich library for creating an overview table.

## Features

- **Add a New Habit:** Create a new habit with a specified task and periodicity (daily or weekly).
- **Complete a Habit:** Mark a habit as completed for a specific date.
- **Delete a Habit:** Remove a habit along with all its associated data.
- **Delete a Completion Date:** Remove a specific completion date for a habit.
- **Show an Overview:** Display an overview of your currently tracked habits with sorting options.
- **Exit:** Exit the application.

## Setup

Download 'HabitTracker' as ZIP and open folder within terminal.

## Prerequisites

Ensure you have installed the requirements. Those include the following:

- Python 3.6+
- **'questionary'** library
- **'pytest'** and **'freezegun'** for running tests
- **'questionary'** for creating and displaying the overview table

You can install the required libraries using pip:

```console
pip install -r requirements.txt
```

## Usage

Run the application using Python:

```console
python main.py
```

or

```console

python3 main.py
```

Upon running the application, you will be prompted to enter your name. After that, you will enter the main loop where you can select from the available tasks.

## Code Overview

The main script performs the following steps:

1. **Initialize the Database:** Ensures the necessary table exists by calling **'create_table()'**.
2. **Greet the User:** Prompts the user for their name.
3. **Main Loop:** Continuously prompts the user to choose a task until they choose to exit.

## Task Choices

- **Add a New Habit:**
  - Prompts for the habit name, task specification, and periodicity.
  - Checks if the habit already exists before adding it to the tracker.
 
- **Complete a Habit:**
  - Lists all current habits and allows the user to select one.
  - Prompts for the completion date and marks the habit as completed for that date.
 
- **Delete a Habit:**
  - Lists all current habits and allows the user to select one.
  - Deletes the selected habit and all its data.
 
- **Delete a Completion Date:**
  - Lists all current habits and allows the user to select one.
  - Prompts for the specific completion date to delete.
 
- **Show an Overview:**
  - Prompts for the periodicity of habits to display (all, daily, weekly).
  - Prompts for the column to sort the table by (Current Streak, Longest Streak).
  - Displays the overview table and waits for the user to finish analyzing their habits.
 
- **Exit:**
  - Exits the application with a farewell message.
 
## Functionality

The following functions are imported from the **'functionality'** module:

- **'add_habit(habit_name, habit_task_specification, habit_periodicity)'**: Adds a new habit to the tracker.
- **'create_overview_table(periodicity_choice, column_sorted_by)'**: Creates and displays an overview table of tracked habits.
- **'create_last_completion_dates_list(habit_name)'**: Creates a list of the last completion dates for a specific habit.
- **'create_list_of_available_completion_dates(habit_name)'**: Creates a list of available completion dates for a specific habit.

The following functions are imported from the **'database'** module:

- **'create_table()'**: Creates the necessary table in the database if it doesn't exist.
- **'get_all_habit_names()'**: Retrieves the names of all currently tracked habits.
- **'create_last_completion_dates_list(habit_name)complete_habit(habit_name, date_completed)'**: Marks a habit as completed for a specific date.
- **'delete_habit_data(habit_name)'**: Deletes a habit and all its associated data.
- **'delete_habit_completion_date(habit_name, habit_completion_date)'**: Deletes a specific completion date for a habit.

