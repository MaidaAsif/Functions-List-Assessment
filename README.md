# Functions & Lists Assessment

## Overview
This repository contains two Python programs that demonstrate functions, string manipulation, lists, and loops through academic scenarios.

| File | Topics |
|------|--------|
| `result_card_generator.py` | Functions, parameters, return values, string methods |
| `class_marks_analyzer.py` | Lists, loops, list functions, custom functions |

## Task 1: Student Result Card Generator

Generates a formatted result card for one student.

**Input:** student name, roll number, and marks in five subjects (English, Math, Physics, Chemistry, Computer).

**Functions:**

| Function | Purpose |
|----------|---------|
| `get_valid_marks(subject)` | Asks for marks until a value from 0 to 100 is entered |
| `calculate_percentage(total, max_total)` | Returns the percentage obtained |
| `get_grade(percentage)` | Returns the letter grade for a percentage |
| `format_name(name)` | Cleans the name with `.strip()` and `.title()` |

**Grading criteria:**

| Percentage | Grade |
|------------|-------|
| 90 and above | A+ |
| 80-89 | A |
| 70-79 | B |
| 60-69 | C |
| 50-59 | D |
| Below 50 | Fail |

**Special rule:** if any subject mark is below 40, the final result is Fail regardless of the overall percentage.

**Output:** a result card showing name, roll number, all subject marks, total, percentage (2 decimal places), grade, and Pass/Fail status.

## Task 2: Class Marks Analyzer

Analyzes the performance of an entire class using two parallel lists, `student_names` and `student_marks`.

**Features:**
- Class average
- Highest and lowest marks, with the student(s) who achieved them
- Count of passing (50 or above) and failing (below 50) students
- Students who scored above the class average
- Marks sorted from highest to lowest

**Custom functions:**

| Function | Purpose |
|----------|---------|
| `get_valid_mark(name)` | Asks for marks until a value from 0 to 100 is entered |
| `students_with_mark(names, marks, target)` | Returns the names of students who scored the target mark |

## Python Concepts Used
- Functions with parameters and return values
- String methods: `.strip()`, `.title()`, `.isdigit()`
- f-strings with alignment and number formatting
- Lists: `append()`, `len()`, `sum()`, `max()`, `min()`, `sorted()`
- List comprehensions and `zip()`
- `for` and `while` loops
- Conditional statements: `if`, `elif`, `else`
- `try` / `except` for invalid input

## How to Run

**Requirements:** Python 3.8 or later.

```bash
git clone https://github.com/MaidaAsif/Functions-List-Assessment.git
cd Functions-List-Assessment
python result_card_generator.py
python class_marks_analyzer.py
```

Use `python3` or `py` if `python` is not recognized.

## Sample Execution

### Task 1: Result card (passing student)

```
Student name: ayesha khan
Roll number: 101
Marks in English (0-100): 95
Marks in Math (0-100): 88
Marks in Physics (0-100): 92
Marks in Chemistry (0-100): 85
Marks in Computer (0-100): 90

================================
          RESULT CARD           
================================
Name: Ayesha Khan
Roll No: 101
--------------------------------
English               95/100
Math                  88/100
Physics               92/100
Chemistry             85/100
Computer              90/100
--------------------------------
Total:      450/500
Percentage: 90.00%
Grade:      A+
Status:     Pass
================================
```

### Task 1: A subject below 40 forces Fail

With marks `95, 90, 92, 35, 90`, the percentage is 80.40%, which would normally be an A. Because one subject is below 40, the result is:

```
Total:      402/500
Percentage: 80.40%
Grade:      Fail
Status:     Fail
```

### Task 2: Class analysis

```
Number of students: 4

Name of student 1: ali
Marks for Ali (0-100): 80

Name of student 2: sara
Marks for Sara (0-100): 45

Name of student 3: ahmed
Marks for Ahmed (0-100): 80

Name of student 4: zoya
Marks for Zoya (0-100): 60

===== CLASS ANALYSIS =====
Average: 66.25
Highest: 80 - Ali, Ahmed
Lowest:  45 - Sara
Passed: 3 | Failed: 1

Above average:
  Ali: 80
  Ahmed: 80

Ranking (highest to lowest):
  1. Ali: 80
  2. Ahmed: 80
  3. Zoya: 60
  4. Sara: 45
```

## Input Validation
- Marks must be numbers between 0 and 100
- Roll number must contain digits only (`.isdigit()`)
- Student name cannot be empty
- Number of students must be a positive whole number
- Invalid input prompts the user to try again

## Project Structure

```
Functions-List-Assessment/
├── result_card_generator.py
├── class_marks_analyzer.py
└── README.md
```

## Author
Maida Asif
