# Identifying-patient-episodes-with-NLP

### Concept

One of the key components of primary care is to provide episodic care to patients, where an episode defines a certain problem a patient is having (e.g. back pain). If a primary care service wants to analyse how well it performs at episodic care, it may struggle with actually identifying episodes in data, as there is often no episode indicator that appointment X was related to appointment Y.

I propose a solution to this by using NLP and doctor's appointment notes, whereby the notes are analysed and compared between appointments to determine if they are about the same problem.

### Process

Due to the sensitive nature of appointment notes, this project uses a dataset from Kaggle (https://www.kaggle.com/datasets/rmisra/news-category-dataset?resource=download) containing data on news articles, including a column containing a short description of each article. The aim of the project is to determine if two articles are about the same subject.

This will be done by cleaning the descriptions of each article such that each article has a comparable set of words used, before calculating the Jaccard Distance between two descriptions' word lists. If the distance is below a certain threshold, the two descriptions are considered to be about the same subject and are assigned the same group ID.

To reiterate how this would apply to doctor's notes, data can be grouped by patient and each appointment a patient has can be compared to each other appointment and grouped into episodes based on similarity between notes.
