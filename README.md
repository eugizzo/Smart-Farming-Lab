# Smart-Farming-Lab


# 🌾 Smart Farming Lab Survey
Welcome to the Smart Farming Lab Survey – a collaborative research initiative aimed at cataloging and analyzing computer vision datasets in the domain of precision agriculture and smart farming.

## 📘 Overview
The Smart Farming Lab compiles and evaluates a wide range of vision datasets used in modern agricultural AI systems. These datasets enable various tasks including plant disease detection, weed classification, crop phenotyping, and more.

This repository provides insights into:

The structure and content of the datasets

Key metadata (plant species, parts, annotation types)

Task-specific dataset categorization (classification, detection, segmentation)

Visual summaries and trends

## 🔍 What’s Included?
A comprehensive survey of agricultural datasets

### Task coverage:

🌱 Weed Detection and Classification

🐛 Disease and Pest Detection

🌾 Seedling and Crop Detection

📈 Plant Growth Stage Detection

🔬 Phenotyping

🧮 Detection and Counting Tasks

### Key dataset fields:

Label – Dataset name or identifier

Year – Publication year

Author – Dataset creator(s)

Plant (English/Latin) – Species

Plant Part – Leaf, stem, etc.

Task – Vision task type

Annotation – Type of labels used

Annotated Images – Quantity of labeled images

## 📊 Insights
Task Distribution:

Classification: Species or disease ID

Segmentation: Delineating plant structures

Detection: Localizing key features

Other: Counting, biomass estimation, etc.

Growth Trends: Historical dataset availability over time

Most Studied Crops: Overview of frequently represented plants

## 🖼️ Dashboard (Coming Soon)
A preview of an interactive visualization dashboard is in progress to allow deeper dataset exploration and filtering by task, plant, year, and more.
```python
import plotly.express as px

fig = px.sunburst(df, path=['task', 'plant_english', 'plant_part'], values='annotated_images',
                  title="🌐 Dataset Coverage by Task, Plant, and Part")
fig.show()
```
📁 Files
Smart_Farming_Lab_Survey.pdf – Full report of the dataset survey (see /docs folder or attached here)

🙏 Acknowledgements
Special thanks to the research contributors, dataset authors, and open-source community enabling precision agriculture innovation.
