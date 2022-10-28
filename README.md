# Uber Case Study
![uber-everywhere](https://user-images.githubusercontent.com/103464869/198420955-1a830889-7ecd-48d2-8d88-0bf6b65340e6.png)

This repo contains a full analysis of the trips, routes, and pricing data of Uber. Uber is a transportation company with an app that allows passengers to hail a ride and drivers to charge fares and get paid. More specifically, Uber is a ridesharing company that hires independent contractors as drivers.


The insights from this project were presented inside MicroStrategy Workstation. For quick access, a summary of insights & screen shoots is available in this [**Slide Deck**](https://docs.google.com/presentation/d/1bEHOxBG0vFUtOBV097XxyQPbmetrcAemB6gyrk0LbUU/edit?usp=sharing) 

## 1. Objectives
One of main objectives of this project was to answer questions like: 
1. How does uber uses near real-time data to determine fare prices? **(Uber's Dynamic Pricing)**
2. Does factors like weather affect _surge factor_ used by uber to determing trip fares? 
3. What best practices & routes can drivers adhere to for optimal earnings?

Furthermore, explore the potential of analysing real-time data from drivers in a specific area to provide **Drivers** with live recommendations to allow better use of their time, and increase _per hour_ earnings. 

## 2. Data Sources

The data analysed in this project are public data from [Uber](https://www.kaggle.com/datasets/mayankvashisht/uber-cab-fare-price-analysis?resource=download), [Uber Review](https://www.kaggle.com/datasets/jschne61701/uber-rides-costumer-reviews-dataset/code?select=Uber+Review+Data.xlsx), facts and supporting information from [Statista](https://www.statista.com/study/54895/uber-technologies/) retrieved for free with ESC Clermont Student Credintials, and [NYC Open Data](https://data.cityofnewyork.us/Transportation/Traffic-Volume-Counts-2014-2020-/ertz-hr4r) all accessable for free through respective links. 

### **Sample Data** 


1. **Fare Prices**

![Fare_Prices](https://user-images.githubusercontent.com/103464869/198450692-e0ab85ad-a667-477c-ae83-fc1194840886.jpg)

2. **Customer Reviews**

![Reviews](https://user-images.githubusercontent.com/103464869/198450728-18ca550e-77bb-4405-89fc-45b4a7b13e9c.jpg)

3. **NYC Traffic Data**

![Traffic_Data](https://user-images.githubusercontent.com/103464869/198450758-37926f28-f994-4650-9703-972cb6dcc450.jpg)


## 3. Analysis 



<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>distance</th>
      <th>cab_type</th>
      <th>time_stamp</th>
      <th>destination</th>
      <th>source</th>
      <th>price</th>
      <th>surge_multiplier</th>
      <th>id</th>
      <th>product_id</th>
      <th>name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.44</td>
      <td>Lyft</td>
      <td>1.544950e+12</td>
      <td>North Station</td>
      <td>Haymarket Square</td>
      <td>5.0</td>
      <td>1.0</td>
      <td>424553bb-7174-41ea-aeb4-fe06d4f4b9d7</td>
      <td>lyft_line</td>
      <td>Shared</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.44</td>
      <td>Lyft</td>
      <td>1.543280e+12</td>
      <td>North Station</td>
      <td>Haymarket Square</td>
      <td>11.0</td>
      <td>1.0</td>
      <td>4bd23055-6827-41c6-b23b-3c491f24e74d</td>
      <td>lyft_premier</td>
      <td>Lux</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.44</td>
      <td>Lyft</td>
      <td>1.543370e+12</td>
      <td>North Station</td>
      <td>Haymarket Square</td>
      <td>7.0</td>
      <td>1.0</td>
      <td>981a3613-77af-4620-a42a-0c0866077d1e</td>
      <td>lyft</td>
      <td>Lyft</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.44</td>
      <td>Lyft</td>
      <td>1.543550e+12</td>
      <td>North Station</td>
      <td>Haymarket Square</td>
      <td>26.0</td>
      <td>1.0</td>
      <td>c2d88af2-d278-4bfd-a8d0-29ca77cc5512</td>
      <td>lyft_luxsuv</td>
      <td>Lux Black XL</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.44</td>
      <td>Lyft</td>
      <td>1.543460e+12</td>
      <td>North Station</td>
      <td>Haymarket Square</td>
      <td>9.0</td>
      <td>1.0</td>
      <td>e0126e1f-8ca9-4f2e-82b3-50505a09db9a</td>
      <td>lyft_plus</td>
      <td>Lyft XL</td>
    </tr>
  </tbody>
</table>
</div>






