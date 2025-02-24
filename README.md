# Resume Screener

## Introduction
This project is a **Resume Category Prediction App** built using **Streamlit**. It allows users to upload resumes in **PDF, DOCX, or TXT format** and predicts the category of the resume using a pre-trained **SVM model with TF-IDF vectorization**.

## Installation
To set up the environment, install the required dependencies using the following commands:

```sh
pip install streamlit
pip install scikit-learn
pip install python-docx
pip install PyPDF2
```

## Files Used
- **`clf.pkl`**: Pre-trained SVM model for classification.
- **`tfidf.pkl`**: TF-IDF vectorizer used during training.
- **`encoder.pkl`**: Label encoder to map category labels.

Ensure these files are in the project directory before running the application.

## How It Works
### 1. Upload Resume
- Users upload a **PDF, DOCX, or TXT** resume.

### 2. Extract Text
- Extracts text using **PyPDF2** (for PDFs) or **python-docx** (for DOCX).

### 3. Preprocess Resume
- Cleans the text using regular expressions.

### 4. Predict Category
- Converts text using the **TF-IDF vectorizer**.
- Predicts the category using a **trained SVM classifier**.
- Outputs the **job category**.

## Usage
Run the Streamlit app with:

```sh
streamlit run app.py
```

Then, follow these steps:
1. Open the **Streamlit UI** in your browser.
2. Upload a resume file.
3. View the extracted text (optional).
4. See the **predicted job category**.

## Code Structure
```sh
├── app.py           # Main Streamlit app
├── clf.pkl         # Pre-trained SVM model
├── tfidf.pkl       # TF-IDF vectorizer
├── encoder.pkl     # Label encoder
├── requirements.txt # Dependencies list
├── README.md       # Documentation
```

## Example Output
After uploading a resume, the app predicts the job category:

```
The predicted category of the uploaded resume is: **Data Scientist**
```

## Contributors
- **Your Name** (your.email@example.com)

## License
This project is licensed under the **MIT License**.

## Future Enhancements
- Improve accuracy with deep learning models.
- Add more categories.
- Implement a **web API** for integration with job portals.

---
Happy Coding! 🚀

