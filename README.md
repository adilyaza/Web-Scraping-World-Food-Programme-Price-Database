# World Food Programme: food price and affordability analysis
### Web scraping

This script illustrates the first phase of the 'World Food Programme: Food Price and Affordability Analysis' project. The project is using data from the World Food Programme Price Database.  

The World Food Programme is monitoring the price of staple foods included in a [basic food basket](https://humanitarianglobal.com/key-tools-and-types-of-information-required-for-monitoring-the-adequacy-of-ration-in-emergencies/#:~:text=Food%20Basket%20Monitoring%20(FBM)&text=A%20systematic%20sample%20of%20households,each%20of%20their%20food%20items) across 99 countries. In the World Food Programme Price Database, the data is stored and can be downloaded at a country level. I aim to merge the available data to gain a global perspective on food price dynamics. The [following Python code](https://github.com/adilyaza/Web-Scraping-World-Food-Programme-Price-Database/blob/main/Data%20Scraping.%20Global%20food%20price%20data%20monitoring.ipynb) was used to create a combined food price data set  in 3 steps: 

1. Scraping

With the list of URLs from ['wfp_countries_global.csv'](https://www.kaggle.com/datasets/jocelyndumlao/global-food-prices?select=wfp_countries_global.csv) I can gain access to each page on [OCHA Services](https://data.humdata.org/dataset?dataseries_name=WFP+-+Food+Prices) where the food price data for each country can be downloaded in a.csv format. Using BeautifulSoup, I've scraped each of the pages to retrieve the links to the individual country data.

2. Using a for loop to download 99 individual data sets

Using the list of links to the individual data sets, I've created a for loop to download all the files. 

3. Combining the data into a single data set

Using pd.concat, I combined the data from the 99 individual data sets into one single dataframe and exported it for further analysis.
