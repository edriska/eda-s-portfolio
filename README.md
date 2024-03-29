# Eda's portfolio's

## Projects:

- [Analyze booking.com reviews](#hotel-reviews) (keywords: AI, Azure Cognitive Services, Azure Blob, Power Bi)
- [Dashboard for Sailrace](#sail-race) (keywords: IOT Device, SQL Server, Azure Event Hub, Azure Analytics Jobs, Power Bi)
- [Simple time-series analysis for influenza data set](#simple-time-series)  (keywords:Power Bi. time-series)



## Hotel reviews

![report-page1](https://github.com/edriska/eda-s-portfolio/assets/103993701/f2ded5a8-6f0b-4010-b3f7-6b00aa208995)
In that business case; the challenge was handling a dataset comprised entirely of free text, I employed an Azure AI solution, specifically the Azure Cognitive Sentiment Analysis feature. This tool allowed me to determine sentiment scores, distinguishing between positive and negative comments.

To delve deeper into customer feedback on hotels, I focused on discerning impressions related to food and cleaning. I curated a keyword list and systematically applied it to the comments, counting the frequency of specific terms. I then crafted a DAX query to quantify these keyword mentions.

Subsequently, I organized the insights into two distinct calculated tables—one for food-related comments and another for cleaning. This facilitated a detailed analysis of sentiment trends across different years. The dataset was sourced from booking.com, accessed through Azure Blob.

This approach not only streamlined the handling of unstructured data but also provided valuable insights into customer sentiments. Combining sentiment analysis with keyword frequency assessments enabled the creation of meaningful tables, offering a comprehensive exploration of customer complaints related to food and cleaning over various years. Utilizing Azure AI tools enhanced the efficiency of the analysis, making it a robust and insightful process.

![hotel-names-by-food-9](https://github.com/edriska/eda-s-portfolio/assets/103993701/28efd120-6b94-4365-9361-89a88af77435)
![hote-lnames-by-cleaning-8](https://github.com/edriska/eda-s-portfolio/assets/103993701/4b0b0157-9d21-4015-b539-34cfb859685e)
![goodfood5](https://github.com/edriska/eda-s-portfolio/assets/103993701/4f0aa6a1-d469-4963-b4be-f6bb8e8eb065)
![goodcleaning7](https://github.com/edriska/eda-s-portfolio/assets/103993701/40a01cc7-d592-4441-b84a-499edb8d3419)
![foodkeywords2](https://github.com/edriska/eda-s-portfolio/assets/103993701/7171850d-090d-4e26-a061-dae0e38aef07)
![complainfood4](https://github.com/edriska/eda-s-portfolio/assets/103993701/66521a9a-9106-488d-8fc3-6b23a62f1a48)
![complaincleanin6](https://github.com/edriska/eda-s-portfolio/assets/103993701/8eb2a5b4-bcab-4091-b311-ef5df5d0a71d)
![cleankeywords3](https://github.com/edriska/eda-s-portfolio/assets/103993701/e64a3df3-bfa7-4a23-8755-efc018b24279)

## Sail Race 

The second business case is about a sailing race in that challenge I should create a dashboard and show each boat current location and show the boats current location and rank by the boat challenge was made a lambda architecture, used the Event hub, and streamed the analysis to the Power Bi dashboard and it should be figured out what should I do batch processing part I used in that part SQL database and make my analysis in there wrote a SQL codes in the Event hub calculated the distance and ranked the boats by distance also I want to rank by speeds and want to see rank differences between them. In that business case, you can see how did write SQL code and make a pipeline from scratch using Azure Stream Analytics Job.

![Vendee Globe Report (1)](https://github.com/edriska/eda-s-portfolio/assets/103993701/c2c9e05d-5649-40a3-97f6-e5b3888a46fd)
![Screenshot_20221221_150601](https://github.com/edriska/eda-s-portfolio/assets/103993701/b66c5f58-dd44-443f-8298-46033a3d5b42)
![Screenshot_20221221_150538](https://github.com/edriska/eda-s-portfolio/assets/103993701/ac5cd314-1a4d-4c3b-b434-ecec8d0eb374)
![Screenshot_20221221_150510](https://github.com/edriska/eda-s-portfolio/assets/103993701/2a6142b7-ab53-4ca1-97f0-33edac3ba339)
![Screenshot_20221221_150421](https://github.com/edriska/eda-s-portfolio/assets/103993701/8762f49e-f1b5-49f9-9da0-7fb13d1de006)
![Screenshot_20221124_232211](https://github.com/edriska/eda-s-portfolio/assets/103993701/6cd9a125-378b-4730-bd5e-1f9d2a347d7d)


 ## Simple time series
 
 ![Screenshot 2023-12-09 204323](https://github.com/edriska/eda-s-portfolio/assets/103993701/887fa7d2-4cb0-4228-8539-8ec453b17067)
In that analysis ,I used the influenza data set to analyze the occurrence of influenza cases each year to drive vaccination policies and identify the trend. I wrote The Dax to create a new calculated column called "Outbreak Check" that uses the CONTAINSSTRING() function, which marks whether there was an influenza outbreak or not for each row of the data.
The TITLE field contains information on the types of influenza events that occurred, and that is why I  checked if the field has the text "Outbreak".I only want to total the influenza cases when an outbreak occurs and use our newly created Outbreak Check field.
I Plotted the total number of influenza cases over time by the kind of outbreak. care about when the case starts, not how long it lasts.
Used a clustered column chart with the SDATE field on the x-axis (Ensure that you are using the date value and not the date hierarchy)
Filtered the visual to focus on France over the last five years of available data. Note that France only has data until 2015.
after all that analysis we can see Which type of variation we see in this influenza dataset, and when we have a spike in outbreak cases. In that case, we have
Cyclical variation in February that variation means data will have a similar increase or decrease at the same point each year and tends to be over a shorter period
![Screenshot 2023-12-09 204257](https://github.com/edriska/eda-s-portfolio/assets/103993701/e964d7fd-e70e-4e48-9474-c4b88fefbf87)
In that case I  analyzed the variance of birth rates in the countries we operate in to drive policy changes. Work through the dataset provided to see when we expect to insure the most births.
I Plotted the total number of births over time using the Month Year field.
By default, Power BI will visualize this using the built-in Date Hierarchy; I changed this to the Date Value instead.
Filtered the page to only show births in France in the last ten years of available data and found which month had the highest birth rate.
![Screenshot 2023-12-09 191849](https://github.com/edriska/eda-s-portfolio/assets/103993701/67ac7d25-402d-4a6e-86c8-2189c0189400)
