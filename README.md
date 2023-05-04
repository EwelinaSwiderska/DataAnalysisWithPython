<h1>Data Analysis with Python</h1>

- <b>[Google Colab link](https://colab.research.google.com/drive/1grr09SNb9j_OV9lqfyjsgdCE62BgOOVp?usp=sharing)</b>


<h2>Description</h2>
<br> I have been given 3 different data files(excel, csv, json) from Camdens Council about trees and their environment in the local area to determine if they can create 3 new initiatives: 
    <br> * List of all trees in the borough<br/>
     * Series of “Tree Walks” brochures with informations about interesting trees and parks locations in the area
     <br>* Enviroment Report of the total carbon and pollution benefit provided by all their trees with information about trees removed, trees planted and the net carbon and pollution impact of this activity</br>
<br><br/>
<b>Additional informations: </b>
<br><br/>
<br> * Trees data set is for public use and owned by Council(downloaded from website, excel file)<br/>
* Common Names data set is for public use and owned by Holiticultural Website(scraped from website, json file)
<br> * Environment data set is for internal use and owned by Council(extracted from database, csv file) <br/>

<br />

<h2>Analysis walk-through:</h2>

<p align="left">
<br <h3> ⇨ Uploading three different data files(excel/ csv/ json) to our notebook and performing some simple checks(head/ shape/ columns/ dtypes) using Pandas Library with each data set to gain some knowlage about our data <br/>
<br></br>
<img width="1349" alt="Screenshot 2023-04-28 at 15 31 20" src="https://user-images.githubusercontent.com/129959595/235176262-443494ea-a1d1-4401-a34f-1188a9f894cf.png">
<img width="1313" alt="Screenshot 2023-04-28 at 15 31 48" src="https://user-images.githubusercontent.com/129959595/235176344-c9560e4c-8846-402c-884d-6533550100f3.png">
<img width="1372" alt="Screenshot 2023-04-28 at 15 29 34" src="https://user-images.githubusercontent.com/129959595/235176440-4579b109-832f-462e-b3f7-930d6321cd32.png">
<img width="1348" alt="Screenshot 2023-04-28 at 15 30 15" src="https://user-images.githubusercontent.com/129959595/235176487-c137c8e1-c43c-4a15-bcfc-74429a7ce2ee.png">
<br></br>
<br />
<br />
⇨ Performing further data checks (value_counts/ describe/ unique) to understand with what kind of data we'll dealing - qualitative(nominal/ ordinal/ binary) or quantitative (discrete/ continous). Wider check of our float data types to look for missing values. Classifying data type in all columns from all data sets <br/>
<br></br>
<img width="1145" alt="Screenshot 2023-04-28 at 15 43 27" src="https://user-images.githubusercontent.com/129959595/235179310-42a150bb-11a4-4a03-ac1b-212be9c5ed6f.png">
<img width="1091" alt="Screenshot 2023-04-28 at 15 43 55" src="https://user-images.githubusercontent.com/129959595/235179344-02972f53-a83a-41a9-b22d-a08634c9d9e9.png">
<img width="985" alt="Screenshot 2023-04-28 at 15 45 01" src="https://user-images.githubusercontent.com/129959595/235179377-4011afbe-4bc8-41e0-a761-f15a3f96c5e5.png">

<br></br>
⇨ Checking all data sets for nulls and zero values to find out how big of a problem we having with missing values  <br/>
<br></br>
<img width="1080" alt="Screenshot 2023-04-28 at 15 50 06" src="https://user-images.githubusercontent.com/129959595/235180593-815d4568-ef77-4cb6-8e71-9576af46006a.png">
<img width="1005" alt="Screenshot 2023-04-28 at 15 50 24" src="https://user-images.githubusercontent.com/129959595/235180625-6373894d-dc1d-48d9-a51b-f7356c96af0e.png">
<br><br/>

⇨ Identifying crazy outliers in all datasets using boxplot to check potential errors  <br/>
<br></br>
<img width="1134" alt="Screenshot 2023-04-28 at 15 52 39" src="https://user-images.githubusercontent.com/129959595/235181179-1773c07a-b9dd-4038-94fb-bba09f9c6e84.png">
<img width="1217" alt="Screenshot 2023-04-28 at 15 52 54" src="https://user-images.githubusercontent.com/129959595/235181213-683b3274-5da4-4769-b4d7-7690d3a526d3.png">

<br></br>
⇨ Identifying duplicates  <br/>
<br></br>
<img width="1245" alt="Screenshot 2023-04-28 at 15 55 51" src="https://user-images.githubusercontent.com/129959595/235181935-5b982a3a-954c-4d47-b21a-335ea0853f3d.png">


<br></br>
⇨ Identifying geolocation issues to find data for trees outside our area  <br/>
<br></br>
<img width="973" alt="Screenshot 2023-04-28 at 15 57 52" src="https://user-images.githubusercontent.com/129959595/235182581-5ed97fa0-69ea-4e52-970f-c519615a6159.png">
<img width="979" alt="Screenshot 2023-04-28 at 15 58 06" src="https://user-images.githubusercontent.com/129959595/235182619-018ac597-1f11-45f2-8a99-0bdb1bd44bc1.png">
<img width="1080" alt="Screenshot 2023-04-28 at 15 58 28" src="https://user-images.githubusercontent.com/129959595/235182769-6bc06e56-496a-4f20-9653-3133570b0ce1.png">
<img width="1030" alt="Screenshot 2023-04-28 at 15 58 44" src="https://user-images.githubusercontent.com/129959595/235182798-c40e046c-1eb2-4ff3-b0e0-2506ae35c92d.png">



<br></br>
⇨ Identyfying unmatched data to find trees without matching environmental data <br/>
<br></br>
<img width="1042" alt="Screenshot 2023-04-28 at 16 01 46" src="https://user-images.githubusercontent.com/129959595/235183627-82de2a95-8f9f-4c8e-875c-d8bb7baa23af.png">
<img width="952" alt="Screenshot 2023-04-28 at 16 02 00" src="https://user-images.githubusercontent.com/129959595/235183662-920ea071-3769-4614-8a63-427f5f99bdbb.png">
<img width="1024" alt="Screenshot 2023-04-28 at 16 02 21" src="https://user-images.githubusercontent.com/129959595/235183724-198e3164-d3b6-426b-8f56-6ca576c2c49c.png">
<img width="938" alt="Screenshot 2023-04-28 at 16 02 32" src="https://user-images.githubusercontent.com/129959595/235183753-89d50266-44c4-4faa-b7bf-7c89ee1d56ff.png"></b></h2>
<br></br>
<h2>Conclusions: </h2> <br/>
<br> ✔️ Problem with Data Quality (lots of missing values, outliers which we can classify like errors, some duplicated data, unmached data within data sets)</br>
<br> ✔️ Problem with Data Sensitivity(data scraped from website without permission, data from council databases for internal use)</br>
<br> ✔️ Not enough informations to complete cauncil initiatives(about park locations, interesting or planted trees) </br>
<br></br>
<h2>Additional knowlege:</h2>
<br> ✔️ Importance of Data Quality</br>
<br> ✔️ Importance of Data Sensitivity and Ownership</br>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
