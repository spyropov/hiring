{% include online-assignment/intro.md %}

# Problem

We are given advertising metrics for two companies. We want to calculate **if there is a discrepancy/difference** between the two datasets.

# Dataset format

The data is in JSON files and the two companies use the exact same JSON format.

The advertising metrics are aggregated on an hourly basis.

Each JSON file contains a list of objects (one for each hour) and each object has the following properties:
- **timestamp (string):** The timestamp of the hour that this object is representing (in ISO 8601 format)

- **spend (decimal):** The total spend/revenue generated in this hour

- **impressions (integer):** The total impressions (ad views) generated in this hour

You can view a sample here: https://s3.amazonaws.com/avocarrot-hiring/backend/companyA.json

# Objective

We want to create a system which will take as input the two datasets (one for Company A and one for Company B) and will return a list of the hours for which we detected a discrepancy higher than 5% in any of the two metrics (spend and impressions). 

# Deliverables

In your uploaded solution you should include:

- The complete working code (so that we can run your solution on our machines) 

- Passing end-to-end tests for the test cases listed below

- Any special instructions on how to run your code (in a txt file)

# Test cases

## Test case 1 (No discrepancies detected)

Company A dataset: https://s3.amazonaws.com/avocarrot-hiring/backend/companyA.json

Company B dataset: https://s3.amazonaws.com/avocarrot-hiring/backend/companyB-no-discrepancies.json

Expected output: Empty list

## Test case 2 (Discrepancies detected)

Company A dataset: https://s3.amazonaws.com/avocarrot-hiring/backend/companyA.json

Company B dataset: https://s3.amazonaws.com/avocarrot-hiring/backend/companyB-discrepancies.json

Expected output: https://s3.amazonaws.com/avocarrot-hiring/backend/expected-discrepancies.json