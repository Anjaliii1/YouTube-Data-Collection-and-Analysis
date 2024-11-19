# YouTube Data Collection and Analysis
This project focuses on collecting and analyzing trending YouTube videos using the YouTube Data API. It includes extracting insights from video metrics and visualizing trends in Trending Videos,view,like,comments etc


### Features

   1. Fetch trending YouTube videos for specific regions using the YouTube Data API.
   2. Analyze video categories, view counts, like counts, and comment counts.
   3. Generate visualizations to uncover trends and patterns.
   4. Clean and preprocess data for meaningful insights.
      
### Technologies Used

 1. Programming Language: Python
 2. Libraries:
     pandas: Data manipulation and analysis.
     matplotlib & seaborn: Visualization.
     googleapiclient: Interact with YouTube Data API.
 3. API: YouTube Data API v3

#### Steps:
 1. Obtaining a YouTube Data API Key:
    - Go to the Google Cloud Console.
    - Click on the project drop-down menu at the top and select "New Project".
    - Enter a project name and click "Create".
    - Navigate to "APIs & Services" > "Library".
    - Search for "YouTube Data API v3", select it, and click "Enable".
    - Go to "APIs & Services" > "Credentials".
    - Click "+ CREATE CREDENTIALS" and select "API Key".
    - Copy the generated API key and save it securely.
2. You will use this API key in the project to authenticate requests to the YouTube Data API. Add the key to the config.py file.
3. The script uses the YouTube Data API to fetch details of the top 200 trending videos in the US, collects various video metrics (e.g., title, description, views, likes), compiles the data into a pandas DataFrame, and saves it as a CSV file for analysis.
The script uses the YouTube Data API to fetch details of the top 200 trending videos in the US, collects various video metrics (e.g., title, description, views, likes), compiles the data into a pandas DataFrame, and saves it as a CSV file for analysis.
4. To quickly assess what the data looks like, you typically examine:

    - Data Preview: Use tools like head() (in Python) or directly view the first few rows to understand the structure.
    - Columns: Look at column names, data types, and overall organization.
    - Summary Statistics: Use functions like describe() to get a sense of distributions, counts, and potential outliers.
    - Missing Values: Identify gaps or inconsistencies in the dataset.
5. This visualization helps us understand how the values for views, likes, and comments are distributed across all videos, highlighting trends and patterns in the data

![image](https://github.com/user-attachments/assets/749cc3c4-cb1b-41dc-9105-7eff5701384c)

  #### The histograms show that the distributions of view counts, like counts, and comment counts are right-skewed, with most videos having lower counts and a few videos having very high counts. 
6. The correlation matrix, visualized using a heatmap, provides insights into the relationships between view count, like count, and comment count for trending videos:

![image](https://github.com/user-attachments/assets/0784aaa4-cb44-48e4-9f0f-c576464fcb8f)

#### The heatmap highlights the interconnected nature of these engagement metrics, reinforcing the idea that higher visibility leads to greater audience interaction across multiple dimensions.
7.  To include the category names along with the category IDs in your analysis of trending videos.
8.  The chart visually represents how trending videos are distributed among categories, with bars indicating the number of trending videos in each category. Categories with more bars are more prominent in trending videos, helping identify which content types dominate trending lists.
  
![image](https://github.com/user-attachments/assets/ce8b057b-a6c2-4a7a-8c1f-92ad0266a998)

#### The bar chart highlights that the Gaming, Entertainment, Sports, and Music categories dominate with the highest number of trending videos. Next, let's analyze the average engagement metrics (such as views, likes, and comments) across different categories to gain deeper insights.
9. The average engagement metrics (views, likes, and comments) for trending YouTube videos by category.
 
![image](https://github.com/user-attachments/assets/0701e8ff-c388-4e44-bdbd-ada3ae6b1045)

#### The categories Music and People & Blogs consistently achieve the highest average numbers for views, likes, and comments. Similarly, the Film & Animation category exhibits significant engagement, particularly in terms of views and likes.
10. We used the isodate library to convert video durations from ISO 8601 format to seconds for numerical analysis. Then, we categorized videos into duration ranges (e.g., 0-5 min, 5-10 min, etc.) by creating a duration_range column. This allows us to analyze engagement metrics (views, likes, comments) across these ranges, providing insights into how video length impacts performance.
11. Scatter Plot: It visualizes the relationship between video length (in seconds) and view count. The plot shows how different video durations correlate with the number of views, with each point representing a video.

![image](https://github.com/user-attachments/assets/30432335-37b0-4a38-b6f8-52cd7e805aa7)

Bar Charts: These display the average engagement metrics (view count, like count, comment count) across different video duration ranges. Three separate bar charts show how video length affects.
View Count
Like Count
Comment Count

![image](https://github.com/user-attachments/assets/4f5a7cc7-9448-4066-958b-e51ca6233328)

#### The scatter plot reveals a slight negative correlation between video length and view count, suggesting that shorter videos generally receive more views. Videos in the 0-5 minute range show the highest average view counts, likes, and comments. As the video length increases, engagement tends to decrease.

12. Analyze the relationship between views and number of tags used in the video.

    ![image](https://github.com/user-attachments/assets/3afcf3c3-8516-43bd-9ef8-fc9f8542dbcd)
#### The scatter plot shows a weak correlation between the number of tags and view count, indicating that tags have little effect on views.

13. The time a video is posted can significantly affect its views. Posting when your audience is most active can lead to higher engagement. For example, videos posted during peak hours, such as evenings or weekends, tend to perform better, as more people are online and can watch. Testing different posting times and analyzing the results can help determine the optimal time for your audience.
   ![image](https://github.com/user-attachments/assets/a6fd4910-dd7d-4ea2-81df-64fe35ed2082)
#### Most videos are published between 2 PM and 8 PM, which may be the optimal upload time. However, there is a weak negative correlation between publish hour and view count, indicating that the time of upload has little impact on engagement.

 ### Conclusion :-
  - Encourage viewers to like and leave comments on videos to enhance engagement metrics.
  - Focus on creating shorter videos (less than 5 minutes) for better engagement, particularly in genres like Music and Entertainment.
  - Upload videos during peak hours (2 PM – 8 PM) to maximize initial views and interactions.

















 
