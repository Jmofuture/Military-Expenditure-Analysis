# Military Expenditure Analysis
### Analysis of military expenditures of more than 150 countries between 1960 and 2019 expressed in U.S. dollars.

Data transformation using Power Query Editor functions to create dashboard-type reports.


### Power Query transformations

- We load the dataset data into PowerBi.
- The table contains blank columns and rows so we have to clean the data and delete what is not useful for Power Query.

![image](https://user-images.githubusercontent.com/78714438/168499907-6552c4ba-ed6a-4bb6-a9c0-a289317941fb.png)

- The first 3 columns and the first two rows are deleted.
- The first row is assigned as header to obtain the column headings.
- We must fill in the continent data since we only have it in the first row corresponding to its countries.

![image](https://user-images.githubusercontent.com/78714438/168499959-1b07b921-1662-4232-a249-8da6165a1070.png)

![image](https://user-images.githubusercontent.com/78714438/168499965-170d5a3a-3673-41b9-bbee-c8993242a3de.png)

- We separate the country code from the name.

![image](https://user-images.githubusercontent.com/78714438/168500002-b9683eed-d2cf-4bbc-a64f-c12dd9531ec8.png)

- We divide the code by custom delimiter, in this case we observe that all have a (space - space), so that will be the pattern that we will go to separate both data, taking from the left of the text.

![image](https://user-images.githubusercontent.com/78714438/168500079-ab4a25eb-b279-4bc7-95fb-24d1efb61f1c.png)

- Now we must remove the parentheses from the country name.

![image](https://user-images.githubusercontent.com/78714438/168500086-dd79e76b-1efe-4e8f-94cf-af7cf413e894.png)

- We use the function extract text between delimiters, in transform data so that it does not create another column.

![image](https://user-images.githubusercontent.com/78714438/168500098-da1bfd36-456c-4013-94f4-964ad25809a3.png)

![image](https://user-images.githubusercontent.com/78714438/168500106-70280281-5e27-450c-8b6b-f49fe1e5584d.png)

- Now we must summarize the columns of the years, since having a single column per year makes it impossible to work with the data in this way, so we will use the function Override column dynamization.

![image](https://user-images.githubusercontent.com/78714438/168500121-e245949f-c554-45e0-b3b2-99e7063a8f95.png)

![image](https://user-images.githubusercontent.com/78714438/168500126-e94688f9-ab20-4a64-8af7-2ee18a3f576b.png)

- We rename the column headings.

![image](https://user-images.githubusercontent.com/78714438/168500133-3731655c-f8c8-4e01-ac08-5c50714d0e3d.png)


![image](https://user-images.githubusercontent.com/78714438/168500137-f0ff9627-db06-4128-8a76-110e01bce364.png)

- Assign the data type in the Expense column to "Currency".

![image](https://user-images.githubusercontent.com/78714438/168500161-59682a65-8344-4d9f-a6f5-923853c33b5c.png)

The others, being descriptive, remain as text.

- We added a conditional column to create categories based on the amount of the expense.

![image](https://user-images.githubusercontent.com/78714438/168500188-efdd2738-1e92-4805-8aa7-0917c5cc99ad.png)

![image](https://user-images.githubusercontent.com/78714438/168500192-86f6f489-dda9-4fd4-a3fe-e1c1c4a128f3.png)

- We added another data source to organize the groups by amount of income by country.

![image](https://user-images.githubusercontent.com/78714438/168500207-06052514-3396-49b9-8010-b8ebf0ed0064.png)

- As they are related by country code, Power Bi makes the relationship automatically. 

![image](https://user-images.githubusercontent.com/78714438/168500224-d7488170-edb2-4f30-a616-a09c8cf1b255.png)


## Power BI

- We adjust the category of the continent and country columns to location references. 

![image](https://user-images.githubusercontent.com/78714438/168500405-29ff3bae-f075-475b-86db-f7665fa12cc3.png)

- Four filters were added:
- By continent

![image](https://user-images.githubusercontent.com/78714438/168500652-9ed3401a-11ec-4dcb-ac26-2f620c02200b.png)

- By expense group

![image](https://user-images.githubusercontent.com/78714438/168500701-cc06c726-2f3e-4975-8f17-723db7e27867.png)

- By income group

![image](https://user-images.githubusercontent.com/78714438/168500736-b160fec9-cc25-4a08-ba61-76aacc1a98a1.png)

- By year, from 1960 to 2018

![image](https://user-images.githubusercontent.com/78714438/168500786-e860ac63-bb43-4382-a837-8d8714c44739.png)






