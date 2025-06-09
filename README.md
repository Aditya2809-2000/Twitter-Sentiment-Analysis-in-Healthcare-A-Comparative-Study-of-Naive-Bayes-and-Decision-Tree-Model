Twitter Healthcare Sentiment Analysis
Project Overview
This study investigates the application of sentiment analysis on healthcare-related Twitter data to understand public opinion and sentiment. Leveraging Apache Spark for big data processing, we compare the performance of Naïve Bayes and Decision Tree classification models in categorizing sentiments as positive or negative. The project aims to extract valuable insights from large volumes of unstructured text data, contributing to advancements in healthcare informatics and informing news media's approach to healthcare issues.

Problem Statement
With the ever-increasing volume of text data generated online, particularly on social media platforms like Twitter, there's a significant opportunity to gauge public sentiment towards critical domains like healthcare. This project addresses the challenge of accurately classifying these sentiments, providing insights that can influence public health policy and practice.

Methodology
Our approach involved several key stages:

Data Collection: Healthcare-related tweets were gathered from various major health news organizations.

Data Preprocessing and Cleaning: Apache Spark on Databricks was utilized to preprocess and clean the raw Twitter data. This included removing URLs, special characters, stop words, and applying natural language processing techniques such as tokenization, stemming, and lemmatization. The data was then labeled with initial sentiment scores (Positive/Negative).

Feature Extraction: Text data was transformed into a numerical format suitable for machine learning models using a Bag-of-Words (BoW) representation. Publication names and sentiment labels were converted using a string indexer. One-hot encoding was applied to categorical features.

Model Implementation: Naïve Bayes and Decision Tree models were developed and trained. The data was split into 70% for training and 30% for testing. Cross-validation measures were used to optimize model parameters and prevent overfitting.

Performance Evaluation: Models were assessed using standard metrics: F1 score, precision, and recall. Confusion matrices were generated to illustrate each model's successes and weaknesses.

Computational Efficiency Assessment: The training times and resource utilization of both models were evaluated, particularly in the context of Apache Spark's big data capabilities.

Results and Discussion
Performance Comparison
Model

Training Time (approx.)

F1 Score

Bias Towards Positive

Naïve Bayes

80 seconds

0.854

Minimal

Decision Tree

13 minutes

0.743

Significant

Naïve Bayes consistently outperformed the Decision Tree model in terms of F1 score and computational efficiency. It demonstrated minimal bias, indicating better generalization to new data.

Decision Tree, despite parameter optimization, showed a strong bias towards predicting positive labels, leading to a lower F1 score and significantly higher training time, especially with larger datasets and deeper trees.

Computational Efficiency with Apache Spark
The Bag-of-Words (BoW) representation of Twitter data, combined with robust preprocessing, proved highly effective for a big data approach to sentiment analysis using Apache Spark.

Naïve Bayes, due to its strong assumptions of feature independence, was remarkably efficient in training, processing over 42,000 rows (70% of the dataset) in just over a minute.

While visualization involved converting Spark DataFrames to Pandas, which could pose scalability issues for even larger datasets, for this study's scope, it was manageable.

Conclusion
This study effectively demonstrates the capabilities of Naïve Bayes and Decision Tree models in sentiment analysis of healthcare tweets. It highlights that the Multinomial Naïve Bayes model is particularly well-suited for text classification tasks due to its efficiency, accuracy, and ability to handle word frequencies. The research also underscores the immense potential of Apache Spark for processing vast amounts of data in healthcare informatics, enabling rapid extraction of valuable insights from unstructured text.

For future work, exploring advanced decision tree evolutions like BFTree could potentially improve performance and address the efficiency challenges encountered with traditional Decision Tree models in big data environments.

Getting Started
To replicate this study or use the code:

Clone the repository:

git clone https://github.com/your-username/twitter-healthcare-sentiment-analysis.git
cd twitter-healthcare-sentiment-analysis

Set up your Apache Spark/Databricks environment:
(Further instructions on setting up Spark and Databricks, including dependencies and environment configuration, would go here. You would likely need to detail specific library installations, e.g., pyspark, nltk, etc.)

Data Acquisition:
(Provide instructions on how to obtain or prepare the Twitter dataset used in the study. If it's a public dataset, link to it. If it's proprietary, explain how a user could use their own similar data.)

Run the analysis:
(Provide clear steps on how to execute the Jupyter notebooks or scripts for data preprocessing, model training, and evaluation.)

Contributing
Contributions are welcome! Please feel free to open an issue or submit a pull request if you have suggestions for improvements, bug fixes, or new features.

Contact
For feedback and inquiries, please contact us through the project repository or reach out to the authors listed in the original paper:

Kieran Fox (psykf2@nottingham.ac.uk)

Aditya Kumar Sasmal (psxas24@nottingham.ac.uk)

Ashwini Bharat Doke (psxad11@nottingham.ac.uk)

Shruthi Chinni (psxsc19@nottingham.ac.uk)
