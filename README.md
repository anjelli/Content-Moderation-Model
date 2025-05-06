# Content-Moderation-Model
# Automated Content Moderation System

### A Machine Learning-Based Text and Image Content Filter

---

## Overview

This is a personal project aimed at building an **automated content moderation system** that can identify whether input text is appropriate or offensive. The system uses **natural language processing (NLP)** techniques and deep learning models like **LSTM** and **BERT** to classify textual content.

In addition to handling raw text, it also processes images (such as memes) by extracting embedded text using the **Google Cloud Vision API**, allowing moderation of content within images.

**Note:** This project is currently **not deployed**. However, the functionality can be fully simulated locally by following the instructions provided.

---

## Project Structure

- `Data_Preprocessing.ipynb`: Cleans and preprocesses the dataset (`hate_offensive_data.csv`) for training.
- `LSTM.ipynb`: Trains and evaluates an LSTM-based classifier on the preprocessed dataset.
- `BERT.ipynb`: Trains and evaluates a BERT-based classifier for the same task.
- `Flask_app/main.py`: Backend script (Flask) to run the moderation system through a browser interface.
- `Flask_app/templates/index5.html`: Frontend HTML page for inputting text or uploading images.
- `Flask_app/app.yaml`: Deployment configuration file (not used in this version).
- `requirements.txt`: List of required Python packages.

---

## How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/automated-content-moderation.git
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Preprocess the data:
   - Open and run `Data_Preprocessing.ipynb` to generate `preprocessed_data.csv`.

4. Train the models:
   - Run `LSTM.ipynb` and `BERT.ipynb` separately to train both models.
   - BERT may take longer to train; it is recommended to use Google Colab for improved performance.

---

## Results

Both models were evaluated using standard classification metrics. The following table summarizes their performance:

| Metric     | LSTM     | BERT     |
|------------|----------|----------|
| Accuracy   | 93.65%   | 95.62%   |
| Precision  | 95.97%   | 97.20%   |
| Recall     | 96.41%   | 97.55%   |
| F1 Score   | 96.19%   | 97.37%   |

BERT outperformed LSTM across all metrics, making it the preferred model for this task.

---
