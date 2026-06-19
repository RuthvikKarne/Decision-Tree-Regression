<h1 align="center">Decision Tree Regression on Housing Dataset</h1>

<p>This repository contains a simple, yet comprehensive, demonstration of using a Decision Tree Regression model to predict California housing prices.</p>

<h2>Project Overview</h2>
<p>The project aims to predict the <code>median_house_value</code> for districts in California using various features such as location, median income, and housing characteristics. The machine learning pipeline is implemented in a Jupyter Notebook (<code>app.ipynb</code>) and uses the <code>scikit-learn</code> library.</p>

<h2>Dataset</h2>
<p>The model uses the <code>housing.csv</code> dataset, which contains the following features:</p>
<ul>
  <li><b>longitude:</b> A measure of how far west a house is; a higher value is farther west</li>
  <li><b>latitude:</b> A measure of how far north a house is; a higher value is farther north</li>
  <li><b>housing_median_age:</b> Median age of a house within a block; a lower number is a newer building</li>
  <li><b>total_rooms:</b> Total number of rooms within a block</li>
  <li><b>total_bedrooms:</b> Total number of bedrooms within a block</li>
  <li><b>population:</b> Total number of people residing within a block</li>
  <li><b>households:</b> Total number of households, a group of people residing within a home unit, for a block</li>
  <li><b>median_income:</b> Median income for households within a block of houses (measured in tens of thousands of US Dollars)</li>
  <li><b>ocean_proximity:</b> Location of the house w.r.t ocean/sea</li>
</ul>

<p><b>Target Variable:</b></p>
<ul>
  <li><b>median_house_value:</b> Median house value for households within a block (measured in US Dollars)</li>
</ul>

<h2>Workflow</h2>
<p>The notebook <code>app.ipynb</code> walks through the following machine learning lifecycle steps:</p>
<ol>
  <li><b>Data Loading:</b> Imports the data using <code>pandas</code>.</li>
  <li><b>Exploratory Data Analysis (EDA):</b> Analyzes the dataset's structure, missing values, and statistical summary.</li>
  <li><b>Data Preprocessing:</b>
    <ul>
      <li>Handles missing values in the <code>total_bedrooms</code> column by imputing them with the median value.</li>
      <li>Encodes the categorical feature <code>ocean_proximity</code> using one-hot encoding (<code>pd.get_dummies</code>).</li>
    </ul>
  </li>
  <li><b>Data Splitting:</b> Separates the dataset into features (<code>X</code>) and the target variable (<code>y</code>), followed by a train-test split (80% training, 20% testing).</li>
  <li><b>Model Training:</b> Initializes and fits a <code>DecisionTreeRegressor</code> on the training data.</li>
  <li><b>Model Evaluation:</b> Predicts housing values on the test set and calculates the Mean Absolute Error (MAE) to measure model performance.</li>
  <li><b>Visualization:</b> Plots the decision tree structure to visualize the splitting rules.</li>
</ol>

<h2>Setup Instructions</h2>
<p>To run this project locally, follow these steps:</p>

<h3>Prerequisites</h3>
<p>Make sure you have Python installed. You will also need Jupyter Notebook or JupyterLab to run the <code>.ipynb</code> file.</p>

<h3>Installation</h3>
<ol>
  <li><b>Clone the repository:</b>
    <pre><code>git clone &lt;repository-url&gt;
cd Decision-Tree-Regression</code></pre>
  </li>
  <li><b>Install the required dependencies:</b>
    <p>It is recommended to use a virtual environment. You can install the required packages using:</p>
    <pre><code>pip install pandas scikit-learn matplotlib jupyter</code></pre>
  </li>
  <li><b>Run the Notebook:</b>
    <pre><code>jupyter notebook app.ipynb</code></pre>
    <p>Execute the cells in the notebook sequentially to see the data processing, model training, and evaluation in action.</p>
  </li>
</ol>

<h2>Results</h2>
<p>The model's performance is evaluated using the <b>Mean Absolute Error (MAE)</b>, which provides an estimate of the average prediction error in dollars. The notebook also outputs a detailed visual representation of the trained decision tree.</p>

<h2>License</h2>
<p>This project is open-source and available for educational purposes.</p>
