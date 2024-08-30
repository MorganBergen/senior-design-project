.≥#  clarity

clarity, food is medicine

[wireframe](https://www.figma.com/team_invite/redeem/PVaDtEEPARNQ8fxIHyGVPo)

###  description 

a health analytics platform that utilized dietary image capture and ai to provide personalized nutrition insights, predict disease risk factors, and offer tailed recommendations to improve health outcomes, and allows users to export their data for sharing with healthcare providers and insurance providers to reduce 
healthcare insurance costs.

<img src="login.svg">

<img src="dashboard.svg">

###  features explained

1.  user profile and data input

users provide their specific information, including age, gender, weight, medical history, medications, and other relevant health data.  the user can set specific health goals related to their dietary needs, such as managing diabetes, losing weight, or improving overall wellness.

2.  mobile device image capture

users capture images of their meals using a mobile device.  the software should be user friendly and guide users on how to take clear and useful photos for analysis.

3.  image analysis and nutritional data extraction

[ai powered analysis](https://openfoodfacts.github.io/openfoodfacts-server/) will consist of uploaded images to a desktop software where machine learning algorithms analyze the food items for nutritional content, portion sizes, and dietary composition.

-  The app allows users to scan the barcode of products, to view the product information, and to take and submit pictures and data for missing products. [ios app](https://github.com/openfoodfacts/openfoodfacts-ios)  

4.  data analysis and health insights

nutritional variables for analysis - 

```JSON
[
  {
    "timestamp": "yyyy-mm-ddThh:mn:ssZ",
    "transaction": [
        {
            "location": "",
            "vendor": "",
            "vendor-id": ""
        }
    ],

    "general": [
        {
            // Barcode of the product
            "code": "200-EAN-13",

            // URL of the product page
            "url": "https://xxx.com",
            
            // Date that the product was added (UNIX timestamp format)
            "created_t": "yyyy-mm-ddThh:mn:ssZ",

            // Date that the product was last modified (UNIX timestamp format)
            "last_modified_t": "yyyy-mm-ddThh:mn:ssZ",

            // Name of the product
            "product_name": "cherios",

            // Generic name of the product
            "generic_name": "cereal",

            // Field that designates quantity and unit size
            "quantity":  _100g
        }
    ],
    "tags" : [
        {
            "packaging": shape, material,
            "packaging_tags": "",
            "brands": "",
            "brand_tags": "", 
            "categories": "",
            "categories_fr": "",
            "origins": "origins of ingredients",
            "origintags": "",
            // Locations where manufactured or transformed
            "manufacturing_places": "",
            "manufacturing_places_atgs": "",
            "labels": "",
            "labels_tags": "",
            "emb_codes": "",
            "emb_code_tags": "",

            // Coordinates corresponding to the first packaging code indicated
            "first_packaging_code_geo": "",
            "cities": "",
            "cities_tags": "",
            "purchase_places": "",
            "stores": "",
            
            // List of countries where the product is sold
            "countries": "",
            "countries_tags": ""
        }
    ],
    "ingredients" : [
        {
            "ingreidents_text": "",
            "traces": "",
            "traces_tags": ""
        }
    ],
    "misc_data" : [
        {
            // Serving size in g
            "serving_side": ...,
            // Indicates if the nutrition facts are indicated on the food label
            "no_nutrients": ...,
            "additives": ...,
            "additives_tags": ...,
            "ingredients_from_palm_oil_n": ...,
            "ingreidents_from_palm_oil": ...,
            "ingreidents_from_palm_oil_tags": ...,
            "ingreidents_that_may_be_from_palm_oil_n": ...,
            "ingreidents_that_may_be_from_palm_oil_tags": ...,
            
            // Nutrition grade ('a' to 'e')
            // Reference: https://fr.openfoodfacts.org/nutriscore
            "nutrition_grade_fr": "a",

            "main_category": ...,
        }
    ],

    "nutrition_facts": [
        {
            "energy_100g": ...,
            "energy-kj_100g": ...,
            ...
        }
    ],

    "nutrition_facts" : [
        {
            "energy-kcal_100g": ...,
            "proteins_100g": ...,
            "casein_100g": ...,
            "serum-proteins_100g": ...,
            "nucleotides_100g": ...,
            "carbohydrates_100g": ...,
            "sugars_100g": ...,
            "sucrose_100g": ...,
            "glucose_100g": ...,
            "fructose_100g": ...,
            "lactose_100g": ...,
            "maltose_100g": ...,
            "maltodextrins_100g": ...,
            "starch_100g": ...,
            "polyols_100g": ...,
            "fat_100g": ...,
            "saturated-fat_100g": ...,
            "butyric-acid_100g": ...,
            "caproic-acid_100g": ...,
            "caprylic-acid_100g": ...,
            "lauric-acid_100g": ...,
            "myristic-acid_100g": ...,
            "palmitic-acid_100g": ...,
            "stearic-acid_100g": ...,
            "arachidic-acid_100g": ...,
            "behenic-acid_100g": ...,
            "lignoceric-acid_100g": ...,
            "cerotic-acid_100g": ...,
            "motanic-acid_100g": ...,
            "melissic-acid_100g": ...,
            "monounsaturated-fat_100g": ...,
            "polyunsaturated-fat_100g": ...,
            "omega_3-fat_100g": ...,
            "alpha-linolenic-acid_100g": ...,
            "eicosapentaenoic-acid_100g": ...,
            "docosahexaenoic-acid_100g": ...,
            "omega_6-fat_100g": ...,
            "linoleic-acid_100g": ...,
            "arachidonic-acid_100g": ...,
            "gamma-linolenic-acid_100g": ...,
            "dihomo-gamma-linolenic-acid_100g": ...,
            "omega_9-fat_100g": ...,
            "oleic-acid_100g": ...,
            "elaidic-acid_100g": ...,
            "gondoic-acid_100g": ...,
            "mead-acid_100g": ...,
            "erucic-acid_100g": ...,
            "nervonic-acid_100g": ...,
            "trans-fat_100g": ...,
            "cholesterol_100g": ...,
            "fiber_100g": ...,
            "sodium_100g": ...,
            // % vol of alcohol
            "alcohol_100g": ...,
            "vitamin-a_100g": ...,
            "vitamin-d_100g": ...,
            "vitamin-e_100g": ...,
            "vitamin-c_100g": ...,
            "vitamin-b1_100g": ...,
            "vitamin-b2_100g": ...,
            "vitamin-pp_100g": ...,
            "vitamin-b6_100g": ...,
            "vitamin-b9_100g": ...,
            "vitamin-b12_100g": ...,
            // Also known as vitamine b8
            "biotin_100g": ...,
            "pantothenic-acid_100g": ...,
            "silica_100g": ...,
            "bicarbonate_100g": ...,
            "chloride_100g": ...,
            "calcium_100g": ...,
            "phosphorus_100g": ...,
            "iron_100g": ...,
            "magnesium_100g": ...,
            "zinc_100g": ...,
            "copper_100g": ...,
            "manganeses_100g": ...,
            "fluoride_100g": ...,
            "selenium_100g": ...,
            "chromium_100g": ...,
            "molybdenum_100g": ...,
            "iodine_100g": ...,
            "caffeine_100gtaurine_100g": ...,
            // pH (no unit)
            "ph_100g": ..., 
            // % of fruits, vegetables, and nuts (excluding potatoes, yams, manioc)
            "fruits-vegetables-nuts_100g": ...,
        }
    ],

    // Nutri-Score
    // Nutrition score derived from the UK FSA score and adapted for the French market (formula defined by the team of Professor Hercberg)
    "nutrition-score-fr_100g" : "a",

    // Nutrition score defined by the UK Food Standards Administration (FSA)
    "nutrition-score-uk_100g": "a",

  }
] 
```

disease risk prediction, health impact projections, and trend analysis.  such as weight gain/loss, nutrient deficiencies, over consumption, heart disease risk factors, etc.

5.  dashboard and reporting

user dashboard:  provide users with an interactive dashboard that displays their dietary habits, nutritional intake, health trends, chronic disease management and progress towards their goals.

6.  data export and sharing with healthcare provider

export options enable users to export their dietary data and health analytics in formats suitable for sharing with healthcare providers.

secure sharing will need to be implemented, which will consist of protocols for sharing data with healthcare providers and insurers, potentially leading to benefits such as reduced insurance premiums based on health improvements.

7.  integration with health devices

cgm - continuous glucose monitors, insulin pumps, and smart watches can gather additional health data such as glucose levels and physical activity.

diabetics on the platform could correlate dietary intake with fluctuations in blood glucose levels, offering tailored dietary advice to help manage glucose levels, or provide insights on how different foods affect insulin requirements

integrate with [HealthKit](https://developer.apple.com/documentation/healthkit/)

8.  privacy and security measures

ensure all user data is encrypted and stored securely and comply with relevant privacy regulations like hippa - health insurance portability and accountability act or gdpr - general data protection regulation to protect personal health information

user consent should be implemented and have clear consent protocols, allowing users to control what data is collected and how it is used or shared

9.  user engagement and support

notifications and reminders can be set up for users to log meals and take health measurements.  personalized recommendations and summaries can be sent to the users to keep them engaged and motivated to improve their health.
 
10.  insurance negotiation reports

generate detailed reports that contain aggregated data on health metrics, trend analysis, risk assessments, and projected health outcomes.  these reports can be exported and formatted in a way that is suitable for submission to insurance companies.

###  development requirements

-  functional requirements
-  application pages
-  system features
-  technology stack
-  api integration
-  architectural planning - technical architecture, including how the app will communicate with the open food facts api, data storage solutions, and how to handle data processing and analysis.
-  api integration point identification - open food facts api, healthkit, and other health devices

###  mobile application development details

functional requirements

-  image capture - access to the device camera to take photos of food or upload images from the gallery
-  user authentication - secure login and logout functionality
-  image analysis - immediate analysis of captured images to identify food items and estimat enutritional content
-  data synchronization - synchronize data with the web application and cloud storage

application pages

-  home/dashboard - overview of daily intake and summarized health statistics
-  login/sign up page - user authentication interface
-  meal log - page to capture or upload images of meals, scan barcode, or log food items
-  profile and settings - manage personal information, health goals, and app settings

system features

-  push notifications - summarize daily intake
-  food log feedback - provide food identification and nutritional information
-  visual representation - graphs and charts to display health metrics and trends
-  interoperate with the web application - synchronize data with the web application and cloud storage

api integration

-  open food facts api - for food identification and nutritional information
-  healthKit - for integration with health devices and data collection

technology stack ideas

-  language -  typescript 
-  library / framework - react native
-  app function - for cross-platform development and provides a native-like experience
-  firebase - for cloud storage, user authentication, and data handling
-  `react-native-health` for integrating with healthKit
-  platform integration - firebase for cloud storage, user authentication, hosting, and database.
-  additional tools - `redux` for state management, `axios` for https request, jest for unit testing

###  web application

functional requirements

-  user authentication - consistent with the mobile application for seamless user experience
-  data analysis tools - advanced tools for deep data analysis and report generation
-  reporting - functionalities to export reports for healthcare providers & insurance companies

application page

-  login/sign up page - unified authentication system with the mobile application
-  dashboard - detailed view of nutritional trends, health insights, and disease risk predictions
-  reports page -  generate & export reports for insurance negotiations & healthcare provider sharing
-  settings - manage application settings, user profiles and api integrations

system features

-  data synchronization - sync with the mobile app for real time data updates
-  interactive graphs and charts - for visual representation of health metrics and trends

api integration

-  open food facts api - for food identification and nutritional information
-  healthKit - for integration with health devices and data collection

technology stack ideas

-  language - typescript
-  library / framework - react for web development
-  app function - provide a framework for building dynamic web application with a focus on user interface
-  firebase - for cloud storage, user authentication, and data handling
-  api integration - open food facts api, healthKit, and other health devices
-  additional tools - `redux` for state management, `axios` for https request, jest for unit testing

###  resources

[uber api](https://developer.uber.com/docs/eats/introduction)

[food labeling](https://www.nal.usda.gov/legacy/aglaw/food-labeling)

[open food facts monitoring](https://github.com/openfoodfacts/openfoodfacts-monitoring)

[open food facts api documentation](https://openfoodfacts.github.io/openfoodfacts-server/api/)