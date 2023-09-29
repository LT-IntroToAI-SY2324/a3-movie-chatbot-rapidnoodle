# Assignment 3 - Writeup

Assignment 3 is all about creating this natural language query system.  In order to do so, you have to write a lot of functions to retrieve infomation.  You will also have to write a function to return answers from a pattern-action list.  There is a lot of work to accomplish in this assignment, but this portion is intended for you to write about what you accomplished.

## Reflection Questions
1. In your own words describe the `search_pa_list` function.
This function loops through all of the available patterns and attempts to match the given source list with each pattern.
If one of the matterns match, it calls the function that is connected to that pattern to retrieve the information.
If no patterns match the source, it will let the uesr know that the bot didn't understand the prompt.

2. What movie did you add to the `movies.py` file?  What year was it made? Any specific reason you added that movie?
I added Iron Man wich (released in 2008) because I didn't see a lot of marvel movies in the list and I wanted to add
at least one of those. How can a movie database forget about the Marvel universe?

3. What pattern / action did you add to the paList data structure?  Why do you think that is a useful pattern / action?
I added "who played in movies that were made in _" to the paList data structure because the only input I need is the year.
Since the year can only be one word long, using a '_' would be the more efficient than using the '%'. It is a useful pattern
because it allows the user to get a sense of actors who were in their prime relative to a specific year.

4. What kind of chatbot would you create?  Describe why you would create it and what it would do.
If I had all of the necessary skills, I would create a completely nonbiased news AI that would be able to cover the daily news
for anyone who was interested in a quick update on the state of our world. Currently, there are many news stations that are very
one-sided and give biased information that can send the wrong message to the audience. With this bot, everyone would have accurate
news that can be respectfully discussed without references to political parties.

5. What was the most difficult portion of this assignment?
The most difficult portion of the assignment was debugging the actions for every assert because there are specific requirements
for each function that I did not reach on the first run.

6. Did you write a new assert for your pattern action?
Yes, I added a type assert and a return assert.

```python
assert isinstance(actors_by_year(["2008"]), list), "actors_by_year not returning a list"
assert sorted(actors_by_year(["2008"])) == sorted(
    [
        "robert downey jr",
        "jon favreau",
        "gwyneth paltrol",
        "jeff bridges",
    ]
), "failed actors_by_year test"
```
