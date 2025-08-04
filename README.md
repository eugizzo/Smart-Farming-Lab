### Eugene mugiraneza  27580

# Smart-Farming-Lab


# 🌾 Smart Farming Lab Survey
Welcome to the Smart Farming Lab Survey – a collaborative research initiative aimed at cataloging and analyzing computer vision datasets in the domain of precision agriculture and smart farming.

* Smart Farming Lab is a collaborative research initiative focused on collecting, curating, and evaluating computer vision datasets used in precision agriculture and smart farming applications.

* A comprehensive catalog of agricultural vision datasets designed to support precision agriculture and smart farming.
Focus on plant species, plant parts, annotation types, and modalities

* Tasks include classification, segmentation, and detection


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

## Load and Clean the Dataset

```python
import pandas as pd

# Load the local TSV dataset
file_path = "/content/drive/MyDrive/smartfarminglab/dataset_table.tsv"
df = pd.read_csv(file_path, sep='\t')

# Drop unneeded fields
df = df.drop(columns=['Paper-URL', 'Dataset-URL'], errors='ignore')

# Show the first few rows
df.head()
```
<img width="1828" height="573" alt="image" src="https://github.com/user-attachments/assets/61df516b-8da0-4a84-9357-440c5d5dca76" />


## 🖼️ Dashboard
A preview of an interactive visualization dashboard is in progress to allow deeper dataset exploration and filtering by task, plant, year, and more.
```python
import plotly.express as px

fig = px.sunburst(df, path=['task', 'plant_english', 'plant_part'], values='annotated_images',
                  title="🌐 Dataset Coverage by Task, Plant, and Part")
fig.show()
```
<img width="1119" height="700" alt="Screenshot (304)" src="https://github.com/user-attachments/assets/166f6789-406b-45a8-8e42-81f3c5c987ca" />

### Dataset Growth Over Time
```python
plt.figure(figsize=(10, 5))
yearly = df['year'].value_counts().sort_index()
sns.lineplot(x=yearly.index, y=yearly.values, marker='o', linewidth=2, color='green')
plt.title('🗓️ Number of Datasets Published Over Time')
plt.xlabel('Year')
plt.ylabel('Dataset Count')
plt.grid(True)
plt.tight_layout()
plt.show()
```
<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/906730e5-2eb0-4a46-9ba5-ce328f97f8eb" />


### Most Common Plant Parts
```python
plt.figure(figsize=(10, 5))
sns.countplot(data=df, y='plant_part', order=df['plant_part'].value_counts().index, palette='coolwarm')
plt.title('🌱 Most Commonly Annotated Plant Parts')
plt.xlabel('Count')
plt.ylabel('Plant Part')
plt.tight_layout()
plt.show()
```
<img width="989" height="490" alt="image" src="https://github.com/user-attachments/assets/73526f09-d8ff-44ca-b8c2-4acc8b90e48e" />

📁 Files

### dataset link

https://drive.google.com/file/d/1c1f8bFDtf4rsl3b3QkrodEqQgTcm_Yeu/view?usp=sharing

### Power BI link

https://drive.google.com/file/d/1kuWWI1VK-3hhLGoPlVLyogcfq8sElNK1/view?usp=sharing

### Power points link

https://www.canva.com/design/DAGvFlVmDZ0/Jp9VBYl9Bstuc5jCSLU-mA/edit?utm_content=DAGvFlVmDZ0&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton


