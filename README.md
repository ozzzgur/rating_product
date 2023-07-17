# Rating Product & Sorting Reviews in Amazon

## Business Problem

One of the key challenges in e-commerce is accurately calculating ratings for products based on post-purchase reviews. Solving this problem can lead to increased customer satisfaction on the e-commerce platform, product visibility for sellers, and a seamless shopping experience for buyers. Another challenge is sorting reviews for products accurately. The prominence of misleading reviews can directly impact product sales, resulting in financial losses and customer attrition. By addressing these two fundamental problems, e-commerce platforms and sellers can boost their sales while providing customers with a hassle-free shopping journey.

## Dataset Story

This dataset contains Amazon product data, including various metadata related to product categories. It focuses on the electronics category and includes user ratings and reviews for the most reviewed product.

**Variables:**
- `reviewerID`: User ID
- `asin`: Product ID
- `reviewerName`: User Name
- `helpful`: Helpful rating score
- `reviewText`: Review text
- `overall`: Product rating
- `summary`: Review summary
- `unixReviewTime`: Review time (UNIX timestamp)
- `reviewTime`: Review time (raw)
- `day_diff`: Number of days since the review
- `helpful_yes`: Number of users who found the review helpful
- `total_vote`: Total number of votes for the review

## Task 1: Calculate Weighted Average Rating Based on Recent Reviews and Compare with the Existing Average Rating

In this task, our goal is to evaluate the given ratings by assigning weights based on the review dates. We need to compare the initial average rating with the weighted average rating obtained.

### Step 1: Read the Dataset and Calculate the Average Rating of the Product

Import the necessary libraries and read the dataset.

### Step 2: Calculate Weighted Average Rating Based on Review Dates

Convert the "reviewTime" column to datetime format and calculate the weighted average ratings for different time intervals.

## Task 2: Determine the Top 20 Reviews to be Displayed on the Product Detail Page

### Step 1: Generate the "helpful_no" Variable

Create the "helpful_no" variable by subtracting the "helpful_yes" count from the "total_vote" count.

### Step 2: Calculate the "score_pos_neg_diff," "score_average_rating," and "wilson_lower_bound" Scores and Add them to the Dataset

Calculate the scores and add them as new columns.

### Step 3: Determine the Top 20 Reviews and Interpret the Results

Sort the dataset by the "wilson_lower_bound" score in descending order and select the top 20 reviews.

This will provide the top 20 reviews based on the Wilson Lower Bound score, which can be displayed on the product detail page.
