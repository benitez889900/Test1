# EDINBURGH PROPERTY MARKET INSIGHTS

### PROJECT SUMMARY 
Last year I decided to start a project to study the house market prices in Edinburgh. Just having bought my first property and with the market on an upwards trend, I found the process of knowing how much to bid to secure a property challenging and frustrating at times. 

My intention was to develop a system that would allow me to monitor, over time, the fluctuation of prices in the different areas of Edinburgh, as well as how much under/over the asking price the properties sell for. In addition to the above, at the time of creating the script I also noticed that I could gain information about the performance of the Estate Agents involved in the sales as this information was available in the listings, so this too was recorded. 

I have been collecting data for over 8 months - approximately 1K entries. Even though this amount of information doesn’t provide yet enough backing to present definitive conclusions, it is possible to start identifying some tendencies and therefore I have decided to publish the first batch of results.The findings are presented through simple and easily understandable visualizations. The intention is to build on this idea and apply a similar approach to other cities in Scotland and the UK.

### MAIN FINDINGS
<dl>
  <dt>Some of the key insights that this project has started building are:</dt>
</dl>

1. What is the average asking price range by postcode sector (this is to the EHXY Z## level of detail)
2. How much over or under the asking price, in average, are properties sold for on each sector.
1. Which are the most/less popular areas of Edinburgh where properties are being listed for sale.
2. What are the usual range of different Estate Agents listings? Is there a difference - for instance some agents specialising in cheaper/more expensive properties?
2. What are the sold prices achieve, in average, by different Estate Agent? Would it be expected a difference if a property is listed with different Agents?


<img width="1302" alt="Properties asking prices" src="https://user-images.githubusercontent.com/70529856/91867653-cb054f00-ec6b-11ea-8f05-0fca4b08db83.png">
<img width="1141" alt="Properties sold prices over-under" src="https://user-images.githubusercontent.com/70529856/91868229-6dbdcd80-ec6c-11ea-9277-32a07e09cb62.png">

#### POPULAR AREAS FOR PROPERTIES LISTINGS
<img width="992" alt="Properties listings locations" src="https://user-images.githubusercontent.com/70529856/91867997-29cac880-ec6c-11ea-9c58-da078c0e3453.png">

![Estate Agents Asking Price](https://user-images.githubusercontent.com/70529856/91870111-8c24c880-ec6e-11ea-9909-a3f829d3a1bf.png)
![Estate Agents OverUnder](https://user-images.githubusercontent.com/70529856/91870113-8dee8c00-ec6e-11ea-844d-714c1f082bff.png)

## PROBLEM STATEMENT 

A year and a half ago I embarked with my wife in the challenging task of buying our first property. We live in Edinburgh, Scotland, where the market has been strong for the last few years and securing a new property is challenging. So, as well as being an exciting time, it can also become quite stressful and frustrating.

Like in many other places, the process for purchasing a new house works in a way that houses are advertised for a certain price (Asking Price), which is usually around the value set up in the Home Report (HR value) which is a mandatory document for any property being sold and establishes the condition of the property along with an estimation of the current market value. With this in mind, people are free to bid whatever they wish to secure the place. Usually the highest bidder is the one that ends up securing the place, defining the Sold Price for the property. 

Therefore, after attending a viewing for a property that we liked and reviewing its HR, it always arose the question: how much should (and can) we offer for this place in order to secure it?

This was not straightforward because, in order to find the right answer, I would need to have information on previous Asking Prices for properties nearby, and the Sold Price achieved by them. That would give us information on similar properties in terms of size and location that we could extrapolate to ours. However, this information was not easy to get since those two prices would not be available at the same time. The Asking Price is available while the property is still up for sale, whereas the Sold Price is shown only after all the legal procedures are finalised and this is at least 3 to 4 months after the sale takes place when the Asking Price has long been removed. Also, the differences between Asking Prices and Sold Prices vary considerably between different areas of the city - but this was not known to us.

## SOLUTION FUNCTIONALITY

In order to provide insight I developed a web scraper that would store the properties as they would become available to the market and try to match them with their Sold Price once this information became available as well - usually a couple months after the sale has been finalise. All the results are stored in a .csv file from which visualizations can be pulled at anytime. The Figure below shows this working arragement:

<p align="center">
<img width="675" alt="Functionality" src="https://user-images.githubusercontent.com/70529856/91943681-e2d4e580-ecf4-11ea-89c2-98142e764294.png">
</p>

#### ListintScraper

In the information recorded for each property would be included:
1. What the date of the property being posted, 
1. The number of beds, 
1. The asking price and also 
1. The State Agent that carrying out the sale 

