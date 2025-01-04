# **News Article Popularity Prediction and Analysis with Dahsboard.** 📰

## Table of Contents
- 1.[Project Overview](#-Project_Overview)
- 2.[About the Data](#-Data)
- 3.[Project Structure](#-Project_Structure)
- 4.[Insights](#-Insights)
- 5.[Future Enhancements](#-Future_Enhancements)

## 1. **Project Overview** 🗂️
In the modern digital era, understanding the factors influencing the popularity of online articles is crucial for businesses that rely on content distribution to drive engagement, revenue, and brand visibility. This project tackles the challenge by analyzing structured and unstructured data from news articles to answer key business questions, such as:

  - What are the most significant factors contributing to an article's popularity across different social media platforms?
  
  - How do textual features, such as headlines and topics, interact with sentiment and source credibility to impact popularity?

By leveraging advanced data analysis and visualization techniques, I have created an interactive Tableau dashboard that provides actionable insights into the factors driving engagement. The dashboard visually correlates topics, sentiment, sources, and timing with article popularity on platforms like Facebook, GooglePlus, and LinkedIn. This allows businesses/authors to understand their audience better and optimize their content strategies.

Additionally, the project employs machine learning models to predict the popularity of articles on these platforms, enabling publishers to forecast the reach and impact of their content. This predictive capability is invaluable in a real-world business scenario, where optimizing resources and tailoring content to platform-specific audiences can significantly improve ROI and customer satisfaction.

By integrating insights from data with predictive analytics, this project empowers businesses to stay competitive in a fast-paced, content-driven marketplace.

## 2. **About the [Data](https://archive.ics.uci.edu/dataset/432/news+popularity+in+multiple+social+media+platforms)** 🏛️

This dataset comprises a comprehensive collection of news items and their respective social feedback from three prominent platforms: **Facebook**, **Google+**, and **LinkedIn**. Spanning a period of 8 months, from **November 2015 to July 2016**, it includes approximately **100,000 news articles** categorized into four distinct topics: **economy**, **microsoft**, **obama**, and **palestine**. 

The dataset is specifically designed for **evaluative comparisons** in predictive analytics tasks. However, its diverse structure allows for exploration in other research areas, such as:
- **Topic Detection and Tracking**
- **Sentiment Analysis in Short Text**
- **First Story Detection**
- **News Recommendation Systems**

#### **News Data Variables**
- **IDLink** *(numeric)*: Unique identifier for each news item.
- **Title** *(string)*: Title of the news item as reported by the official media sources.
- **Headline** *(string)*: Headline of the news item as reported by the official media sources.
- **Source** *(string)*: Original news outlet that published the article (e.g., USA Today, Bloomberg).
- **Topic** *(string)*: The primary topic of the news article, one of **['obama', 'microsoft', 'palestine', 'economy']**.
- **PublishDate** *(timestamp)*: Date and time when the news item was published.
- **SentimentTitle** *(numeric)*: Sentiment score of the news title, reflecting the emotional tone.
- **SentimentHeadline** *(numeric)*: Sentiment score of the news headline, reflecting the emotional tone.
- **Facebook** *(numeric)*: Popularity score of the news item on Facebook.
- **GooglePlus** *(numeric)*: Popularity score of the news item on Google+.
- **LinkedIn** *(numeric)*: Popularity score of the news item on LinkedIn.

#### **Key Insights**
The dataset's multi-platform nature and temporal feedback make it ideal for:
- Analyzing the dynamics of news virality across platforms.
- Understanding the impact of different sentiments on social engagement.
- Developing robust predictive models for news popularity.

This dataset offers an excellent foundation for advanced analytics and innovative applications in the fields of data science, machine learning, and social media studies.

## 3. **Project Structure** 🧱

This project is organized into four main components to ensure clarity, maintainability, and ease of collaboration.

---

### **Directory Overview**

```plaintext
Project_Root/
├── data/
│   ├── raw/                     # Contains the raw datasets
│   │   ├── news_data.csv        # News metadata
│   ├── processed/               # Stores cleaned and transformed data
│       ├── processed_data.csv
├── scripts/
│   ├── etl.py                   # ETL (Extract, Transform, Load) script
│   ├── analysis.py              # Data analysis and insights generation for Decision making
│   ├── ml_model.py              # Machine learning model development
├── dashboards/
│   ├── news_popularity_dashboard.twb  # Tableau dashboard for visualizations and KPI's
├── visuals/
│   ├── charts/                  # Stores generated visualizations and plots
├── reports/
│   ├── README.md                # Project documentation
```

### **How to Use**

1. **Setup**: 
   - Clone the repository.
   - Place raw data files in the `data/raw/` directory.
2. **Run ETL**:
   - Execute `etl.py` to generate the processed data.
3. **Analysis**:
   - Use `analysis.py` to generate insights and visualizations.
4. **Model Development**:
   - Run `ml_model.py` to build and evaluate predictive models.
5. **Dashboard**:
   - Use Tableau to visualize data using `news_popularity_dashboard.twb`.
   - [Dashboard Link](https://public.tableau.com/app/profile/adhyatma.sharma6816/viz/News_Dashboaord/News_Dashboard)

---

### **Dependencies**
- Python 3.x
- Tableau Desktop

## 4. **Insights** 🔍

### Insights: **Understanding News Popularity Across Social Media Platforms**

This analysis explores the factors influencing the popularity of news articles across Facebook, GooglePlus, and LinkedIn. The insights generated from this project aim to answer business questions, guide content strategy, and assist decision-makers in optimizing their platform-specific content approaches.

---

### **Key Insights and Business Questions Addressed**

#### **1. Popular Topics by Platform**
- **Facebook**: Topics with sentimental appeal, such as "obama," perform exceptionally well (Avg. Popularity = 2411.93). 
- **GooglePlus**: Global issues like "palestine" gain higher traction (Avg. Popularity = 2480.58).
- **LinkedIn**: Professional topics like "microsoft" (Avg. Popularity = 909.74) align with the platform's purpose.  

**Business Impact**:  
- Sentimental and globally relevant topics resonate differently across platforms. For content optimization, businesses should tailor their posts based on the platform's audience.  
- For example, a business targeting LinkedIn users should focus on professional and industry-relevant content.

---

#### **2. Source Popularity Analysis**
- Repeating sources for a topic consistently achieve higher traction across all platforms.  
- **Key Finding**: A frequently appearing source is a significant determinant of an article's popularity, irrespective of the platform or topic.  

**Business Impact**:  
- Consistency in publishing from credible and recognized sources boosts engagement.  
- Businesses should consider partnering with well-known sources or maintaining a consistent presence on topics to maximize visibility.

---

#### **3. Sentiment Analysis: Headline and Title**
- Articles with **extreme sentiment** (either positive or negative) perform better than those with neutral or modest sentiments.
  - **Facebook**: Avg. Popularity for extreme positive sentiment = 1890.26  
  - **GooglePlus**: Avg. Popularity for extreme negative sentiment = 1869.39  
  - **LinkedIn**: Extreme negative sentiment slightly outperforms positive sentiment.  

**Business Impact**:  
- Articles with strong sentiments align with the "Bad publicity is good publicity" effect.  
- Content creators can leverage polarizing topics to increase engagement but should balance this approach to avoid reputational risks.

---

#### **4. Headline/Title Word Patterns**
- Headlines and titles with highly repeated words within a topic have significantly higher popularity.  
- This trend is likely driven by the "Hot Topic" phenomenon, where widespread coverage leads to increased visibility.  

**Business Impact**:  
- Crafting headlines with trending or widely recognized keywords can enhance article visibility and popularity.  
- Businesses should monitor trending topics and tailor headlines accordingly.

---

#### **5. Publishing Day vs. Platform Popularity**
- **Facebook and GooglePlus**: Articles posted on weekends gain higher traction.  
- **LinkedIn**: Articles posted on weekdays perform better, aligning with its business-oriented audience.

**Business Impact**:  
- Scheduling posts based on platform-specific user activity can maximize engagement.  
- Businesses can adopt a targeted posting schedule:  
  - Sentimental or casual content for weekends on Facebook and GooglePlus.  
  - Professional content for weekdays on LinkedIn.

---

### **Conclusion**
The insights generated from this analysis highlight how platform-specific characteristics, content sentiment, and publishing patterns influence news article popularity. Decision-makers can use this information to:  
1. **Optimize Content Strategy**: Tailor topics, headlines, and sentiment for each platform.  
2. **Enhance Timing and Distribution**: Align posting schedules with audience behavior.  
3. **Leverage Reliable Sources**: Prioritize consistent and credible sources for higher engagement.  

These actionable insights help businesses refine their content strategies, boost social media engagement, and improve overall effectiveness in reaching their target audiences. Further Anlaysis and insights are provided in the News_Analysis.ipynb file and the Tableau Dashboard.

## 5. **Future Enhancement Plans** 🔮

### Future Enhancements

To make this project more scalable and applicable to real-life industry scenarios, the following enhancements can be implemented:

- **Distributed Processing with Apache Spark**:  
  - We can Spark for handling large-scale datasets, enabling faster ETL processes and real-time analytics.  
  - Leverage Spark MLlib for advanced machine learning model training on massive data.

- **Integration with AWS Services**:  
  - **S3**: Store and retrieve large datasets efficiently. We can store the cleaned Data in S3 and put a life cycle on the Raw data.  
  - **Redshift**: Use for scalable and high-performance data warehousing.  
  - **Lambda**: Automate data processing tasks and trigger workflows.  
  - **SageMaker**: Train and deploy machine learning models seamlessly.  

- **Real-Time Data Pipelines**:  
  - We can implement tools like Kafka for real-time ingestion and analysis of news data from multiple sources and sites.
  
These enhancements will improve scalability, efficiency, and applicability in enterprise settings.

Dashboard Screenshot:
![News_Dashboard](https://github.com/user-attachments/assets/90834c0a-2fc4-4ba2-a8de-170017c82c24)

