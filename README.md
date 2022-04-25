# Consulting-assignment-for-Insaid-Telecom
* In this project Insaid Telecom is seeking to leverage behavioral data from more than 60% of the 50 million mobile devices active daily in India to help its clients better understand and interact with their audiences. 
* In this consulting assignment, we are performing EDA to understand user's demographic characteristics based on their mobile usage, geolocation, and mobile device properties.
*  Doing so will help millions of developers and brand advertisers around the world pursue data-driven marketing efforts which are relevant to their users and catered to their preferences.
## Data Description:
gender_age_train - Devices and their respective user gender, age and age_group

phone_brand_device_model- device ids, brand, and models phone_brand: note that few brands are in Chinese

Brand Name Brand English Mapping '华为' 'Huawei' '小米' 'Xiaomi' '三星' 'Samsung' 'vivo' 'vivo' 'OPPO' 'OPPO' '魅族' 'Meizu' '酷派' 'Coolpad' '乐视' 'LeEco' '联想 ' 'Lenovo' 'HTC' 'HTC'

events_data - when a user uses mobile on INSAID Telecom network, the event gets logged in this data. Each event has an event id, location (lat/long), and the event corresponds to frequency of mobile usage. timestamp: when the user is using the mobile.
![image](https://user-images.githubusercontent.com/97185610/165026549-407409b6-8cc4-4a00-bb28-d66e41710ae4.png)
## Introduction:

InsaidTelecom, one of the leading telecom players, understands that customizing offering
is very important for its business to stay competitive. Currently, InsaidTelecom is seeking to leverage behavioral data from more than 60% of the 50 million mobile devices active daily in India to help its clients better understand and interact with their audiences.
## Project Description:

We are building a project to understand users' demographic characteristics based on their mobile usage, geolocation, and mobile device properties. Doing so will help millions of developers and brand advertisers around the world pursue data-driven marketing efforts which are relevant to their users and catered to their preferences. Our Focused States are Arunachal Pradesh, Chandigarh, Manipur, Tamil Nadu, Tripura, Uttar Pradesh.
## Problem Statement:

a)	Business Problem Statement: User behavior across the focused State, which is going to directly impact the company's offerings. To deploy the right way forward and suggest actionable insights from marketing and product terms.

b)	Dataset Problem Statement: We faced challenges with missing data in geolocations, device ids, handset names in Chinese language in the database, multiple tables with segmented data which were very important for getting the right insights. We were required to get a consolidated, curated data set and then apply the EDA steps to generate insights.

## Problem Analysis (Strategy for the Problem Statement analysis):

##### a.	Understanding the Problem statement -

Understanding the activity that InsaidTelecom data project is given to us, which is the key to ensure the result is achieved with collaboration of the different Team members. Before thinking about the data, we have long discussions with the team about process, responsibility, timelines etc.  This was the kickstart of our data initiative.

##### b.	Getting data in python Notebook - 

We have connected with MySQL to get the data for gender and Brands and upload CSV file for event data.

##### c.	Exploring and Cleaning data - 

We have started digging the data to see what we got and how we can link everything together to achieve our original goal. We have started taking notes on our first analyses and asked questions within the team to understand what all our variables mean. We started cleaning the data like filling the missing values, converting float into integer, converting absolute values, changing names from Chinese to English etc.

##### d.	Enriching Dataset - 

Now that we have clean data, it’s time to manipulate it to get the most value out of it. We have started the data enrichment phase of the project by joining all your different sources and group logs to narrow our data down to the essential data series. We have enriched our data by creating merged dataset, converting timestamp into date and time, extracting focused state for consulting etc.

##### e.	Building helpful visualizations (EDA) - 

Now we have a nice dataset, we started exploring it by building graphs. Visualization is the best way to explore and communicate our findings and is the next phase of your data analytics project. This helps us to enrich our dataset and develop more interesting findings. For example, by putting our data points on a map we could perhaps notice that specific geographic zones have more usage/users/brands than specific states or cities.

## Sources of Data (Explanation about database connection, tables, and their columns) :

##### a)	Connecting with MYSQL database server to get the gender and phone brand files.

a.	gender_age_train - Devices and their respective user gender, age, and age groups

b.	phone_brand_device_model - device ids, phone brand, and phone models: note that few brands are in Chinese

##### b)	Downloading the CSV file for event data

a.	events_data - when a user uses mobile on INSAID Telecom network, the event gets logged in this data. Each event has an event id, location (lat/long), and the event corresponds to frequency of mobile usage. timestamp: when the user is using the mobile.

## Summary of Data Preprocessing : (Challenges faced with the Data and how we resolved them)
	
data taking device id as reference and using merge function with “inner”. 
Challenges  | Resolution
------------- | -------------
Missing values in State data series  | Replaced with mode with reference to City data series
Missing latitude  | longitude data series	Replaced with mode with reference to City data series
Negative values for Device id data series | Made all the device id positive using absolution function
Data type of device id is found to be float in CSV data, whereas it is int in SQL file | Converted device ids in all the database as int64
Timestamp contains both date and time | We have split the date and time with 2 different data series
Chinese names in Phone Brand data series| Converted into English names with reference to respective Chinese name by creating dictionary
Merging data set	| We have merged data taking device id as reference and using merge function with “inner”

## Description Analysis in Details(EDA) :
Exploratory Data Analysis | Outcome(Focused State)
------------- | -------------
Distribution of Users(device_id) across States.  | Highest no. of Users (device_id) found in TAMILNADU with 44 nos.
Distribution of Users across Phone Brands (Consider only 10 Most used Phone Brands)  | Highest no. of Users is having SAMSUNG as Phone Brand with 22 nos.
Distribution of Users across Gender | 43 nos. of MALE users and 27 nos. of FEMALE users found in our consulting States
Distribution of Users across Age Segments | Highest no. of users is coming under the age segment of M 39+ with 10 unique users
Distribution of Phone Brands (Consider only 10 Most used Phone Brands) for each Age Segment, State, Gender | Age Segment: SAMSUNG is the most used Brand (4 nos.) which is present under the Age segment FEMALE 27-28. 

State: SAMSUNG is most used in the State TAMILNADU with 13 users.

Gender: SAMSUNG is used by most of the FEMALES gender with 13 users. 



We have analyzed the data based on following EDA points:


## Tools : DS Tools used :

We have used the following DS Tools 
a)	Jupyter Notebook / Google Collab

b)	Python  (Library : Panda, Pandas_Profiling, Numpy, Matplolib, Seaborn, Sweetviz,Folium, Geopandas) 

c)	SQL and Excel

## Suggestions on the basis of Analysis :

a.	TAMIL NADU has the most users in both MALE and FEMALE. We recommend clients to focus more on TAMIL NADU in our state group.

b.	SAMSUNG is the most used brand in focused States. Clients can make combo offers of their call plan with new users who purchase SAMSUNG brand mobile.

c.	Most people are active between 11 -12 pm in most of the States. Clients can run the promotions activity in this hour.

d.	M39+ is the Age segment with maximum users. Clients can propose unique propositions for the segment. We can promote OTT content like Netflix, Hotstar, Amazon Prime etc. to generate additional revenue.

