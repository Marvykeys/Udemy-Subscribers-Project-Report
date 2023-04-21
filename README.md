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
 ## Data Cleaning 
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
