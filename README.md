# Starbucks Index

### The Starbucks Tall Latte

![coffee](starbucks.jpeg "Starbucks Coffee")

Starbucks can be considered iconic as it is one of the most recognizable coffee stores in the world. With over 35,000 stores in 80 different countries, Starbucks has distinguished itself as one of the world’s most successful companies in the coffee industry. For this project to be successful, it is important that the product chosen is identical wherever you go. Starbucks is known for altering their menu to better appeal to the country they are in however one item that is the same everywhere you go is the Starbucks Tall Latte. A simple drink recognized and loved by coffee fanatics on a global scale!


## Bulding my Index:

### 1. Finding my data and using web scraping to import it

I was able to find pricing data on Starbucks tall lattes around the world through this website, https://www.finder.com/ca/starbucks-index. The website essentially had the prices of a tall latte in 76 different countries all displayed in a table. After a simple scrape I had my pricing data and was ready to start tidying up.

![code1](code1.png "Code used for web scraping")
![code2](code2.png "Code used for web scraping")

### My data:
![code3](code3.png "My table")


### 2. Tidying up my data

My data was not in need of much cleaning however it still needed work. The first thing I did was select only 10 countries out of the 76 as this was the requirement. I selected 10 rows simply by using the ‘take’ command and ensuring that Canada was a part of the selected countries. I kept all this data in a table called ‘coffee_prices.’

I then needed to convert the prices into floats (numbers) from string seeing that they were displayed with a currency sign ($10.23). To do this I defined a function that uses the command ‘strip’ to get rid of the currency sign and leave me with the prices as numbers. All I needed to do was apply this function to the column ‘prices’ in my table. This is important as I will later be manipulating these prices, and this can only be done if they are numbers. 

This was practically all the tidying up my data needed. I am now ready to start using this data to create my index!


### 3. Displaying local prices and currency codes

As part of the assignment, I needed to display the prices in different countries in their respective currencies. Since I already had the prices in CAD I needed to work back from there. I first gathered the exchange rates for the 10 chosen countries and created an array for them. I also created an array with all currency codes of the chosen countries. I then defined a function that simply multiplies 2 given elements, in this case it would be the price in CAD multiplied by the exchange rate of the respective country. I created a new table called ‘coffee_prices_local’ in which I brought everything together. I had 4 columns which were ‘Country’, ‘Price (CAD)’, ‘Local Currency Codes’ and ‘Local Price.’ The table displayed the 10 countries with the price of a tall latte in CAD as well as in their local prices.

[code4](code4.png "Code used for price conversions")
