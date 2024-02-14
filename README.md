 # :books:Udemy-Subscribers-Project-Report:books:
 ## Scope :page_with_curl:
 This report is focused on studying the preferences of subscribers, their subscription trends and other useful insights using the provided data on courses from different topics.
 ## Data Design :bar_chart:
 The raw data provided was downloaded in CSV file format which came with some of its contents being incorrect and improperly formatted hence, a proper data cleaning had to be done by removing duplicates, renaming cells, creating filters and also deleting empty rows.
 ## Import and Transform Data :scroll:
 After downloading the data which contained four different CSV files, I imported the data into Microsoft Excel being the tool I’ll be using for analysis. Then I clicked on these in order. (Data > Get Data > From File > From Folder)  
![image](https://user-images.githubusercontent.com/130637591/232629319-b1e58ddd-1929-4074-8299-acd745b0b98d.png)
 ##
Next, I selected the folder in which the file was saved, then I selected the four CSVs. 
A description box popped up with details of the four CSVs and multiple options to click on. I clicked on “Transform Data” because I want to combine all four CSVs into one spreadsheet.  
![image](https://user-images.githubusercontent.com/130637591/232913181-44436f66-ac03-4794-817d-ab3b9d82d8df.png)
 ##
Next, the Microsoft power query editor appears and then I clicked on the two downward arrows on the content column to merge the CSVs.  
![image](https://user-images.githubusercontent.com/130637591/232913302-8ee42a87-aaeb-4f8d-9551-9eff930ebadf.png)
 ##
The “Combine Files” box pops up, I was satisfied with the settings so I clicked OK.  
![image](https://user-images.githubusercontent.com/130637591/232913681-4f8dc48b-ff88-4140-a28e-246bfc1aeb88.png)
 ##
Now, you see below, all four CSVs are joined and the number of rows is now 3,681 rows loaded.                                                                     ![image](https://user-images.githubusercontent.com/130637591/232913848-073975b3-aad0-4bd3-86be-e05cdc9692b5.png)
 ## Data Cleaning :shower:
My first cleaning process was to check for duplicates and remove them. I did this by highlighting the whole data and then clicked on the remove duplicates icon.      
![image](https://user-images.githubusercontent.com/130637591/233659975-c0f0512b-6a71-4236-a45f-5e9840b2e812.png)
 ##
The remove duplicates dialog box appears, then I selected all columns, ticked the box “My data has headers” because my data has got headers, then I clicked OK.            
![image](https://user-images.githubusercontent.com/130637591/233661790-81fb8fad-899b-4a94-9a9c-11f28c35424a.png)
 ##
One duplicate row was found and removed. The previous total rows were 3681, but 3680 rows are now left.                                
![image](https://user-images.githubusercontent.com/130637591/233661962-20130b02-e366-4138-8949-cdb2ff6add32.png)
 ##
My next cleaning process was to filter the data for blank rows and remove them. I used the shortcut Alt + A + T to add a filter, searched for blanks and then clicked OK.      
![image](https://user-images.githubusercontent.com/130637591/233662280-b1ba6d6a-ead8-4073-9847-eb25650d1615.png)
 ##
Now, below are the four empty rows, with just one column having a content. I selected all four empty rows and deleted them.                                  
![image](https://user-images.githubusercontent.com/130637591/233664528-1a5049b5-e8c9-4053-be0a-59be66164ef4.png)
 ##
I found an error on the “Subject” column, which contains four unique subjects, which are “Business Finance”, “Graphic Design”, “Musical Instruments”, “Web Development”. 
“Subject: Web Development” was entered instead of “Web Development”.                                           
![image](https://user-images.githubusercontent.com/130637591/233665038-5f6c9c44-3926-4c1c-a3a4-44681fb876da.png)
 ##
I used the shortcut CTRL + F to bring out the Find & Replace box which I used to  correct the errors and Replaced All.          
![image](https://user-images.githubusercontent.com/130637591/233666892-2af22ec8-12b2-41a9-8cdd-fcaa77a41843.png)
![image](https://user-images.githubusercontent.com/130637591/233666961-09ee93bb-ac45-4f20-922b-40216407f239.png)
 ##
I added a new column, so I could extract only the date from the “Published_TimeStamp” column.                  
![image](https://user-images.githubusercontent.com/130637591/233672288-b3f02846-033e-4bd5-baa5-fc2678914e7c.png)
 ##
I used the =INT() function to convert the value in the “Published_TimeStamp” column which was in text type to integer.          
![image](https://user-images.githubusercontent.com/130637591/233672477-0188b7d9-52e5-4831-9dc5-5630d16cc3be.png)
![image](https://user-images.githubusercontent.com/130637591/233673486-b40b634d-53c5-472e-bc35-4f7529fcc7e8.png)
 ##
Now the column is in Integer format, but I want it in date format. Hence, I formatted the column cells to a Date format.            
![image](https://user-images.githubusercontent.com/130637591/233674675-f965dc27-486c-4894-9f7e-0adc7956d4fd.png)
 ##
Here is how it looks like in Date format.         
![image](https://user-images.githubusercontent.com/130637591/233675107-033313b4-58ac-4c41-8b85-82fdce081942.png)
 ##
I created another column to find out the courses which were Free and the courses which were Paid for using an IF Function. With the Logical statement being If the “Price” column is “0”	 then return “Free” If True and “Paid” If False.             
![image](https://user-images.githubusercontent.com/130637591/233675582-142b98c4-8916-424b-ac8d-b0314e63fe03.png)
 ##
Here are the results of the IF Statement.            
![image](https://user-images.githubusercontent.com/130637591/233675787-0fb9059d-9cfd-4293-a43c-401d38d90161.png)
 ##
Next, I used the VLOOKUP Function to lookup courses from the table for the “Level” they belong to, whether they are “Free_Or_Paid”, the “Content_Duration” and the “Date” they were created.              
![image](https://user-images.githubusercontent.com/130637591/233676002-61eba936-5681-4b3c-9d93-453fe5cd82ce.png)
 ##
An example of what I did was =VLOOKUP(“course_name”,”the_source_table_range”,”the_column_index_in_the_range”,False_exact_match)               
![image](https://user-images.githubusercontent.com/130637591/233676214-4806c526-1cf4-4025-b0db-9a9a3e4f95f0.png)
![image](https://user-images.githubusercontent.com/130637591/233676415-6017b0e1-8ff2-44e6-aa14-4e81e23140df.png)
 ##
For the Date column, it came as an integer.        
![image](https://user-images.githubusercontent.com/130637591/233676606-9ef98dd5-dad4-4da7-a867-d4898c4826ac.png)
 ##
But you can always change to Date Format.                   
![image](https://user-images.githubusercontent.com/130637591/233676827-d385fa1d-61dd-47b7-adc3-86680c67311b.png)
 ##
Here is how the extracted data from the source table looks like using VLOOKUP.              
![image](https://user-images.githubusercontent.com/130637591/233677023-ca721d0f-2b24-47a1-b260-9efbf575a981.png)
 ## PIVOT TABLES FOR SUMMARY STATISTICS :bar_chart:
For multi-conditional calculations, Pivot Tables are a powerful tool and they are faster than using formulas because they take less time to set up than other formula methods.                                                                                                                                                                     
I was looking to answer some questions to gain insight from the dataset. The questions were:                                                                                  

a) What is the total number of recorded subscribers per Subject?                                                                                                                   
b) What is the average number of subscribers per Subject?                                                                                                                         
c) What is the average content duration per Subject?                                                                                                                              
d) What is the average price per Subject in each Level?                                                                                                                           
e) What is the average rating per Subject in each Level?                                                                                                                          

I was able to answer these questions with the use of Pivot Tables.                                                                                                                            
Here are the results from the Pivot Tables, answering the above questions.            
![image](https://user-images.githubusercontent.com/130637591/233677661-d20097f8-72f3-4027-907e-820c5785c756.png)
 ## :bar_chart: INSIGHTS :art:
1. From the analysis completed, Web Development courses has got more subscribers than the other courses with 7,981,935 subscribers recorded.       
![image](https://user-images.githubusercontent.com/130637591/233678140-7e66516a-fc4c-44a7-862e-1f069d8a52df.png)
 ##
2. With an average number of subscribers of 6635 subscribers, the Web Development courses are in high demand compared to the others, this entails that most of the subscribers prefer Web Development courses to others.                                            
![image](https://user-images.githubusercontent.com/130637591/233682344-63a77ed7-448b-450b-8604-9605c5cd605b.png)
 ##
3. As expected, due to previous results, the Web Development courses has got the highest average content duration with over 5 hours of content compared to Graphic Design’s 3 plus hours, Business Finance’s 3 plus hours and Musical Instrument’s 2 plus hours.                    
![image](https://user-images.githubusercontent.com/130637591/233684308-455f0048-86c2-473a-9fb9-dcef50ef73a8.png)
 ##
4. The Web Development courses have got the highest cost in each of the four levels, with $79 at the Beginner, $85 at the Intermediate, $67 at the Expert and $75 at the All Levels.                    
![image](https://user-images.githubusercontent.com/130637591/233684656-d50d2bce-d4f2-4ab5-95e8-f800706fd3ab.png)
 ##
5. Now in ratings, The Graphic design courses come on top with the highest average ratings in each of the four levels. 
Business Finance courses have got the second highest average ratings, Web Development courses have got the third highest average ratings.
Musical Instrument courses have got the lowest average ratings in each of the four levels.                      
![image](https://user-images.githubusercontent.com/130637591/233685183-43cf5899-5082-42d5-bbb8-ce6ccd6634e6.png)
 ## CONCLUSION :spiral_notepad:
With the analysis completed, I was able to gain some insights from the dataset.

The Graphic Design courses are highly rated amongst the others, in each of the four levels on the Udemy Website.

Though with the third highest average ratings, and having the most expensive courses, the Web Development courses are still in high demand.
 ## THE FINAL DASHBOARD :art:
 ![UDEMY SUBSCRIPTION TRENDS DASHBOARD](https://user-images.githubusercontent.com/130637591/c8a2f06c-55e4-4a50-bf7d-cc93962ebc0d.png)

