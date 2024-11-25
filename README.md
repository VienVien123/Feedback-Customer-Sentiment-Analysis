# Customer Sentiment Analysis Through Feedback

## Table of Contents
1. [Introduction](#introduction)
2. [Data Analysis Process](#data-analysis-process)
3. [Labeling Methods](#labeling-methods)
   - [1. Rating-Based Labeling](#1-rating-based-labeling)
   - [2. Using a Pre-Trained Model (5CD/AI)](#2-using-a-pre-trained-model-5cdai)
4. [Technologies Used](#technologies-used)
5. [Installation Guide](#installation-guide)
   - [1. Clone Repository](#1-clone-repository)
   - [2. Create Virtual Environment (venv)](#2-create-virtual-environment-venv)
   - [3. Install Required Libraries](#3-install-required-libraries)
   - [4. Run the Project](#4-run-the-project)
6. [References](#references)

---

## Introduction
This project focuses on analyzing customer sentiment based on feedback received after purchasing a product from Company X. The initial dataset contains customer feedback that has not yet been cleaned or labeled.

The goal of this project is to perform preprocessing, label the data, and classify customer sentiment into three categories: **Positive**, **Negative**, and **Neutral**.

---

## Data Analysis Process
The original data contains customer feedback that has not yet been processed. The main steps in the analysis process include:

1. **Data Preprocessing**: Clean the data by removing unnecessary characters, and handling synonyms and spelling errors.
2. **Label Sentiment**: The data is classified into three sentiment categories: Positive, Negative, and Neutral.
3. **Sentiment Analysis**: Evaluate customer sentiment using two different labeling methods.
4. **Compare Labeling Methods**: Compare the results from the two labeling methods.
5. **Visualization**

---

## Labeling Methods

### 1. Rating-Based Labeling
- Feedback is labeled based on the number of stars given by the customer.
  - **Positive**: Ratings of 4 or 5 stars.
  - **Neutral**: Rating of 2 or 3stars.
  - **Negative**: Ratings of 0 or 1 stars.

### 2. Using a Pre-Trained Model (5CD/AI)
- Use a pre-trained model - **[5CD/AI Vietnamese Sentiment visobert](https://huggingface.co/5CD-AI/Vietnamese-Sentiment-visobert)**.
- The model will label the sentiment of feedback and combine it with the **KMeans** algorithm to improve the accuracy of the labels.

You can learn more about the 5CD/AI model via the link [here](https://huggingface.co/5CD-AI/Vietnamese-Sentiment-visobert).

---

## Technologies Used
- **Language**: Python, Jupyter Notebook (`.ipynb`)
- **Python Version**: 3.8 or higher
- **Operating System**: Windows and macOS

---

## Installation Guide

### Set Up Virtual Environment and Install Libraries

```bash
python -m venv venv
source venv/bin/activate       # macOS/Linux
source .venv\Scripts\activate  # Windows
pip install -r requirements.txt
