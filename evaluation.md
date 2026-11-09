## 1. What was the most challenging part of this lab for you, and how did you overcome it?

The most challenging part was getting pandas to work in my notebook. When I ran the first cell, I received a `ModuleNotFoundError` saying that pandas was missing. With guidance, I ran `uv add pandas` in the terminal, checked that the notebook was using the project's `.venv` Python environment, and restarted the notebook kernel. After running the cells again, the import worked and I could continue the analysis.

## 2. Which dining hall did you choose to analyze?

I chose Brooks. I filtered the original data to keep its 15 records and stored them in a separate DataFrame called `filtered_df`.

## 3. For your chosen dining hall, which day had the highest coffee consumption per swipe?

January 26, 2024 had the highest coffee consumption per swipe at Brooks. The recorded coffee consumption was 40 and the number of swipes was 130. Dividing 40 by 130 gives approximately 0.307692 per swipe. This date appeared first after I sorted `average_coffee` in descending order.

## 4. How would you determine which day had the lowest coffee consumption per swipe for your dining hall?

I would sort `average_coffee` in ascending order and display the first row:

```python
print(filtered_df.sort_values(by="average_coffee", ascending=True).head(1))
```

For Brooks, the lowest value occurred on January 8, 2024: 24 divided by 108 equals approximately 0.222222 per swipe. Since my saved data is already sorted in descending order, I could also use `filtered_df.tail(1)` to find this row.