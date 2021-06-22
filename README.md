# You-tube-Analysis
Importing some packages
First, we import some Python packages that will help us analyzing the data, especially pandas for data analysis and matplotlib for visualization
![image](https://user-images.githubusercontent.com/77747784/122914350-2f6ad980-d378-11eb-9ac6-e95e7613da3b.png)
Reading the dataset
Then we read the dataset file which is in csv format and getting a feel of our dataset by displaying its first few rows
![image](https://user-images.githubusercontent.com/77747784/122914466-4c071180-d378-11eb-9518-4379d98816a1.png)
![image](https://user-images.githubusercontent.com/77747784/122914507-575a3d00-d378-11eb-8e5e-21cde4f3baa4.png)
![image](https://user-images.githubusercontent.com/77747784/122914611-6fca5780-d378-11eb-83df-ff0c80a08aac.png)
Data Cleaning:
![image](https://user-images.githubusercontent.com/77747784/122915187-1e6e9800-d379-11eb-99d8-186ea2fb4337.png)
![image](https://user-images.githubusercontent.com/77747784/122915242-2c241d80-d379-11eb-92c7-4d99aa4d77b9.png)
![image](https://user-images.githubusercontent.com/77747784/122915285-37774900-d379-11eb-90f4-ebf65c88feb0.png)
![image](https://user-images.githubusercontent.com/77747784/122915321-452cce80-d379-11eb-9a13-01efd3037a59.png)
![image](https://user-images.githubusercontent.com/77747784/122915373-51b12700-d379-11eb-89c2-5c888b953e63.png)
We can see that the number of trending videos published on Sunday and Saturday are noticeably less than the number of trending videos published on other days of the week.


![image](https://user-images.githubusercontent.com/77747784/122915424-5d9ce900-d379-11eb-9cbe-9dae59541454.png)
We can see that the period between 2PM and 7PM, peaking between 4PM and 5PM, had the largest number of trending videos. We notice also that the period between 12AM and 1PM has the smallest number of trending videos. But why is that? Is it because people publish a lot more videos between 2PM and 7PM? Is it because how YouTube algorithm chooses trending videos?
![image](https://user-images.githubusercontent.com/77747784/122915471-68f01480-d379-11eb-8869-a5baec0a2957.png)
![image](https://user-images.githubusercontent.com/77747784/122915531-75746d00-d379-11eb-9791-90e778e68330.png)
we can see that some videos trended on the same day they were published and for some videos it took 4214 days to trend after being published.

Description of numerical columns
Now, let's see some statistical information about the numerical columns of our dataset
![image](https://user-images.githubusercontent.com/77747784/122915568-7f966b80-d379-11eb-8b57-0b43f2036ee8.png)
We note from the table above that:
The average number of views of a trending video is 2,360,784.
The median value for the number of views is 681,861, which means that half the trending videos have views that are less than that number, and the other half have views larger than that number.
The average number of likes of a trending video is 74,266, while the average number of dislikes is 3,711. The Average comment count is 8,446 while the median is 1,856
How useful are the observations above? Let's examine more.
![image](https://user-images.githubusercontent.com/77747784/122915615-8b822d80-d379-11eb-9291-e11b04254b02.png)
![image](https://user-images.githubusercontent.com/77747784/122915655-99d04980-d379-11eb-98a8-23de1388208b.png)
![image](https://user-images.githubusercontent.com/77747784/122915691-a8b6fc00-d379-11eb-9263-d71e8882f74c.png)
![image](https://user-images.githubusercontent.com/77747784/122916520-9c7f6e80-d37a-11eb-8c3a-187e7cd9a552.png)
![image](https://user-images.githubusercontent.com/77747784/122916581-ad2fe480-d37a-11eb-8cb5-f83985de35a4.png)
![image](https://user-images.githubusercontent.com/77747784/122916643-bc169700-d37a-11eb-86b0-e00421e7e283.png)
![image](https://user-images.githubusercontent.com/77747784/122916678-c6389580-d37a-11eb-8744-dd7c6711ee36.png)
we can infer that majority of the videos that trend have 2 million views or less, 400k or less likes,2000 or less dislikes, 5000 comments or less and 15 or less days were taken for a video to trend
![image](https://user-images.githubusercontent.com/77747784/122916704-d0f32a80-d37a-11eb-81ad-a9be29c0a6d1.png)
![image](https://user-images.githubusercontent.com/77747784/122916745-dd778300-d37a-11eb-9d60-5ab217cb4555.png)
there is s strong linear relation between the no of views and the no of likes on a video. We see that views and likes are truly positively correlated: as one increases, the other increases too—mostly.
![image](https://user-images.githubusercontent.com/77747784/122916818-eec08f80-d37a-11eb-9981-481a1ae90d85.png)
![image](https://user-images.githubusercontent.com/77747784/122916919-0dbf2180-d37b-11eb-9763-0e6fc816ee8b.png)
We made a new column 'category_name' containing the coressponding name of the category of the video
![image](https://user-images.githubusercontent.com/77747784/122916983-23344b80-d37b-11eb-9322-93f7c66b1025.png)
![image](https://user-images.githubusercontent.com/77747784/122917009-2deee080-d37b-11eb-9dd9-8291bed5f86d.png)
We see that the Entertainment category contains the largest number of trending videos with around 10,000 videos, followed by Music category with around 6,200 videos, followed by How to & Style category with around 4,100 videos, and so on.
![image](https://user-images.githubusercontent.com/77747784/122917103-452dce00-d37b-11eb-80bc-8eb0c561d68e.png)
![image](https://user-images.githubusercontent.com/77747784/122917181-5c6cbb80-d37b-11eb-9061-362c7c478e39.png)
Music and Entertainment has more likes

Describe non numerical columns:
![image](https://user-images.githubusercontent.com/77747784/122917262-773f3000-d37b-11eb-9144-0b341ceab16c.png)
There are 6351 unique video IDs, we expect to have 6351 unique video titles also, because we assume that each ID is linked to a corresponding title. One possible interpretation is that a trending video had some title when it appeared on the trending list, then it appeared again on another day but with a modified title. Similar explaination applies for description column as well.

To verify our interpretation for title column, let's take a look at an example where a trending video appeared more than once on the trending list but with different titles
![image](https://user-images.githubusercontent.com/77747784/122917341-8d4cf080-d37b-11eb-973b-3b8f22662062.png)
![image](https://user-images.githubusercontent.com/77747784/122917431-a35ab100-d37b-11eb-8d3e-a0826665aa1c.png)
How many trending videos have capitalised word?
![image](https://user-images.githubusercontent.com/77747784/122917530-c4230680-d37b-11eb-874d-faa3894ebbcd.png)
![image](https://user-images.githubusercontent.com/77747784/122917617-d7ce6d00-d37b-11eb-84fc-83043fc2568d.png)
We can see that 44% of trending video titles contain at least a capitalized word.

Video title lengths
Let's add another column to our dataset to represent the length of each video title, then plot the histogram of title length to get an idea about the lengths of trending video titles
![image](https://user-images.githubusercontent.com/77747784/122917685-e87ee300-d37b-11eb-905d-ceb600d2bc36.png)
we can see that distribution is normal max between 30 to 60
![image](https://user-images.githubusercontent.com/77747784/122917772-02202a80-d37c-11eb-9281-de9c57e534d8.png)
![image](https://user-images.githubusercontent.com/77747784/122917824-1106dd00-d37c-11eb-8b4e-bbf7c1b2d4ba.png)
By looking at the scatter plot, we can say that there is no relationship between the title length and the number of likes.
![image](https://user-images.githubusercontent.com/77747784/122917929-30056f00-d37c-11eb-8a2f-f8722143c2b6.png)
How many trending videos have an error?
![image](https://user-images.githubusercontent.com/77747784/122918008-44e20280-d37c-11eb-8cac-9162c0b91350.png)
![image](https://user-images.githubusercontent.com/77747784/122918059-56c3a580-d37c-11eb-9b85-7f99ac2c604c.png)
how many trending videos have their rating disabled?
![image](https://user-images.githubusercontent.com/77747784/122918131-6e029300-d37c-11eb-89b8-020c1011e345.png)
How many videos have both ratings and comments disabled?
![image](https://user-images.githubusercontent.com/77747784/122918219-870b4400-d37c-11eb-9db7-259e9cbe4ed6.png)
![image](https://user-images.githubusercontent.com/77747784/122918307-99857d80-d37c-11eb-83c8-0a55ca4d628a.png)
![image](https://user-images.githubusercontent.com/77747784/122918352-a86c3000-d37c-11eb-9bde-2b92622669e2.png)
![image](https://user-images.githubusercontent.com/77747784/122918394-b621b580-d37c-11eb-8d65-b5773aa7eb8a.png)
![image](https://user-images.githubusercontent.com/77747784/122918442-c2a60e00-d37c-11eb-9be7-53e38c0cd604.png)
![image](https://user-images.githubusercontent.com/77747784/122918490-cfc2fd00-d37c-11eb-8079-ab0343abfcbe.png)
![image](https://user-images.githubusercontent.com/77747784/122918542-dcdfec00-d37c-11eb-9bfe-939801865d0e.png)
![image](https://user-images.githubusercontent.com/77747784/122918593-ebc69e80-d37c-11eb-9ae9-db7b90b61cd0.png)
![image](https://user-images.githubusercontent.com/77747784/122918666-fb45e780-d37c-11eb-9522-82a2dda533d9.png)
Conclusion:we get r-squared score of 0.89 which is pretty good.





















