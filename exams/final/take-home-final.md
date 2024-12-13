# Data 200: Data Systems for Data Analytics


# Name:

# Take Home Final Exam
<font color='red'>**Due Date:** Dec 20, 5p (T-F 1:30p section) </font> <br>
<font color='red' style="margin-left: 1.85cm; display: inline-block;">Dec 21, 11:59a (T-F 3p section)</font>

---

### **Task**: Scrape data from Goodreads.com 📚

---

### **Objective**
For this exam, you will scrape and analyze data from Goodreads.com. The work is split into two parts, each focusing on different aspects of the data
1. **"Best Books" Analysis**: Explore Goodreads' "Best Books" lists for a specific year.
2. **Author-Level Analysis**: Study the trends and patterns in the works of a specific author.

---

### **Instructions**

#### **Task 1: Best Books**
You are tasked with analyzing Goodreads' "Best Books" lists for a specific year based on the **first letter of your first name**. For example, if your first name starts with **A–E**, you are assigned to the year **2023**; if it starts with **F–J**, you are assigned to **2022**, and so on:

| Initials | Assigned Year | URL                                              |
|----------|---------------|---------------------------------------------------------|
| A–E      | 2023          | [Best Books of 2023](https://www.goodreads.com/list/best_of_year/2023) |
| F–J      | 2022          | [Best Books of 2022](https://www.goodreads.com/list/best_of_year/2022) |
| K–O      | 2021          | [Best Books of 2021](https://www.goodreads.com/list/best_of_year/2021) |
| P–T      | 2020          | [Best Books of 2020](https://www.goodreads.com/list/best_of_year/2020) |
| U–Z      | 2019          | [Best Books of 2019](https://www.goodreads.com/list/best_of_year/2019) |



**Your Tasks**:
1. Scrape data from the Goodreads "Best Books of [Year]" list:
   - **URL**: https://www.goodreads.com/list/best_of_year/2023 (replace the year with your assigned year). You can also use the table above.
2. Collect the following data for each book:
   - Title
   - Publication date (first published)
   - Author
   - Genre (if available, and feel free to pick the first genre listed)
   - Average rating
   - Number of ratings
   - Number of pages
   - Rank
   - Language (if available)
   - Number of people who are currently reading (if available)
   - Number of people who want to read (if available)
3. Perform the following analyses:
   - **Genre ratings**:
       - Compare average ratings across genres. Which 2-3 genres tends to have the highest ratings? Create a table showing average rating score, and average rank by genre.
   - **Popularity and ratings**:
       - Examine whether books with more ratings tend to have higher or lower average scores. Create a scatterplot showing the relationship between the number of ratings and average rating. On the x-axis, you should have **number of ratings**; on the y-axis, you should have **average rating**.

---

#### **Task 2: Author-Level Analysis**
You are now tasked with analyzing books by a specific author based on the **first letter of your first name**:

| Your first name initial | Author              | Author Goodreads link                               | Birthday       |
|----------|---------------------|--------------------------------------------------------------------|----------------|
| A–E      | Stephen King        | [Stephen King](https://www.goodreads.com/author/list/3389)         | Sep 21, 1947   |
| F–J      | George R.R. Martin  | [George R.R. Martin](https://www.goodreads.com/author/list/346732) | Sep 20, 1948   |
| K–O      | Ernest Hemingway    | [Ernest Hemingway](https://www.goodreads.com/author/list/1455)     | Jul 21, 1899   |
| P–T      | Neil Gaiman         | [Neil Gaiman](https://www.goodreads.com/author/list/1221698)       | Nov 10, 1960   |
| U–Z      | Nora Roberts        | [Nora Roberts](https://www.goodreads.com/author/list/625)          | Oct 10, 1950   |


**Your Tasks**:
1. Scrape all books by your assigned author:
   - Use the link provided for your author.
2. Collect the following data for each book:
   - Title
   - Publication date (first published)
   - Author
   - Genre (if available, and feel free to pick the first genre listed)
   - Average rating
   - Number of ratings
   - Number of pages
   - Rank (from the books written by the author)
   - Language (if available)
   - Number of people who are currently reading (if available)
   - Number of people who want to read (if available)
3. Perform the following analyses:
   - **Language Distribution**:
     - How many books has the author published in English? In other languages? Create a table showing the count of books by language.
   - **Author's Age and Page Count**:
     - Do authors tend to write longer books as they age? Use the author's birthday to calculate their age at the time of each book's publication. Create a line plot with **author's age** on the x-axis and **page count** on the y-axis.
   - **Author's Age and Rating**:
     - For English-only books, create a line plot with **author's age** on the x-axis and **average rating** on the y-axis.
     - Repeat the analysis including books in languages other than English. Does your interpretation change?
   - **Pages vs. Ratings**:
     - Is there a relationship between the number of pages and a book's average rating? Create a scatterplot with **page count** on the x-axis and **average rating** on the y-axis.
   - **Interest on a book**:
     - Is there a relationship between the number of people who are currently reading the book and the number of people who left a rating? Create a scatterplot with **number of people who are currently reading** on the x-axis and **number of ratings** on the y-axis. Create a second scatterplot with **average rating** on the y-axis. Do books with more interest tend to receive higher ratings?

---

### **Submission Requirements**
Submit your work as a single `.ipynb` file, along with a copy of it as a `.md` file. The notebook should include:
1. **Code**:
   - Well-documented python code using Selenium for web scraping.
   - Proper error handling and strategies for dynamic content.
2. **Cleaned Data**:
   - Include the cleaned datasets from both tasks as .csv files. You can upload them in your github repo.
3. **Analysis and Report**:
   - Present your findings using markdown cells, tables, and visualizations you make in python.
   - Address all questions posed for your assigned tasks.
4. **Visualizations**:
   - Include relevant charts (e.g., bar charts, line plots, scatterplots) to support your conclusions.

---

### **Rubric**

| Item                        | Weight |
|-----------------------------|--------|
| Code accuracy               | 25%    |
| Code clarity and annotation | 25%    |
| Exploratory data analysis   | 25%    |
| Discussion of findings      | 25%    |

---

### **Tips**
- Make sure to insert time.sleep() right after you request driver to go to a link (before requesting elements). Make sure to wait at least 0.7 second, or even slightly higher if you run into issues.
- Try-except blocks will be your friend because xpath positions on a page may differ depending on the book and content availability.

---

### **Resources**
- Course notes on Github
- Selenium documentation: https://www.selenium.dev/documentation/
- Pandas documentation: https://pandas.pydata.org/docs/
- Matplotlib documentation: https://matplotlib.org/stable/contents.html

Good luck! 🏁



```python

```
