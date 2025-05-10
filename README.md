# BAIT - A Project to detect phishing website using Machine Learning

## What is a Phishing Website?
A phishing website is a fraudulent website designed to look like a legitimate one in order to trick users into revealing sensitive information such as Usernames and passwords, Credit card numbers, Bank account details, Personal identification information (like Aadhaar or PAN in India), etc.

These websites often imitate trusted sites like banks, email providers, social media platforms, or e-commerce stores. Once users enter their information, the data is captured by cybercriminals for misuse.

## Objective of this project
The objective of this project is to train machine learning models and deep neural netwoks on a dataset created to predict phishing websites. Both phishing and legitimate URLs of websites are gathered to form a dataset and from them the requiered URL and website content based features are extracted. On that many machine learning models and neural networks are trained and the performance level of each model is measured and compared.

## Data Collection 
### Phishing URLs
A set of 5000 phishing URLs are collected to train the ML model from an opensource service called PhishTack (https://www.phishtank.com/developer_info.php) which provides a set of phishing URLs in multiple formats like csv, json, etc. 

### Legitimate URLs
The legitimate URLs are obtained from Kaggle. We found a source that has a collection of legitimate and phishing URLs. The link to it is https://www.kaggle.com/datasets/harisudhan411/phishing-and-legitimate-urls?resource=download
This URL collection was downloaded and then from that the 'Legitimate_urls.csv' file is created by extracting only the legitimate URLs from the collection. Out of this collection, a set of 5000 legitimate URLs were sampled randomly for training the models. 

The above mentioned datasets are uploaded to the [Dataset](./Dataset/) folder.

## Feature Extraction
The below mentioned features are extracted from the URL data:
1.URL starting with http or https
2. Domain of URL
3. IP Address in URL
4. "@" Symbol in URL
5. Length of URL
6. Depth of URL
7. Redirection "//" in URL
8. "http/https" in Domain name
9. Using URL Shortening Serives "TinyURL"
10. Prefix or Suffix "-" in Domain
11. No of dots(.)
   
In total there are 11 features extracted from the 10,000 URL dataset and are stored in 'final_dataset.csv' in the Dataset folder. 

The feature extraction is done in the '[Feature Extraction](./FeatureExtraction.ipynb/)'.
