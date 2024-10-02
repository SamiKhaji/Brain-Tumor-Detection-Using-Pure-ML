# brain_tumor_classification

Firstly this is a team Project
Lets introduce my team:

#### 1.Aateesh cb.en.u4cse214304
#### 2.Bhavana N cb.en.u4cse21411
#### 2.Rohanlal Gudivada  cb.en.u4cse21420
#### 3.K.Mahammad Sami cb.en.u4cse21430
#### 4.N.Ujwal Srimanth Varma cb.en.u4se21440

# Write Up

Image classification using pure machine learning models presents a significant challenge due to the inherent nature of image data. Unlike other types of data, images require transformation into numerical formats for machine learning models to interpret them effectively. These transformations often involve representing images as pixel-based data, typically organized as a matrix. In our dataset, MRI scans are grayscale images with a resolution of 224x224 pixels, each pixel being a one-dimensional array encompassing three values (R, G, B). Consequently, these images, when converted into numerical data, form a 3D structure of shape (224x224x3), resulting in a 4D data representation.


However, most machine learning models don't directly accommodate 4D data structures, necessitating the flattening of arrays and conversion into data frames. Yet, such data frames can become unwieldy, boasting over 150,000 columns, leading to computational inefficiencies and prolonged processing times. To mitigate this challenge, dimensionality reduction becomes pivotal. After evaluating various hyperparameters, we discovered that reducing dimensions to 100 achieved optimal performance for our MRI scan dataset, resulting in a structured shape of (3109x100).


Addressing class imbalances, we experimented with techniques like random sampling and random over-sampling, although these methodologies either incurred data loss or introduced redundancy, impacting model performance. Furthermore, we explored SMOTE to alleviate these issues. Subsequently, we trained several machine learning models, encompassing KNN, random forest, XGBoost, AdaBoost, Gradient Boost, Stacking, Decision Tree, Naïve Bayes, and Gaussian Processes, among others. KNN emerged as the top-performing algorithm, achieving an unexpected 89.9% accuracy.
KNN's efficacy might stem from its approach, as it distances itself from learning patterns in data, relying instead on measuring distances between images. For instance, the disparity between a white-colored pixel and a black-scaled image significantly contrasts with the similarity between two dark-colored pixels. Consequently, KNN measures similarity based on these distance values.


Probabilistic models exhibited inefficiency within this dataset while refining numerous algorithms consumed considerable time. Intriguingly, certain high-computational-power algorithms showcased performance akin to neural networks. It's apparent that fine-tuning hyperparameters doesn't uniformly enhance outcomes; in this scenario, adjustments led to fluctuations, both positive and negative. This emphasizes the variable nature of fine-tuning, suggesting its potential for improvement without ensuring consistent enhancements across diverse datasets. This complexity highlights the challenges in optimizing models for image recognition tasks.

