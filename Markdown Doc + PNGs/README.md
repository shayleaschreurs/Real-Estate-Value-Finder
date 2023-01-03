# A Solution To Finding Homes Under Average Market Price

## Our Mission

   Our goal is to analyze housing data in an attempt to find properties listed significantly under the average price of comparable homes in a given area. In doing so, we hope to help any future investors find a home for the best possible value. 

## The Data

We knew we wanted to use an API to help us form some data frames. Reality Mole provided us with a few very valuable APIs. With the the Reality Mole APIs, we were able to pull property listings with their addresses, latitude and longitude coordinates, square footage, number of bedrooms and bathrooms, and comparables. We were able to form a few different data frames to help us organize the data in a way that allowed us to analyze it and come to conclusions about where each home fell on the pricing spectrum.

The comparable API proved to be very valuable in helping us create a data frame that lists homes with very similar specifications. The way it works is, first, we select a target property, then we feed it into the API call. And wah lah! The API will gives us data that shows the target property along with 5-20 very similar homes. This allows us to find all the homes within a certain area, with a certain number of bedrooms and bathrooms, and compare their prices with ease.

## The Visualizations

Figure 1 is a geo plot that displays all the listings in the area including all property types. The gradient represents the square footage of each property if availble. 

![Plot #1 - Raw Listings Geo Plot.png](attachment:9a8af5c9-7a7d-4e7c-ae1f-d273e032e537.png)

Figure 2 shows the same listings as above on a scatter plot based on price per square foot.

![Plot #2 - Raw Listings Scatter Plot.png](attachment:9b790375-2776-43c7-a526-6e6c47da2e0e.png)

Figure 3 is another geo plot narrowed down to single family homes in the area.

![Plot #3 - Selected Listings Geo Plot.png](attachment:304f38d5-6961-470b-ba30-b3903f545421.png)

Figure 4 represents the data from figure 3 in a scatter plot based on price per square foot.

![Plot #4 - Selected Listings Scatter Plot.png](attachment:850f95bb-d966-40f5-9495-35c167f5a89b.png)

Figure 5 displays a geo plot of comparables based on the target property. The lighter gradient dots represent properties with a lower price per square foot. These are the homes we are seeking out.

![Plot #5 - Comparables Geo Plot.png](attachment:b5793999-d6ff-4ffa-b7db-d2096f8f3ae8.png)

Figure 6 is a scatter plot of the data from figure 5. The bottom right quadrant will have homes with a lower price per square foot. These are the homes we are seeking out. The top left quadrant will have homes with a higher price per square foot. These are homes we would avoid.

![Plot #6 - Comparables Scatter Plot.png](attachment:f42ba4ae-fa99-487c-b5a4-e2d885c61b97.png)

## Our Analysis

#### Were we able to find an API that gave us the data we were looking for? 

Reality Mole provided us with more than enough information. We were concerned we might have to find multiple APIs for each different type of data we would need, but Reality Mole had everything we needed and more. The main data points we wanted were lat/long cooordinates, prices of homes, square footage, and number of bedrooms and bathrooms. We knew we would could make a solution with all of this information. Reality Mole really helped us more than we expected with the comprable API because it gave us exactly the information we needed to compare similar homes without putting in a ton of effort. 

#### Were we able to use this data to pinpoint properties that are priced sigificantly below average market value?

Yes, looking at the visuals that the comprable API helped us create, we can see that there is quite a range in prices for homes that have similar specs. All of these homes are 3 bedroom, 2 bathroom homes with about the same amount of square footage, and in the same area. The highest priced home, which is our target property is \\$731 per square foot and the lowest is \\$246 per square foot. 

#### Is this a tool that investors could use to buy a home for the best possible value?

Yes. Investors can save a lot of time using this tool to narrow down homes similar to what they are lookin for and easily be able to see which ones have a better price. Rather than hiring an inspector on tons of homes that may not even be a good value, investors can go in after using our tool to narrow it down, then hire an inpsectore on much fewer properties. This will save them countless hours, money on inspectors, and most importantly buy a home for the greatest value.

## How To Use Our Product

### Instruction

Step 1: Install Realty Mole API
Step 2: Import the following: os, pandas, numpy, hvplot.pandas, json, requests, dotenv, &matplotlib inline
Step 3: Call API
Step 4: View API in JSON format
Step 5: Target an opportunity area
Step 6: Pull and restructure data from opportunity area
Step 7: Compare comparable properties
Step 8: Create visualizations for simplification in storytelling