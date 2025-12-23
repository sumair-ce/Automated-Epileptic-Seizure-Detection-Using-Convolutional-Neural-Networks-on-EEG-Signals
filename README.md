<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
<h1 align="left">Epileptic Seizure Detection Using 1D CNN</h1>
<p>Automated epileptic seizure detection from EEG signals using a 1D Convolutional Neural Network. Distinguishes ictal (seizure) from interictal/non-seizure states with high precision.</p>

<h2>Features</h2>
<ul>
    <li>Binary classification of EEG signals (seizure vs. non-seizure)</li>
    <li>Exploratory Data Analysis with spectrograms and power spectral density</li>
    <li>Feature normalization and stratified train-test split</li>
    <li>1D CNN architecture with batch normalization and dropout</li>
    <li>Performance evaluation: loss/accuracy curves, confusion matrix, precision-recall metrics</li>
    <li>Literature review (2019–2025)</li>
</ul>

<h2>Technical Overview</h2>
<ul>
    <li><b>Model Architecture:</b> 1D CNN with three Conv1D blocks (32-64-128 filters), MaxPooling, Flatten, Dense layer, Dropout (0.5), Sigmoid output</li>
    <li><b>Training:</b> Adam optimizer, Binary Cross-Entropy loss, 50 epochs, Early Stopping</li>
</ul>

<h2>Dataset</h2>
<p>Uses the <a href="https://www.kaggle.com/datasets/subirbiswas19/eeg-dataset" target="_blank">subirbiswas19/eeg-dataset</a> on Kaggle (pre-processed UCI Epileptic Seizure Recognition Dataset, Bonn University). 11,500 samples, 178 time points per second-long EEG recording.</p>

<h2>Model Performance</h2>
<h3>Performance Metrics</h3>
<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr>
            <th>Metric</th>
            <th>Value</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Accuracy</td><td>95.68%</td></tr>
        <tr><td>Precision</td><td>93.18%</td></tr>
        <tr><td>Recall (Sensitivity)</td><td>71.43%</td></tr>
        <tr><td>F1-Score</td><td>80.87%</td></tr>
    </tbody>
</table>

<h3>Confusion Matrix</h3>
<table border="1" cellpadding="8" cellspacing="0">
    <thead>
        <tr><th></th><th>Predicted Non-Seizure</th><th>Predicted Seizure</th></tr>
    </thead>
    <tbody>
        <tr><td>Actual Non-Seizure</td><td>1945 (TN)</td><td>15 (FP)</td></tr>
        <tr><td>Actual Seizure</td><td>82 (FN)</td><td>205 (TP)</td></tr>
    </tbody>
</table>

<h2>Usage</h2>
<p>Ideal for real-time epileptic seizure monitoring systems. Provides efficient, automated detection from raw EEG signals using deep learning.</p>

<h2>Acknowledgments</h2>
<ul>
    <li>UCI Epileptic Seizure Recognition Dataset (Bonn University)</li>
    <li>Kaggle dataset by subirbiswas19</li>
    <li>Open-source deep learning frameworks (Keras/TensorFlow)</li>
</ul>
</body>
</html>
