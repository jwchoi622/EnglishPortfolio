# Pizza Restaurant Data Analysis

## Problem 
A new restaurant needs a database and a way to analyze orders, inventory and staff.

## Solution 
Design a SQL database in QuickDBD
![](/images/database.png)


Use SQL queries to get the necessary information on each of the three problems
![](/images/query.png)


Use Looker Studio to get a dashboard 
![](/images/dashboard.png)


## Insights
1. There are a couple ingredients that need to be restocked
2. Seafood pizzas are the most expensive pizzas by cost
3. Orders peak around 1pm and 7pm (lunch and dinner time)
4. Caesar salad is the highest revenue after pizza
5. Average order value is high so maybe focus on increasing orders

## Recommendations
1. Always restock when there is less than 25% left
2. Add more salads or improve Caesar Salad to get more sales 
3. Have more staff on during peak hours and less during less busy hours
4. Try to have some advertisements outside of the center of Manchester to the outer regions of the city 

# [Air Quality Index Web Application with Django](https://github.com/jwchoi622/aqproj)
## Overview
This project is a Django-based web application designed to provide up to date air quality information for any city in the world. I used the AQICN API to get the air quality data and Leaflet to get the map on the website. Lastly I used PythonAnywhere to deploy the application. The application is accessible at [https://jwchoi622.pythonanywhere.com](https://jwchoi622.pythonanywhere.com). 
## Features
- **Air Quality Information:** The first table will give the current air quality information for the city that the user inputs. It also includes a widget 
  that has a concise summary of current air quality for that city. Not all cities will get a widget because the API seems to only return a widget for major cities. 
  It also may not have information on all of the different types of pollutants such as CO or O3. 
- **Interactive Map:** The map will be centered on the queried city and also have tiles that indicate the AQI index for different neighborhoods within the city. 
  Smaller cities may not have as many tiles because they do not have as many air quality sensors. The user can also zoom in or zoom out to look at neighboring cities. 
- **PM 2.5 Forecast:** The forecast focuses on PM 2.5 because it is the most harmful of pollutants and also a big problem in Korea. The forecast will usually show 
  the PM 2.5 forecast for the next couple days in the week and have color coded dates according to the average level for that date. 
- **Calendar:** The calendar will indicate which days are safe for outdoor activity by looking at the PM 2.5 index. 

## Future Improvements
- Adding a forecast for PM10 would also be helpful in determining what the air quality would be like for future days.
- The calendar could also include markers for good, average and poor air quality.
- Including different language options.

## External APIs Used
### AQICN API
- **Description:** I used this AQICN to get the air quality data, widget, forecast data and also the map tiles.
- **Documentation:** [https://aqicn.org/api/](https://aqicn.org/api/)

### Leaflet API
- **Description:** I used the Leaflet API to get an interactive map of the queried city.
- **Documentation:** [https://leafletjs.com/reference.html](https://leafletjs.com/reference.html)

### OpenCage Geocoding API
- **Description:** I used the OpenCage API to get the latitude and longitude of the city and fed those coordinates into the Leaflet map. 
- **Documentation:** [https://opencagedata.com/api](https://opencagedata.com/api)

![](/images/pic2.png)


# [End-to-End Azure Data Engineering Project](https://github.com/jwchoi622/TokyoOlympics)
## Overview
This project is an Azure-based data engineering project, focusing on the entire data pipeline from ingestion to visualization. It starts with data preprocessing, leveraging Azure Data Factory for ingestion and Databricks for transformation. The project demonstrates effective use of Azure's ecosystem, emphasizing learning and skill development within Azure services. Key components include handling Kaggle datasets, data transformation, analytics with Azure Synapse, and visualization with Tableau due to compatibility considerations. This project serves as an introductory exploration into Azure platform capabilities, data pipeline design, and data insight generation.

## Technologies Used
- Azure Data Factory
- Azure Databricks
- Azure SQL Database
- Azure Data Lake
- Tableau

## Additional Resources

For more detailed insights and visual representations of the data analyzed in this project, refer to the following resources:
- **Project Walkthrough on Medium**: A comprehensive overview of the project's data engineering process on Azure. [Read the article here](https://medium.com/@jwchoi622/end-to-end-azure-data-engineering-project-73ade8163e91).

- **Tokyo Olympics Dashboard on Tableau**: Interactive visualizations showcasing insights derived from the Tokyo Olympics dataset. [View the dashboard here](https://public.tableau.com/app/profile/james.choi1221/viz/TokyoOlympics_17022794668810/TokyoOlympicsDashboard?publish=yes).


![](/images/pipeline.png)

![](/images/dashboard.png)


# [Fighter Image Classifier Project](https://github.com/jwchoi622/fighterClassification)
## **Overview**
This project aims to develop an image classification model that can accurately identify and classify images of fighters. Utilizing a convolutional neural network (CNN), the model learns to distinguish between different fighters based on their visual features from a curated dataset.

## **Problem Statement**
The challenge lies in accurately classifying images of fighters, which may vary significantly in terms of pose, lighting, background, and equipment. Such variability introduces complexity in identifying distinctive features that are consistent across different images of the same fighter while differentiating them from images of other fighters.

## **Solution**
To address this challenge, we developed a CNN-based model tailored to capture the nuanced visual patterns present in images of fighters. The solution involves several key steps:

**Data Preparation:** Images are collected and labeled with their corresponding fighter class. This dataset is then split into training and validation sets to ensure the model can generalize well to new, unseen images.

**Model Architecture:** The CNN model consists of several layers designed to extract and learn from the hierarchical patterns in the images. Starting with convolutional layers to capture low-level features such as edges and textures, the model progressively builds up to more abstract features that define each fighter's unique visual signature.

**Training and Evaluation:** The model is trained using the training dataset with a focus on minimizing classification error. Performance is evaluated on the validation set to ensure accuracy and the ability to generalize.

## **Implementation Details**
**Data Augmentation:** To enhance the robustness of the model, data augmentation techniques such as rotation, scaling, and horizontal flipping are employed.

**Optimization:** The model uses the Adam optimizer with a binary cross-entropy loss function, fine-tuned to achieve the best performance.  
  


![](/images/fightergraph.png)

