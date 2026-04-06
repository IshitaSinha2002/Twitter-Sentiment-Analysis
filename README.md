<h1>Twitter Sentiment Analysis</h1>

<h2>Overview</h2>
<p>This project performs <b>Sentiment Analysis</b> on textual data using Natural Language Processing (NLP) techniques.
The goal is to classify text (tweets) into <b>Positive</b> or <b>Negative</b> sentiment.</p>
<p>The model is trained on a large-scale dataset of tweets and uses machine learning techniques to identify patterns
in human language and determine sentiment polarity.</p>

<h2>Objective</h2>
<ul>
  <li>Analyze text data and determine sentiment polarity</li>
  <li>Build a robust NLP pipeline for classification</li>
  <li>Understand feature extraction techniques like TF-IDF</li>
  <li>Evaluate model performance using standard metrics</li>
</ul>

<h2>Dataset</h2>
<p>The dataset used is the <b>Sentiment140 dataset</b>, which contains approximately <b>1.6 million tweets</b> labeled for sentiment.
</p>
<ul>
  <li><b>0</b> → Negative</li>
  <li><b>4</b> → Positive (converted to <b>1</b>)</li>
</ul>
<p>Dataset Link: <a href="https://www.kaggle.com/datasets/kazanova/sentiment140" target="_blank">https://www.kaggle.com/datasets/kazanova/sentiment140</a></p>

<h2>Tech Stack</h2>
<ul>
  <li>Python</li>
  <li>Pandas, NumPy</li>
  <li>Matplotlib</li>
  <li>Scikit-learn</li>
  <li>Natural Language Processing (NLP)</li>
</ul>

<h2>Data Preprocessing</h2>
<p>Text data is inherently noisy, so several preprocessing steps were applied:</p>
<ul>
  <li>Converted text to lowercase</li>
  <li>Removed URLs</li>
  <li>Removed Twitter mentions (@user)</li>
  <li>Removed special characters and punctuation</li>
  <li>Stored cleaned text in a separate column</li>
</ul>
<p>These steps reduce noise and standardize the input, making it more suitable for machine learning.</p>

<h2>Exploratory Data Analysis (EDA)</h2>
<p>Basic analysis and visualizations were performed to understand the dataset:</p>
<ul>
  <li>Sentiment distribution (balanced dataset)</li>
  <li>Text length distribution</li>
  <li>Comparison of raw vs cleaned text</li>
</ul>
<p>These insights helped validate data quality and guided preprocessing decisions.</p>

<h2>Feature Engineering</h2>
<h3>TF-IDF Vectorization</h3>
<p>The cleaned text was converted into numerical features using TF-IDF (Term Frequency–Inverse Document Frequency):</p>
<ul>
  <li>Represents text as numerical vectors</li>
  <li>Assigns higher importance to informative words</li>
  <li>Limits features to the most relevant terms</li>
</ul>
<p>This allows the model to effectively learn patterns from textual data.</p>

<h2>Model Building</h2>
<h3>Algorithm Used: Logistic Regression</h3>
<ul>
  <li>Supervised learning algorithm for binary classification</li>
  <li>Efficient and scalable for large datasets</li>
  <li>Performs well with sparse, high-dimensional data like text</li>
</ul>
<p>The model was trained on TF-IDF-transformed features to classify sentiment.</p>

<h2>Model Evaluation</h2>
<p>The model was evaluated using multiple metrics:</p>
<ul>
  <li><b>Accuracy Score</b> → Overall correctness</li>
  <li><b>Confusion Matrix</b> → Breakdown of predictions</li>
  <li><b>Classification Report</b>:
    <ul>
      <li>Precision</li>
      <li>Recall</li>
      <li>F1-score</li>
    </ul>
  </li>
</ul>
<p>These metrics provide a comprehensive understanding of performance.</p>

<h2>Visualizations</h2>
<ul>
  <li>Sentiment distribution bar chart</li>
  <li>Confusion matrix visualization</li>
  <li>Text length histogram</li>
  <li>Top positive and negative contributing words</li>
</ul>

<p>These visual tools help in understanding both dataset characteristics and model behavior.</p>

<h2>Key Insights</h2>
<ul>
  <li>The dataset is balanced, improving model reliability</li>
  <li>TF-IDF effectively captures important textual features</li>
  <li>Logistic Regression performs well for sentiment classification</li>
  <li>Certain words strongly influence sentiment predictions</li>
</ul>

<h2>Prediction System</h2>
<p>A prediction system was implemented to classify new input text into positive or negative sentiment.</p>
<p>The process involves:</p>
<ul>
  <li>Cleaning the input text using the same preprocessing steps</li>
  <li>Transforming the text into numerical form using the trained TF-IDF vectorizer</li>
  <li>Passing the transformed data into the trained model</li>
  <li>Returning the predicted sentiment label</li>
</ul>
<p>This ensures consistency between training and inference, allowing accurate real-time predictions.</p>

<h2>Conclusion</h2>
<p>This project demonstrates how machine learning and NLP techniques can be applied to analyze textual data and extract meaningful insights.
It showcases a complete pipeline from raw data preprocessing to model evaluation and prediction.</p>
