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

Employees upload bank statements or open item lists. The system recognizes patterns (e.g., names, amounts, time frames), assigns the payments to invoices, and creates an overview. Open items can be automatically exported as reminders.



Simplifyed prototype of AI_Method:
This just assign the example input to the groups: "rent", "bill" and "unclear".
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
So the inputs of the customer where assign. The next step is to clearify the "unclear" values and figuere out the differences of the groups to can exactly determine where the saldo comes from.

## Data sources and AI methods

AI methods:
NLP (Natural Language Processing)
Clustering / Matching
Rule-based logic

## Challenges

The AI_Method should exactly solve the descripted problem. Maybe somtimes the Method can not say if the assignment is 100% correct. 

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
  <br>For example: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
* etc
