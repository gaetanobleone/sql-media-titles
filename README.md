# Data Visualization In Netflix

Overview:

In this project, the goal had been to demonstrate the affective utilization of sql, python, and excel for managing, and analyzing data regarding television series, and movies on the site Netflix; the dataset was sourced from an external site, that is Kaggle. In addition, this project displays the use of the following skills...

* data import
* data export
* data cleaning
* data visualization


## Description

I will take you step-by-step through the process of the project. I began the project by sourcing data concerning television series, and movie titles. I then created a database titled “netflix” to host the table title “media” which contained a list of television series, and movie titles that had been imported into the table. In the process of importing said data into the table, I ran into an issue concerning the original dataset. The original dataset contained several commas trailing at the last column; thus, to remove said trailing commas I wrote a script in “python”.

```
import csv

# the file in question
old_file = r"C:\Users\gaeta\Desktop\sql_project\dirty_netflix_titles.csv"

# the new file.
new_file = r"C:\Users\gaeta\Desktop\sql_project\cleaned_netflix_titles.csv"

'''this opens up "old file" reads each row up until row 12, 
and then skips to the next line, copying all the data to the "new file"'''
with open(old_file, newline='', encoding='latin-1') as f:
    reader = csv.reader(f, delimiter=',', skipinitialspace = True)
    with open(new_file, 'w', newline='', encoding='utf-8') as i:
        writer = csv.writer(i)
        for row in reader:    
            writer.writerow(row[:12])
```

The script pulls the outlined csv file, and then takes the first twelve columns of each row, and writes it into a new csv file; thus, removing the trailing commas. I then was able to take said data, select specific columns of data, export it out, and then use now exported data, turning it into a pie chart to display the ratio of television series to movie titles on the site Netflix.


# Use This... and delete the top later

# Data Visualization In Netflix

In this project, the goal had been to demonstrate the affective utilization of sql, python, and excel for managing, and analyzing data regarding television series, and movies on the site Netflix; the dataset was sourced from an external site, that is Kaggle. In addition, this project displays the use of the following skills...

<div align="center">
  <kbd>
    <img src="https://imgur.com/PBCjNZs" width="75%" height="75%" /> 
  </kbd>
</div>

## Description

Longer description explaining the rationale/intent behind the project, what it's good for, and how it works. If the next two subsections are short enough, they can be merged up into this block—perhaps as bulleted lists.

### Features

- It's TINY. A short README is a good README.
- List other standout qualities that'll make a potential user want to try out your project.

### Built with

- Markdown
- Love

## Getting started

### Prerequisites

Dependencies not explicitly covered in the installation process; e.g., OS restrictions.


