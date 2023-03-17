# FIFA-21-DATA-CLEANING-PROJECT-USING-POWER-QUERY

![Data cleaning image](https://user-images.githubusercontent.com/81152387/225836331-a84420c8-33de-45a4-b338-ae136a1793d7.png)

**Introduction**

I recently hopped on a data cleaning challenge organized by some amazing individuals in the tech space which provides intermediate learners like me the opportunity to work on a data cleaning project. We were asked to use any preferred tool for the task e.g. (Power Query, Excel, Python, SQL, R etc). I used power query editor in Microsoft excel for the task.

**About the data**

The dataset used for the project is the FIFA 21 data set and it contains information about the players, as well as various statistics and attributes associated with each player. The dataset also contains a wide range of variables, including player attributes such as speed, dribbling, shooting, passing and overall rating to mention a few. A file which incudes a dictionary to gain an understanding of every entry in the data set was also included with the data file.

**Data Cleaning Process**

![data cleaning cycle](https://user-images.githubusercontent.com/81152387/225840696-c0ed8ff4-2a55-48b8-85bb-4a560a1e27c3.jpeg)


After loading the data, I looked through to identify columns that needs cleaning like the name, contract, wage, value, height etc. and also took note of some that are not important for the purpose of this analysis which will be deleted to give a clean data set. The unwanted columns were deleted e.g. the player url and photo url columns.

The first thing i did was to remove the space in between the columns and this was achieved by trimming the club column to remove the wide space.

![club](https://user-images.githubusercontent.com/81152387/225837678-5b5e0dd8-7247-4875-89fd-1dfc7f90c398.jpg)

The Name and LongName columns have some special characters that could neither be analyzed nor useful for the purpose of the analysis such as @, ? , / and so on. To remove them from the dataset, I changed the file origin from western European (Windows) to Unicode (UTF-8).

![name complete](https://user-images.githubusercontent.com/81152387/225837870-9b283d89-57c9-4f09-8be9-309e78e13d9e.jpg)

The players Overall (OVA) and Potential (PO) rating columns should be measured in percentage so I divided the columns by 100 and changed the data type to percentage.

![ova](https://user-images.githubusercontent.com/81152387/225838066-17b8e60c-7a3a-4fa9-8408-72832cdcb11b.PNG)

The contract column was splitted with conditional column to separate the contract start and end dates and as well as to get the contract duration and contract agreement whether it's free, on contract or on loan. These columns created are very useful at the analyzing stage for various decision making.

![contract complete](https://user-images.githubusercontent.com/81152387/225838196-bd614a41-33dd-4853-9386-f6a82c3ecc0c.jpg)

The height and weight columns are expected to be measured in cm and lbs respectively so for the weight column, it  was splitted with conditional column to separate the kg and lbs and to get everything to be in lbs, the kg column was multiplied by 2.205 which is the standard conversion from kg to lbs. The height column was also splitted with conditional column and the measurement in feets were converted into cm by multiplying the values in inch by 2.54.

![height complete](https://user-images.githubusercontent.com/81152387/225838659-06f476df-7312-47b9-a53d-89d4c0683fd8.jpg)

The special character in the wage, value, release clause columns were removed with find and replace and the currency column were expected to be in represented in dollars so the average euro to USD exchange rate of 1.183 was used to multiply the wage, values and release clause columns to give the exact values in dollar. The data type was changed to currency. The Euro special character was removed with find and replace.

![wages complete](https://user-images.githubusercontent.com/81152387/225838796-c666725e-5e0f-4288-bef5-709ee052f9c1.jpg)

The hits column which is the number of times a player's profile was viewed has some special character and some players has over a thousand views and this was represented by K. I removed the K with find and replace and multiplied the K values by 1000 using conditional column.

![hit complete](https://user-images.githubusercontent.com/81152387/225838920-d9c8d42f-72b9-46fe-8c2c-f30a74c5c72d.jpg)

The weak foot, skill moves and injury rating columns have some star symbol in them and this was removed with find and replace.

![star com](https://user-images.githubusercontent.com/81152387/225839030-16556ec2-1b63-4f1e-8cd9-5a2bc762b8fe.jpg)

**Conclusion**

Hearing about this data cleaning challenge and putting all the works is the best decision i made in recent time as it has opened new way to tackle messy data set. I also learnt new concepts and procedures.

The hallmark of a quality data which are consistency, completeness, accuracy and validity were followed to get a clean data set.

I am open to reviews and feedbacks. 

You can reach out to me on Twitter https://twitter.com/DollyJide?t=tipDIB49oMMWCm5WAJIhwA&s=09 and also on Linkedin https://www.linkedin.com/in/dolapo-kenny-jide-284a16208
 
Thank you.
