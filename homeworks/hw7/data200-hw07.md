# Data 200: Data Systems for Data Analytics


# Homework 7: API

**Dickinson College**<br/>
Prof. Eren Bilen<br/>
<font color='red'>**Due Date:** Dec 12 at 11:59p </font>
---
Enter your name in the markdown cell below.

# Name:

# Tasks

- Review the notes posted on Github on regular expressions and API.
- Review pages 103-128 in Bressoud & White textbook on regular expressions.
- Review the TMDB API documentation on https://developers.themoviedb.org/3/getting-started/introduction
- Commit and push your completed `.ipynb` and `.md` files


```python
import re
```

# Exercises: API

Please go to https://developers.themoviedb.org/3/getting-started/introduction and create a free account. Using your free account, get an API key. With your unique API key, you will be able to send requests to TMDB for data retrieval. Review the API documentation on "/discover/movie" at https://developers.themoviedb.org/3/discover/movie-discover


```python
import requests
import pandas as pd
```

<div class="exercise"><b>Exercise 1:</b></div> 

Return the 10 highest rated movies (according to `vote_average`) in 2021 that have received more than 5000 votes (according to `vote_count`). Return `title`, `vote_average`, and `vote_count` *Hint: insert the filter requests to your API query*.


Below is the output from my solution:<br>
<code>
                          title  vote_average  vote_count
0  Zack Snyder's Justice League           8.2        8356
1                        Nobody           8.1        5244
2                       Cruella           8.1        7699
3       Spider-Man: No Way Home           8.0       15948
4      Raya and the Last Dragon           8.0        5717
5              The Tomorrow War           7.9        5984
6                          Luca           7.9        6877
7                          Dune           7.8        8014
8             Godzilla vs. Kong           7.7        8380
9                       Encanto           7.7        7614
</code>


```python

```

<div class="exercise"><b>Exercise 2:</b></div> 

Return the 10 highest rated movies (according to `vote_average`) that were released between 1980 and 2022 and have received more than 5000 votes (according to `vote_count`). Return `title`, `vote_average`, `vote_count`, and `year` *Hint: Use a combination of filtering via API request and filtering via Pandas.*.


Below is the output from my solution:<br>
<code>
                      title  vote_average  vote_count  year
0  The Shawshank Redemption           8.7       22733  1994
1          Schindler's List           8.6       13478  1993
2              Pulp Fiction           8.5       24112  1994
3         Life Is Beautiful           8.5       11477  1997
4                  Parasite           8.5       14772  2019
5              Forrest Gump           8.5       23659  1994
6                GoodFellas           8.5       10698  1990
7            The Green Mile           8.5       14667  1999
8             Spirited Away           8.5       13592  2001
9                Your Name.           8.5        9255  2016
</code>


```python

```

<div class="exercise"><b>Writing in Discipline (WiD) Assignment:</b></div> 

The SQL Murder Mystery is a fun story based game experience where you use SQL code and a careful inspection of a relational database structure to solve a murder mystery: https://mystery.knightlab.com

Please go ahead and give the game a try. Feel free to use the walkthrough if you get stuck on any part of it.

Your assignment is to write your own "story" where your story includes an event where its details could be traced in a relational database, much like the SQL Murder Mystery's story. Please feel free to be creative! After you turn in your WiD assignment, I will give you my feedback, and you will resubmit an updated version which then will be included in your WiD portfolio. Note that you have to complete this assignment even if you are not a Data Analytics Major. Please make sure your story is around 500 words. Feel free to use a relational database schema you construct "by hand". Good luck, and I look forward to reading your stories!


```python

```
