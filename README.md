
# Resume Categorization App

## Overview

This is a **Resume Categorization** app built using **Streamlit** and **Machine Learning**. The app allows users to upload resumes in PDF format, which are then categorized into various job domains using a **Logistic Regression** model. The app stores categorized resumes in folders and generates a CSV file containing the filename and corresponding category.

## Project Structure

```
Resume-Categorization/
│
├── app.py                   
├── application.ipynb        
├── model/                   
│   ├── model.pkl            
│   └── tfidf.pkl            
├── data/
│   └── ResumeDataSet.csv    
```

## Requirements

To run this app, you will need to install the following dependencies:

- Python 
- Streamlit
- scikit-learn
- PyPDF2
- pandas
- pickle



## How to Use

### 1. Launch the App
Run the Streamlit app by executing:

```bash
streamlit run app.py
```

This will start the Streamlit app and open it in your browser.

### 2. Upload Resumes
- Click the file uploader to select multiple PDF resumes for processing.
- The app will process the resumes and categorize them based on their content.

### 3. Categorize the Resumes
- After uploading the resumes, click the "Categorize Resumes" button.
- The app will display a table with the filename and its assigned category.
- The categorized resumes will be stored in folders named after the predicted categories.

### 4. Download Results
- After categorization, you can download the results as a CSV file that contains the filenames and their respective categories.
- The CSV file will be available for download directly from the app.

### 5. Directory Structure
- The categorized resumes will be stored in the output directory, organized into folders for each category.
  - Example: `categorized_resumes/Java Developer/Resume1.pdf`

## File Descriptions

### `app.py`

This file contains the Streamlit application code. It handles:
- Uploading resumes
- Categorizing the resumes using the pre-trained model
- Saving the categorized resumes in respective folders
- Generating and providing a downloadable CSV file with the results

### `application.ipynb`

This Jupyter Notebook is used for:
- Training the machine learning model using a dataset of resumes (`ResumeDataSet.csv`).
- Evaluating the model's performance.
- Saving the trained model (`model.pkl`) and the TF-IDF vectorizer (`tfidf.pkl`).

### `model/model.pkl`

This is the trained **Logistic Regression** model used to categorize resumes. It is used by the `app.py` file to predict the category of the uploaded resume.

### `model/tfidf.pkl`

This file contains the **TF-IDF vectorizer** that is used to transform the text data (cleaned resume) into numerical features that can be fed into the model for categorization.

### `data/ResumeDataSet.csv`

This CSV file contains the dataset of resumes used to train the machine learning model. Each row represents a resume with its associated category.

## Category Mapping

The app categorizes resumes into the following job domains:

- **0**: Advocate
- **1**: Arts
- **2**: Automation Testing
- **3**: Blockchain
- **4**: Business Analyst
- **5**: Civil Engineer
- **6**: Data Science
- **7**: Database
- **8**: DevOps Engineer
- **9**: DotNet Developer
- **10**: ETL Developer
- **11**: Electrical Engineering
- **12**: HR
- **13**: Hadoop
- **14**: Health and Fitness
- **15**: Java Developer
- **16**: Mechanical Engineer
- **17**: Network Security Engineer
- **18**: Operations Manager
- **19**: PMO
- **20**: Python Developer
- **21**: SAP Developer
- **22**: Sales
- **23**: Testing
- **24**: Web Designing

## Conclusion

The Resume Categorization App helps automate the process of categorizing resumes into different job domains using machine learning. It provides a user-friendly interface for uploading resumes, categorizing them, and downloading the results.
