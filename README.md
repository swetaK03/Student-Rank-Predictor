# Student Rank Predictor

## Project Overview
This project aims to analyze Testline quiz performance and predict student ranks based on past NEET exam results. The solution processes quiz data, extracts insights, and builds a model to estimate a student’s probable NEET rank. Additionally, it predicts the most likely college a student could get admitted to based on their rank.

## App Link
[NEET Testline - Google Play](https://play.google.com/store/apps/details?id=com.neet.testline)

## Tech Stack
- **Node.js** (Backend processing)
- **Express.js** (API handling)
- **MongoDB** (Database for storing quiz data)
- **React.js** (Frontend for user interaction)
- **Python (Optional)** (For advanced data analysis and ML model)

## Data Overview
The solution works with two datasets:
1. **Current Quiz Data:** Details of a user’s latest quiz submission, including questions, topics, responses, and overall score.
   - Source: Quiz API Endpoint
   - Data: Quiz Submission Data
   
2. **Historical Quiz Data:** Performance data from the last 5 quizzes for each user.
   - Source: API Endpoint
   - Data: Score trends and response map (Key: Question ID, Value: Selected Option ID)

## Features
- **Data Analysis:** Identifies patterns in student performance by topics, difficulty levels, and response accuracy.
- **Insight Generation:** Highlights weak areas, improvement trends, and performance gaps for each student.
- **Rank Prediction:** Uses a probabilistic model to estimate the student’s NEET rank based on their quiz performance and historical NEET results.
- **College Admission Prediction (Bonus):** Predicts the most likely college a student could be admitted to based on the estimated rank.

## Installation & Setup
1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/student-rank-predictor.git
   cd student-rank-predictor
   ```
2. **Install Dependencies**
   ```bash
   npm install
   ```
3. **Set Up Environment Variables**
   Create a `.env` file in the root directory and configure:
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   API_KEY=your_api_key
   ```
4. **Start the Server**
   ```bash
   npm start
   ```
   The server will run on `http://localhost:5000`.

5. **Start the Frontend**
   ```bash
   cd client
   npm install
   npm start
   ```
   The React.js frontend will run on `http://localhost:3000`.

## API Endpoints
- **GET /api/quiz/current** – Fetch the latest quiz submission data.
- **GET /api/quiz/history** – Retrieve historical quiz performance.
- **POST /api/predict-rank** – Predict student rank based on quiz data.
- **POST /api/predict-college** – Predict the most likely college based on rank.

## Approach
1. **Data Preprocessing:**
   - Extract quiz performance metrics.
   - Clean and normalize data for analysis.
2. **Performance Analysis:**
   - Identify weak topics and accuracy trends.
3. **Rank Prediction Model:**
   - Uses statistical/probabilistic methods to estimate rank.
4. **College Prediction:**
   - Maps predicted rank to historical NEET admission data.

## Future Improvements
- Enhance prediction accuracy using ML models.
- Expand dataset coverage for more precise results.
- Improve UI/UX of the React frontend.

## Contributors
-  ([SWETAK03]((https://github.com/swetaK03)))



