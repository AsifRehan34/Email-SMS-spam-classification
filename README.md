# Email Spam Classification Project

## Overview

This project demonstrates how to build a machine learning model to classify emails as either "spam" or "ham" (not spam). Using the `Naive Bayes` algorithms, we preprocess the text data, vectorize it, and apply various classifiers to predict whether a given email is spam or not. The project is implemented in Python and leverages popular libraries such as `scikit-learn`, `pandas`, and `nltk`.

## Dataset

The dataset used for this project was sourced from Kaggle and contains two columns:
- **Category**: Indicates whether the email is "spam" or "ham".
- **Message**: Contains the email content.

The dataset can be found in the `/Dataset` folder in the project directory.

## Project Structure

- `Dataset/`: Contains the email spam dataset.
- `main.py`: The main Python script that contains the entire workflow for preprocessing, training, and testing the models.
- `README.md`: This file, providing an overview of the project.
- `requirements.txt`: List of Python dependencies required to run the project.

## Requirements

Before running the project, ensure you have the following Python libraries installed:

```bash
pip install pandas scikit-learn nltk
```

## Project Workflow

### 1. Data Preprocessing

The raw email text data is preprocessed to make it suitable for machine learning models. This includes:
- Removing punctuation.
- Converting text to lowercase.
- Tokenizing the text into words.
- Removing stopwords (commonly used words with little semantic meaning).
- Optional: Stemming words to their base form.

### 2. Feature Engineering

The preprocessed text data is then vectorized using `CountVectorizer`. The vectorizer converts the text data into a binary matrix, where each word in the vocabulary is represented as a feature. This binary representation is used as input for the machine learning models.

### 3. Model Training and Evaluation

Multiple `Naive Bayes` models are trained and evaluated, including:
- **Multinomial Naive Bayes**
- **Bernoulli Naive Bayes**

The dataset is split into 70% training and 30% testing data to evaluate the performance of these models.

### 4. Results

The models' performance is evaluated using the following metrics:
- **Accuracy**: Proportion of correctly classified emails.
- **Confusion Matrix**: A matrix showing the correct and incorrect classifications.
- **Precision**: The ratio of correctly predicted positive observations to the total predicted positives.

### 5. Predictions on New Emails

The trained models are also used to classify new email samples as "spam" or "ham". The results are printed to the console.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/email-spam-classification.git
   cd email-spam-classification
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the main script:
   ```bash
   python main.py
   ```

4. The script will output the accuracy and precision of the models, along with predictions for sample emails.

## Example Output

The script will classify sample emails as either "spam" or "ham". Here is an example of the output you might see:

```bash
Prediction Results for New Emails:
spam
ham
spam
ham
```

## Contributions

Contributions are welcome! If you have suggestions or improvements, feel free to fork the repository and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

