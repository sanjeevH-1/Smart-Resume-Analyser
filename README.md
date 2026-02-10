# 📄 AI Resume Analyzer

![AI-Resume-Analyzer-Banner](https://socialify.git.ci/sanjeevH-1/Smart-Resume-Analyser/image?description=1&descriptionEditable=Advanced%20Resume%20Analysis%2C%20Predictions%20%26%20Recommendations&font=Raleway&language=1&pattern=Plus&theme=Light)

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

**A powerful tool aimed at helping students and professionals analyze their resumes, get predictions on suitable job roles, and receive personalized recommendations to improve their chances of getting hired.**

[Features](#-features) • [Tech Stack](#-tech-stack) • [Installation](#-installation) • [Usage](#-usage) • [Contributing](#-contributing)

</div>

---

## 🚀 Overview

The **AI Resume Analyzer** is a sophisticated application designed to parse resumes, extract key information, and provide actionable insights. It serves both job seekers and recruiters by offering a dual-interface system:

*   **For Candidates:** Analyzes resume strength, suggests skills, predicts suitable job roles, and recommends courses and videos.
*   **For Recruiters (Admin):** Visualizes applicant data, tracks trends, and manages candidate profiles efficiently.

## ✨ Features

### 👤 User (Client) Side
*   **Smart Parsing:** Automatically extracts basic info, skills, and keywords from PDF resumes.
*   **Intelligent Recommendations:**
    *   Missing skills analysis.
    *   Predicted job role suitability.
    *   Curated course and certificate recommendations.
    *   Resume improvement tips.
    *   Interview preparation videos.
*   **Scoring System:** Calculates an overall resume score to benchmark quality.

### 🛡️ Admin Side
*   **Data Analytics:** Comprehensive dashboard with pie charts for:
    *   Predicted roles & experience levels.
    *   Resume scores & user ratings.
    *   Demographic insights (City, State, Country).
*   **Data Management:**
    *   View all applicant data in tabular format.
    *   Download parsed data as CSV.
    *   Access original PDF resumes.
*   **Feedback System:** Track user ratings and feedback history.

## 🛠 Tech Stack

| Component | Technologies |
| :--- | :--- |
| **Frontend** | [Streamlit](https://streamlit.io/), HTML, CSS, JavaScript |
| **Backend** | Python (feature-rich logic) |
| **Database** | MySQL |
| **NLP & ML** | `pyresparser`, `pdfminer3`, `NLTK`, `spacy`, `pandas` |
| **Visualization** | Plotly |

## ⚙️ Installation

Follow these steps to set up the project locally.

### Prerequisites
*   [Python 3.9+](https://www.python.org/downloads/)
*   [MySQL Server](https://www.mysql.com/downloads/)
*   [Visual Studio Build Tools](https://aka.ms/vs/17/release/vs_BuildTools.exe) (for C++ dependencies)

### Step-by-Step Guide

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/sanjeevH-1/Smart-Resume-Analyser.git
    cd AI-Resume-Analyzer-main
    ```

2.  **Set Up Virtual Environment** (Recommended)
    ```bash
    python -m venv venvapp
    
    # Activate script
    # Windows:
    .\venvapp\Scripts\activate
    # macOS/Linux:
    source venvapp/bin/activate
    ```

3.  **Install Dependencies**
    Navigate to the `App` directory and install the required packages:
    ```bash
    cd App
    pip install -r requirements.txt
    python -m spacy download en_core_web_sm
    ```

4.  **Database Configuration**
    *   Create a MySQL database named `cv`.
    *   Update the database credentials in `App/App.py` (Search for the connection string or configuration section).

5.  **Patch `pyresparser`**
    *   Locate the `resume_parser.py` file inside your project's `pyresparser` folder.
    *   Copy it and replace the file in your virtual environment library:
        `venvapp\Lib\site-packages\pyresparser\resume_parser.py`

## 🏃 Usage

1.  **Run the Application**
    Ensure your virtual environment is active and you are in the `App` directory:
    ```bash
    streamlit run App.py
    ```

2.  **Access the Interface**
    *   The app will open in your default browser.
    *   **User Mode:** Select "User" to upload and analyze resumes.
    *   **Admin Mode:** Select "Admin" to view analytics.
        *   **Username:** `admin`
        *   **Password:** `admin@resume-analyzer`

> **Note:** If you encounter a `GeocoderUnavailable` error, please check your internet connection.

## 🛣 Roadmap

*   [x] Predict user experience level
*   [x] Implement scoring criteria for skills and projects
*   [x] Recommendations for Web, Android, iOS, and Data Science roles
*   [x] Advanced detail fetching from resumes
*   [ ] Expand role support (DevOps, Blockchain, etc.)
*   [ ] Individual user detail view for Admin
*   [ ] Dark mode support

## 🤝 Contributing

Contributions are welcome! Please feel free to check the [issues page](https://github.com/sanjeevH-1/Smart-Resume-Analyser/issues) or submit a Pull Request.

1.  Fork the project
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 👏 Acknowledgements

*   **Dr. Bright** - *The Full Stack Data Scientist BootCamp*
*   **Omkar Pathak** - Creator of `pyresparser`
*   Research paper: *Resume Parser with Natural Language Processing*

---

<p align="center">
  Built with ❤️ by <a href="https://github.com/sanjeevH-1">Sanjeev Hanchinal</a>
</p>
