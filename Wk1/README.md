# Data Mining


Imagine you're organizing a small birthday party for your friend in college. It’s a big day for them, and you want it to be memorable. So you’ve invited everyone they know - school friends, college friends and extended family. But there is one problem: all the guests at this party don’t know each other at all!
To ensure that everyone can easily interact with each other, and enjoy themselves, you’ve decided to include some party games. You already have a list of games that sound fun, but you’re unsure which ones can be enjoyed equally by everyone attending.


So, what do you do? How do you choose the right games for this party?

Simple. Instead of blindly guessing or relying on your personal preferences, gather information on what your guests prefer and plan accordingly. You can talk directly to people from each group to understand their preferences, or you can explore online to discover their interests. This way, you’ll be certain about which games should be included in the mix.




Similarly, in business, understanding your customers' needs through data gathering is crucial. By analyzing customer feedback, market trends, and consumer behavior, you can tailor your products, services, and marketing strategies effectively. This data-driven approach ensures your business decisions are as well-informed as planning a successful party that delights all attendees.


In this project, I gathered data from Amazon reviews of 12 different products for analysis. 

This hands-on experience was done with the sole purpose of understanding the challenges and best practices of data collection. 

## Here is a quick overview of the steps I followed to gather data for this project:
1. Select Products: Find one Beats product (Speaker) and 11 competitor products with a good number of reviews.
2. Scrape Reviews: Use OxyLabs API to scrape the reviews. by inputting the URLs into the relevant spaces.
3. Save Data: Download the reviews and save them as a CSV file.


Step 1: Finding Products to Review
    My first task was to identify as many products on Amazon with a substantial number of reviews. One of these products should be a Beats product, and the others should be from different brands, acting as competitors to the Beats product. This exercise was to help me understand how to select relevant data sources for your analysis.
        1. Identify Beats Product: I selected a beats product, 'Beats Pill Speaker' because it had lots f reviews (my aim was for at least 100 reviews, More reviews mean more data for my analysis!) on Amazon. I copied the URL from the address bar because it is my gateway to all those reviews.
        2. Identify Competitor Products: I selected 11 competitors wo had similar products like the Beats pill Speaker. I ensured each product had a good number of reviews, copied the URLs of these product pages.
## Step 2: Data Mining – Collecting Amazon Reviews

**Overview**  
- Purpose: Gather Beats Pill Speaker + 11 competitors' Amazon reviews for sentiment analysis and comparisons.  
- Approach: Data-driven workflow to select products, scrape reviews, and save data for analysis.

**High-level workflow**  
1) Choose products  
- Beats product: Beats Pill Speaker  
- 11 competitor products with substantial reviews (target ~100+ per product)

2) Scrape reviews  
- Use Oxylabs API by inputting product URLs  
- Ensure parameters maximize data quality (sufficient pages, appropriate user agent)

3) Save data  
- Download reviews and save as a CSV for analysis

**Notes**  
- Beats Pill Speaker chosen for large review volume to support robust analysis.  
- If a product has fewer reviews, include additional pages or listings to reach a meaningful dataset.

---

## Step 3: Save the Data

**Purpose**  
- Save all collected reviews to a CSV file as the final deliverable for this step. Do not edit the raw data file after saving.

**Scope**  
- Dataset includes reviews for one Beats product and four competitor products with a substantial number of reviews.

**Ethics**  
- Follow data collection ethics and respect terms of service; avoid violations.

**What you’ll end up with**  
- A CSV file containing the reviews for subsequent steps (data cleaning and analysis).

**Next up**  
- In the next module, explore Pandas to clean and preprocess the data.




# Step 2: Extract Amazon Reviews with Oxylabs

Overview
- For dynamic sites like Amazon, using a third-party tool simplifies scraping and lets you focus on analysis.
- This guide uses the Oxylabs API, which offers a generous free tier (up to 5,000 requests in a 7-day trial).

Important notes
- Complete all requests within the trial period. Create the trial account only when you’re ready to start sending requests.
- Amazon limits can yield ~100 reviews or 10 pages per product. This is acceptable for our assignment, as we target 100 reviews per product.

Demo and data flow
- A full demo shows extracting Amazon reviews with Oxylabs, processing the data, and exporting to CSV.
- After extraction, parse the JSON into a dataset and export as CSV for analysis.

High-level workflow
1) Access Oxylabs API
   - Sign up for an Oxylabs account using Google.
   - Open the eCommerce Scraper API or Scraper API Playground.

2) Configure the request
   - Enter the Amazon ASIN (product identifier).
   - Choose a user agent (e.g., desktop).
   - Disable JavaScript rendering.
   - Enable parsing to get structured data.
   - Set domain to Amazon (.com for US).
   - Specify starting page and number of pages (up to 20).
   - Test the request with the validation button.

3) Increase data collection if needed
   - If limited to 100 reviews, increase the number of products or adjust pages to collect more data.

4) Export data
   - Export results as JSON.
   - Load the data into a dataset (e.g., in Colab) using the provided code.

5) Compile data to CSV
   - Store the data frame as a CSV file in Colab’s runtime.
   - Download the CSV file for safekeeping.

6) Merge and finalize
   - Load multiple CSVs into data frames.
   - Merge data frames to concatenate all data.
   - Export the final merged data frame to a single CSV for analysis.

Safety and best practices
- Be mindful of Oxylabs’ 5,000-request free tier.
- Avoid excessive, random requests to maximize free tier usage.
- Download and securely store all final CSV files.

If you’d like, I can tailor this to match your exact repository structure or convert it into a compact Markdown block you can paste directly into README Step 2.


