# Task 7 — Text Cleaning

This task focuses only on cleaning the standardized WELFake text fields before any downstream analysis or modeling.

## Objective
Use the standardized dataset from the previous task and remove:
- punctuation
- numbers
- special characters
- non-alphanumeric symbols

Keep only meaningful alphabetic words and spaces, while handling missing or non-string values safely.

## Scope
This task does not include:
- stemming
- lemmatization
- stopword removal
- TF-IDF
- model training

## Input
The script reads the standardized dataset saved in the project data folder:

- `data/data_cleaned_task6.csv`

## Output
The cleaned dataset is saved here:

- `data/data_cleaned_task7.csv`

## Method
The cleaning pipeline uses Python, Pandas, and regex-based string processing:

1. Load the standardized dataset.
2. Convert missing or non-string values to empty strings.
3. Convert text to lowercase.
4. Remove all characters outside letters and spaces.
5. Collapse repeated whitespace into a single space.
6. Save the cleaned dataset.
7. Print before-and-after examples and validation checks.

## Example
Sample before-and-after cleaning:

- Before: `law enforcement on high alert following threats against cops and whites on 9-11by #blacklivesmatter...`
- After: `law enforcement on high alert following threats against cops and whites on by blacklivesmatter...`

## Usage
From the project root, run:

```bash
python task_7_text_cleaning/text_cleaning_task.py
```

## Conclusion
The text-cleaning step successfully removes punctuation, digits, and noise while preserving meaningful words and spacing. The cleaned data is standardized and ready for later stages without introducing unnecessary transformations.
