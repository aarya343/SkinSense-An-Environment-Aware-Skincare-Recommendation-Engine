# SkinSense: An Environment-Aware Skincare Recommendation Engine

**Author:** Aarya Nenawatee  
**Project Category:** Open Source Programming (OSP) Project-Based Learning (PBL)

##  Project Overview
**SkinSense** is a pipeline-driven Python application designed to act as an environment-aware skincare advisory tool. The application uses community-sourced product data and live local weather to match an individual's profile with safe, high-efficacy cosmetic ingredients suited to their microclimate.

##  Open-Source Data Pipelines & APIs
* **Cosmetics Ingredient Core:** [Open Beauty Facts API & Dump](https://world.openbeautyfacts.org/data)
* **Live Environmental Conditions:** OpenWeatherMap API

##  Architecture & Pipeline Steps

The system runs sequentially through a structured 8-cell notebook workflow:

1. **Cell 1: Environment Setup**: Installation of necessary open-source data manipulation, networking, and dashboarding modules.
2. **Cell 2: Remote Data Ingestion**: Fetching raw public cosmetic registries and chemical listings through the Open Beauty Facts ecosystem.
3. **Cell 3: Text Normalisation & Clean INCI Map**: String cleansing, text transformation, and mapping of active items to standardised INCI (International Nomenclature Cosmetic Ingredient) indices.
4. **Cell 4: Ingredient Classification Array**: Tagging extracted ingredients into specific biological functionalities (e.g., Humectants, Emollients, Occlusives, Exfoliants, UV Filters).
5. **Cell 5: Interactive User Skin Quiz**: Collecting user-specific attributes (Skin type: Dry/Oily/Sensitive, specific concerns like Acne/Ageing, and personal restrictions).
6. **Cell 6: Meteorological Context Extraction**: Pinging the OpenWeather API using the user's city location to retrieve real-time Temperature, Humidity, and UV Index.
7. **Cell 7: Dual-Heuristic Matching Engine**: Combining skin profiles with atmospheric factors (e.g., suggesting lighter humectants/sebum control in hot, humid areas, or deep occlusives and barriers in dry, frozen conditions).
8. **Cell 8: Interactive UI Dashboard**: Providing an intuitive visual dashboard summarising matching scores and explaining the scientific rationale behind each cosmetic asset recommendation.

##  Requirements & Installation
To execute the engine locally, run:
```bash
pip install pandas numpy requests matplotlib seaborn
