## Project Report

### 1. Motivation
The project aims to analyze Instagram usage patterns to understand better how the user interacts with content on the platform. By examining activity, the user aims to discover insights about engagement and potential patterns in their Instagram usage. This analysis can help make more intentional decisions about how to interact with the platform.

### 2. Data Source
The data for this project is collected from various Instagram exports and API interactions, including:
- **HTML files**: Exported data files such as `advertisers_using_your_activity_or_information.html`, `post_comments_1.html`, `followers_1.html`, `following.html`, `liked_posts.html`, and `recommended_topics.html`.
- **Instagram API**: Additional data regarding engagement metrics.

### 3. Data Analysis

#### Techniques Used

1. **Data Collection and Preprocessing**:
   - **BeautifulSoup**: Used to parse HTML files and extract relevant data.
   - **Regular Expressions**: Employed to extract specific patterns of information from HTML content.
   - **Pandas**: For data manipulation and organization into structured DataFrames.

2. **Exploratory Data Analysis (EDA)**:
   - **Descriptive Statistics**: Calculating key metrics such as the number of followers, following, mutual connections, and engagement metrics.
   - **Data Visualization**: Using `Matplotlib` and `Seaborn` to create visual representations of data trends and distributions.

3. **Clustering and Dimensionality Reduction**:
   - **Sentence-BERT**: For encoding text data into semantic embeddings.
   - **K-Means Clustering**: To identify clusters of similar topics or advertisers.
   - **t-SNE**: For reducing dimensionality and visualizing data in a 2D scatter plot.

4. **Sentiment Analysis**:
   - **TextBlob**: To perform sentiment analysis on comments and classify them as positive, negative, or neutral.

#### Stages of Analysis

1. **Extracting Advertiser Data**:
   - Parsed HTML content to extract the list of advertisers using the user's activity or information.
   - Applied Sentence-BERT to encode advertiser names into embeddings.
   - Used K-Means for clustering advertisers and t-SNE for visualization.

2. **Analyzing Comments**:
   - Extracted comments from HTML and performed sentiment analysis using TextBlob.
   - Classified comments into sentiment categories and visualized sentiment distribution.

3. **Examining Followers and Following**:
   - Extracted usernames of followers and following from HTML.
   - Compared lists to identify mutual connections, users not following back, and users not followed back.

4. **Investigating Liked Posts**:
   - Extracted liked posts' data, including usernames, post URLs, and timestamps.
   - Analyzed the frequency of liked posts over time, most active liking hours, and days.
   - Identified top users by the number of liked posts.

5. **Exploring Recommended Topics**:
   - Extracted recommended topics and encoded them using Sentence-BERT.
   - Applied K-Means clustering and t-SNE for visualization.

### 4. Findings

#### Advertisers
- Identified clusters of advertisers, with the main meanings being companies like "Shelf Inc.", "BOSS", "Fashion Nova", etc.

#### Comments
- Most comments extracted were positive, with a smaller proportion being neutral or negative.
- Visualized the sentiment distribution of comments.

#### Followers and Following
- Analyzed the number of followers, following, mutual connections, and users not following back.
- Identified a small number of users who were not following back and users not followed back.

#### Liked Posts
- The frequency of liked posts showed specific patterns over time, with certain hours and days being more active.
- Identified top users based on the number of liked posts.

#### Recommended Topics
- Clusters of recommended topics included "Crafts", "Cars & Trucks by Make & Model", "Travel Gear & Accessories", etc.
- Visualized these clusters using t-SNE and identified links between similar topics.

### 5. Limitations and Future Work

#### Limitations
- **Data Completeness**: The analysis is limited to the data available in the HTML exports and API interactions. Some data might be missing or incomplete.
- **Model Accuracy**: The clustering and sentiment analysis rely on pre-trained models, which may not be perfectly accurate for all types of data.
- **Visualization**: The visualizations provide a general overview but might not capture all nuances in the data.

#### Future Work
- **Expand Data Collection**: Collect more data from different sources to enhance the analysis.
- **Improve Clustering**: Experiment with different clustering algorithms and parameters to improve the accuracy of topic clusters.
- **Deep Dive into Sentiment Analysis**: Use advanced sentiment analysis techniques to gain deeper insights into comment sentiments.
- **Longitudinal Study**: Conduct a longitudinal study to analyze changes in Instagram usage patterns over a more extended period.
- **User Behavior Analysis**: Explore additional aspects of user behavior, such as interaction patterns with specific types of content or engagement with different user groups.
