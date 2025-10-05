<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Project Title

account clarification

## Summary

Many companies need to resolve outstanding items in customer accounts because payments often don't exactly match invoices. My idea is an AI that automatically assigns incoming payments to the correct invoices, calculates balances, and creates reminders, including late payment fees.



## Background

Incorrect or incomplete payments are a regular occurrence, particularly in the real estate and energy sectors. Manual reconciliation is error-prone and time-consuming.

* problem 1: account clarification
* problem 2: reminder sending



## How is it used?

#Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?
Employees upload bank statements or open item lists. The system recognizes patterns (e.g., names, amounts, time frames), assigns the payments to invoices, and creates an overview. Open items can be automatically exported as reminders.

#Images will make your README look nice!
Once you upload an image to your repository, you can link link to it like this (replace the URL with file path, if you've uploaded an image to Github.)
![Pfoto](...)

If you need to resize images, you have to use an HTML tag, like this:
<img src=<...>

This is how you create code examples:
```
import pandas as pd
data = {
    "date": ["2025-01-01", "2025-01-05", "2025-01-10"],
    "amount": [500, -200, -300],
    "purposeofuse": ["bill 123", "custumer a payment", "rent january"]
}

df = pd.DataFrame(data)

# solve saldo
saldo = df["amount"].sum()

# identify open positions (simplified logic)
df["assignment"] = df["purposeofuse"].apply(
    lambda x: "rent" if "rent" in x else "bill" if "bill" in x else "unclear"
)

print(df)
print("Saldo:", saldo)


```


## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
If you need to use links, here's an example:
[Twitter API](https://developer.twitter.com/en/docs)

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

AI methods:
NLP (Natural Language Processing)
Clustering / Matching
Rule-based logic

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?
The AI_Method should exactly solve the descripted problem.

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
  <br>For example: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
* etc
