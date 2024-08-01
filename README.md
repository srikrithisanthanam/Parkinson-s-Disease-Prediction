# Parkinson-s-Disease-Prediction
A Machine Learning Approach for the Diagnosis of Parkinson's Disease via Speech Analysis
<br><br>
<b><h2>Introduction</h2></b>
<br>
Parkinson's Disease ranks as the second most prevalent neurodegenerative disorder after Alzheimer's, affecting over 10 million people worldwide. It primarily manifests through the decline of motor and cognitive functions. Diagnosing Parkinson's is challenging due to the absence of a single definitive test; instead, physicians must conduct a thorough clinical evaluation of the patient's medical history. This method, however, is often unreliable. A study by the National Institute of Neurological Disorders indicates that the accuracy of early diagnosis (within the first five years of symptom onset) is only 53%, which is barely better than random guessing. Yet, early diagnosis is vital for effective treatment.<br>
<br>
<b><h2>Dataset Used and Description</b></h2><br>
Given these diagnostic difficulties, I am exploring a machine learning approach to enhance the accuracy of Parkinson's diagnosis, using a dataset of various speech features provided by the University of Oxford. Speech features are highly indicative of Parkinson's disease because nearly every patient with Parkinson's experiences significant vocal degradation, such as difficulties with sustained phonation, tremors, and hoarseness. Thus, using voice analysis for diagnosis is logical. Additionally, this method is non-invasive, inexpensive, and easy to perform in clinical settings.<br>
<br><ul>
<li>Source: the University of Oxford</li>
<li>195 instances (147 subjects with Parkinson’s, 48 without Parkinson’s)</li>
<li>22 features (elements that are possibly characteristic of Parkinson’s, such as frequency, pitch, amplitude / period of the sound wave)</li>
<li>1 label (1 for Parkinson’s, 0 for no Parkinson’s)</li></ul>
<br>
<b>Performance Metrics</b><br>
<br>TP = true positive, FP = false positive, TN = true negative, FN = false negative
<br><b>Accuracy:</b>(TP+TN)/(P+N)
<br><b>Matthews Correlation Coefficient:</b> 1=perfect, 0=random, -1=completely inaccurate<br>

<b><h2>Algorithms Employed</h2></b>
<br>
<ul>
  <li>Logistic Regression (LR): Uses the sigmoid logistic equation with weights (coefficient values) and biases (constants) to model the probability of a certain class for binary classification. An output of 1 represents one class, and an output of 0 represents the other. Training the model will learn the optimal weights and biases.</li>
  <li>k Nearest Neighbors (KNN): Makes predictions about the validation set using the entire training set. KNN makes a prediction about a new instance by searching through the entire set to find the k “closest” instances. “Closeness” is determined using a proximity measurement (Euclidean) across all features. The class that the majority of the k closest instances belong to is the class that the model predicts the new instance to be.</li>
  <li>Decision Tree (DT): Represented by a binary tree, where each root node represents an input variable and a split point, and each leaf node contains an output used to make a prediction.</li>
  <li>Naive Bayes (NB): Simplifies the calculation of probabilities by assuming that all features are independent of one another (a strong but effective assumption). Employs Bayes Theorem to calculate the probabilities that the instance to be predicted is in each class, then finds the class with the highest probability.</li>
  <li>Gradient Boost (GB): Generally used when seeking a model with very high predictive performance. Used to reduce bias and variance (“error”) by combining multiple “weak learners” (not very good models) to create a “strong learner” (high performance model). Involves 3 elements: a loss function (error function) to be optimized, a weak learner (decision tree) to make predictions, and an additive model to add trees to minimize the loss function. Gradient descent is used to minimize error after adding each tree (one by one).</li>
</ul>
<b><h2>Results</h2></b>
<br><center>
  
![image](https://github.com/user-attachments/assets/8bde04ac-103e-4605-90a0-bb1fb84763ce)
</center>

