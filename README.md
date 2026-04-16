# 📊 WhatsApp Chat Analyzer Tool

A comprehensive Streamlit web application that helps you analyze your WhatsApp chat exports. Extract meaningful insights, track user activity, understand conversation trends, and visualize emoji usage—all displayed in an interactive dashboard with adaptive themes!

---

## 🚀 Features

- 📬 **Message Statistics**: See total messages, total words, media shared, and links sent.
- 🧑‍🤝‍🧑 **User Analysis**: Find highly active users and their overall contribution percentage in group chats.
- 🕒 **Timeline Visualizations**: Analyze message trends spanning hours, days, and months.
- 📅 **Activity Maps**: Find the busiest days, months, and hours using intuitive heatmaps.
- ☁️ **Word Cloud**: Visualize the most frequently used words (smartly filters out 'Hinglish' stop words).
- 😂 **Emoji Analysis**: Breakdowns of the most used emojis using data tables and pie charts.
- 🌗 **Light/Dark Theme Toggle**: Switch dynamically between bright and dark aesthetic modes with responsive Matplotlib chart styling!

---

## ⚙️ How it Works

The tool relies on data science and NLP processes behind the scenes.
1. **Data Preprocessing**: The raw exported `.txt` file from WhatsApp is parsed by `preprocessor.py` using Regular Expressions (Regex) to correctly split dating, timestamps, users, and message contexts. 
2. **Data Extraction**: `helper.py` processes the parsed data using the `pandas` library, applying various filtering groupings locally. Unnecessary stop words (utilizing `stop_hinglish.txt`) and media-omitted tags are skipped for word analysis.
3. **Data Visualization**: Mathematical calculations and dataset groupings are piped into `matplotlib` and `seaborn` plotting libraries.
4. **Presentation**: The output data visualization and numbers are cleanly laid out on a front-end framework handled by `streamlit`.

---

## 💻 Local Setup & Installation

To run this application locally on your machine, follow these steps:

### Prerequisites:
- Python 3.8+ installed on your system.

### Steps:
1. **Clone the repository** (or download the files locally):
   ```bash
   git clone https://github.com/AmitKumarMaurya92/ChatAnalyzer.git
   cd ChatAnalyzer
   ```

2. **Install the required libraries**:
   Run the following terminal command to install all necessary Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Application**:
   Start the Streamlit development server by running:
   ```bash
   streamlit run app.py
   ```
   The dashboard will automatically open in your default web browser at `http://localhost:8501`.

---

## 📤 How to Export WhatsApp Chat for Analysis

To use the tool, you need to provide a chat history text file from WhatsApp:

1. Open a WhatsApp chat on your phone.
2. Tap the **⋮ (menu icon) > More > Export chat**.
3. Choose **"Without media"** when prompted.
4. Save or email the resulting `.txt` file to yourself.
5. In the running application, upload the `.txt` file in the sidebar to start seeing analytics!

---

## ☁️ Deployment on Render

This web service can be fully deployed online for free via Render!

1. Upload/Push this full code repository to a GitHub account.
2. Sign in to [Render.com](https://render.com/) and click **New + -> Web Service**.
3. Authenticate and connect the GitHub Repository containing these files.
4. **Environment**: Select `Python 3`
5. **Build Command**: 
   ```bash
   pip install -r requirements.txt
   ```
6. **Start Command**: 
   ```bash
   streamlit run app.py --server.port $PORT --server.headless true --server.enableCORS false
   ```
7. Click **Create Web Service**. Wait 3–5 minutes for it to successfully build and deploy!

---

## 🔧 Technologies Used

- **Python**: Core programming language
- **Streamlit**: Web front-end and dashboard framing
- **Pandas**: Machine Learning Dataframe processing
- **Matplotlib & Seaborn**: Charting and plotting libraries
- **WordCloud**: Word weighting models
- **URLExtract**: Finding and parsing URLs efficiently
- **Emoji**: Text emoji recognition

---

## 📃 License
This project is open-source! Feel free to modify and expand its capabilities. 

---

## 🙌 Acknowledgements
- Inspired by countless late-night WhatsApp conversations and deep dives into text analytics ☕
