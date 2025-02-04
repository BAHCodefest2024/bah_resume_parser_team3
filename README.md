

# **Resume Analyzer**: https://github.com/BAHCodefest2024/resume_analyzer_t3`

## **Overview**

**BAH Codefest Submission**: This resume Analyzer is designed to utilize a 1 bit transformer based model to compare the content of resume and job descriptions, outputting a similarity score (descending order) and the m (in descending order) matching words to justify each comparison.

## **Table of Contents**

- [Features](#features)
- [Usage](#usage)
- [Data Preparation](#data-preparation)
- [References](#references)

## **Features**

- **Resume Parsing**: Converts resume PDFs into parsable text format.
- **Job Description Parsing**: Converts job description PDFs into parsable text format.
- **Content Similarity**: Uses an LLM to calculate the similarity between resume and job description content.
- **Score Justification**: Provides a justification for the similarity score based on matching words/phrases.
- **CPU Only Support**:  Utilizes CPU with minimal RAM requirements.

 **Shortcomings of our Implementation**: The text parsing and cleaning does not strip common words (e.g. At, the, into etc.)
 
## **Usage**

### Running the Notebook in Google Colab (Recommended)

1. **Open the Notebook**:
   - Click on the following link to open the notebook in Google Colab: [Colab Notebook](https://colab.research.google.com/drive/1mmXSjQaEHx2NUXYVCKJlMiMctkAWJp4p?usp=sharing)
   -  Model Hugging Face Repo: https://huggingface.co/sentence-transformers/multi-qa-mpnet-base-cos-v1)
   
2. **Install Required Packages**:
   - The notebook will automatically install the necessary packages when you run the first cell.

3. **Clone Data**:
   - The notebook clones and places sample job description PDFs in `/resume_analyzer_t3/data/job_descriptions/`.
   - The notebook clones and places sample resume PDFs in `/resume_analyzer_t3/data/resumes/`.
   
4. **Run the Notebook**:
   - Execute the cells in the notebook sequentially to process the resume and job descriptions, calculate similarity scores, and view the results.

### Running Locally (Optional)

If you prefer to run the notebook locally, follow these steps:

1. **Clone the Repository**:
   - git clone https://github.com/BAHCodefest2024/resume_analyzer_t3/
   - cd resume_analyzer_t3
   
2. **Install Required Packages**:
   - pip install -q git+https://github.com/huggingface/transformers.git
   - pip install -q torch git-lfs bitsandbytes accelerate peft sentence-transformers pypdf kaleido beautifulsoup4

3. **Open the Notebook:**:
   - Open ~/resume_analyzer_t3/
   
4. **Prepare Data**:
   - Place job descriptions in  `/resume_analyzer_t3/data/job_descriptions/`
   - Place resume in  `/resume_analyzer_t3/data/resumes/`
  
   
5. **Run the Notebook**:
   - Execute the cells in the notebook sequentially to process the resume and job descriptions, calculate similarity scores, and view the results.
   
## **Data Storage**

Confirm that job descriptions and resume are in the correct directories:

 **Job Descriptions**: `/resume_analyzer_t3/data/job_descriptions/`
 
 **Resumes**: `/resume_analyzer_t3/data/resumes/`

## **References**

### **Microsoft Bitnet:**
* https://github.com/microsoft/BitNet
* https://papeg.ai/#
*  https://colab.research.google.com/drive/1ovmQUOtnYIdvcBkwEE4MzVL1HKfFHdNT?usp=sharing
* https://huggingface.co/blog/1_58_llm_extreme_quantization
  #### 1 bit LLMs:
  * https://huggingface.co/collections/HF1BitLLM/llama3-8b-158-66e6003b038300b07a34c4f3
  * https://huggingface.co/1bitLLM/activity/models

### **Sentence Transformer Documentation & Pretrained 1B Models**
* https://sbert.net/examples/applications/semantic-search/README.html
* https://sbert.net/docs/sentence_transformer/pretrained_models.html

### **PyPDF:**
* https://pypi.org/project/pypdf/

### **spaCy:**
* https://spacy.io/usage/spacy-101
* https://www.analyticsvidhya.com/blog/2020/03/spacy-tutorial-learn-natural-language-processing/

### **Gauge Implementation:**
* https://github.com/kirudang/CV-Job-matching/blob/main/Matching_Algorithm.ipynb


