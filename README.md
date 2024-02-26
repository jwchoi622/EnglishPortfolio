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


# [앤드 투 앤드 Azure 데이터 엔지니어링 프로젝트](https://github.com/jwchoi622/TokyoOlympics)

## **개요**
이 프로젝트는 데이터 수집부터 시각화까지 전체 데이터 파이프라인에 중점을 둔 Azure 기반 데이터 엔지니어링 프로젝트입니다. Azure Data Factory를 활용한 데이터 전처리로 시작하여 Databricks에서 변환을 진행합니다. 본 프로젝트에서는 Azure 서비스 내에서의 학습 및 기술 개발에 주안점을 둔 Azure 에코시스템을 효과적으로 활용하고 있습니다. 

주요 구성 요소로는 Kaggle 데이터셋 처리, 데이터 변환, Azure Synapse를 이용한 분석, 호환성 고려한 Tableau를 이용한 시각화가 포함되었습니다. 이 프로젝트를 통하여 Azure 플랫폼 기능, 데이터 파이프라인 설계, 데이터 인사이트 생성까지의 앤드 투 앤드 데이터 프로젝트를 수행하였습니다.


## **사용된 기능**
1) Azure Data Factory  
2) Azure Databricks  
3) Azure SQL Database  
4) Azure Data Lake  
5) Tableau  

##  **추가 자료**
**Medium 프로젝트 블로그:** Azure에서의 프로젝트 데이터 엔지니어링 과정에 대한 종합적인 개요입니다. [블로그 글](https://medium.com/@jwchoi622/end-to-end-azure-data-engineering-project-73ade8163e91).   
**Tableau 대시보드:** 도쿄 올림픽 데이터셋에서 파생된 인사이트를 보여주는 인터랙티브 시각화입니다. [대시보드](https://public.tableau.com/app/profile/james.choi1221/viz/TokyoOlympics_17022794668810/TokyoOlympicsDashboard?publish=yes). 

![](/images/pipeline.png)

![](/images/dashboard.png)


# [UFC 파이터 이미지 분류 프로젝트](https://github.com/jwchoi622/fighterClassification)

## **개요**
이 프로젝트는 UFC 파이터의 이미지를 정확하게 식별하고 분류할 수 있는 이미지 분류 모델을 개발하는 것을 목표로 합니다. 본 모델은 컨볼루션 신경망(CNN)을 사용하여 준비된 데이터셋에서 파이터들의 시각적 특징을 바탕으로 서로 다른 파이터들을 구별하도록 학습합니다.

본 프로젝트에서 가장 중요한 점은 포즈, 조명, 배경, 장비 등에 따라 다양한 형태로 달라지는 파이터 이미지를 정확하게 분류하는 것입니다. 이러한 변이성으로 인하여 다른 파이터의 이미지와 구별하면서도 같은 파이터의 다른 이미지들 간의 일관된 특징을 식별하는 일이 도전적인 일입니다.

## **해결책**
이 도전과제를 해결하기 위하여 파이터의 이미지에서 미묘한 시각적 패턴을 포착하도록 맞춤화된 CNN 기반 모델을 개발했습니다. 해결책은 다음의 몇 가지 주요 단계를 포함합니다:

**데이터 준비:** 파이터 클래스에 해당하는 라벨이 붙은 이미지를 수집하고, 이 데이터셋을 학습과 검증으로 분할하여 모델이 새로운 이미지도 분별할 수 있도록 합니다.  
**모델 구조:** CNN 모델은 이미지의 계층적 패턴에서 추출하고 배우도록 설계된 여러 레이어로 구성됩니다. 모델은 에지나 텍스쳐같은 로우레벨 특징들을 캡쳐하기 위한 컨볼루션 레이어로 시작하여 점차 각 파이터의 독특한 시각적 특징을 정의하는 더 추상적인 기능들로 발전합니다.  
**훈련 및 평가:** 모델은 분류 오류를 최소화하는 데 중점을 두고 훈련 데이터셋을 사용하여 훈련됩니다. 성능은 검증 세트에서 평가되어 정확성과 일반화 능력을 보장합니다.  

## **구현 세부사항**
**데이터 증강:** 모델의 강건성을 향상시키기 위해 로테이션, 스케일링, 수평 뒤집기와 같은 데이터 증강 기술이 사용됩니다.  
**최적화:** 모델은 최상의 성능을 달성하기 위해 세밀하게 조정된 이진 교차 엔트로피 손실 함수(binary cross-entropy loss function)와 함께 Adam 최적화기를 사용합니다.  


![](/images/fightergraph.png)

